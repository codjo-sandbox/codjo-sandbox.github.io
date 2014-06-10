---
layout: post
title: agf-agent - Mock d'agents
tags: [framework-1-96,codjo-agent]
---
Ajout de la méthode ```mock``` dans la classe ```StoryRecorder``` permettant de simuler un système d'agent représenté par la classe abstraite ```SystemMock```.
```java
public <T extends SystemMock> T mock(T systemMock);
```

Exemple : 
```java
   public void test_mock() throws Exception {
        story.record().mock(new MySystemMock())
              .startAgent("bobo");

        story.record().assertContainsAgent("bobo");

        story.execute();
    }


    private static class MySystemMock extends SystemMock {
        private Story story;

        @Override
        protected void record(Story myStory) {
            this.story = myStory;
        }


        public void startAgent(String nickName) {
            story.record().startTester(nickName);
        }
    }
```