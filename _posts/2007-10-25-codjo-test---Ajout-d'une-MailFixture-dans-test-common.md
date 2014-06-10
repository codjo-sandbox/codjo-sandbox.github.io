---
layout: post
title: agf-test - Ajout d'une MailFixture dans test-common
tags: [codjo-test,framework-1-18]
---
Instanciation :
```
private MailFixture mailFixture = new MailFixture(99);
```
setUp() :
```
protected void setUp() throws Exception {
    super.setUp();
    mailFixture.doSetUp();
}
```
tearDown() :
```
protected void tearDown() throws Exception {
        mailServer.doTearDown();
}
```
Exemple de test :
```
public void test_spamTheKid() throws Exception {
    MySpamMailer.sendMail("darth.Vader", "luke.Skywalker", "révélation", "Je suis ton père");

    List<MailMessage> messageList = mailFixture.getReceivedMessages();
    assertEquals(1, messageList.size());
    MailMessage message = mailFixture.getReceivedMessage(0);
    message.assertThat()
              .from("darth.Vader")
              .to("luke.Skywalker")
              .subject("révélation")
              .bodyContains("Je suis ton père");
}
```
Note : Utiliser un port différent de 25 sinon le proxy de mail Symantec installé sur le réseau bloquera l'envoi du message.