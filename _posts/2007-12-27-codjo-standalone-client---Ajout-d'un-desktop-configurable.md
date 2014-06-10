---
layout: post
title: agf-standalone-client - Ajout d'un desktop configurable
tags: [codjo-standalone-client,framework-1-25]
---
Pour pouvoir différencier les environnements de Développement, Intégration, Recette et Production, codjo-standalone-client offre la possibilité de configurer l'apparence du bureau via l'interface **DesktopPaneCustomizer** et son implémentation par défaut **DefaultDesktopPaneCustomizer**.

Il est possible de configurer :
* l'image de fond via les méthodes ```setIconFor(Environment, String)``` (image de fond spécifique à l'environnement) et ```setDefaultIcon(Icon)``` (image de fond par défaut),
* un texte sous l'image via les méthodes ```setLabelFor(Environment, String)``` (texte spécifique à l'environnement) et ```setDefaultLabel(String)``` (texte par défaut),
* la couleur de fond via les méthodes ```setColorFor(Environment, Color)``` (couleur spécifique à l'environnement) et ```setDefaultColor(Color)``` (couleur par défaut).

<u>Exemple</u> d'utilisation (configuration d'un plugin) :
```
public static class MyStandalonePlugin extends StandalonePlugin {
 private final StandaloneClient standaloneClient;

 public MyStandalonePlugin(StandaloneClient standaloneClient) {
    this.standaloneClient = standaloneClient;

    DefaultDesktopPaneCustomizer customizer = 
          new DefaultDesktopPaneCustomizer();

    customizer.setColorFor(Environment.PRD, new Color(189, 167, 231));
    customizer.setColorFor(Environment.REC, new Color(208, 231, 167));
    customizer.setDefaultColor(new Color(0, 78, 152));

    customizer.setLabelFor(Environment.PRD, "PRODUCTION");
    customizer.setLabelFor(Environment.REC, "RECETTE");
    customizer.setDefaultLabel("Développement");

    customizer.setDefaultIcon(Constant.ICON_ORBIS);

    standaloneClient.getConfiguration()
                    .setDesktopPaneCustomizer(customizer);
 }

 ...

}
```