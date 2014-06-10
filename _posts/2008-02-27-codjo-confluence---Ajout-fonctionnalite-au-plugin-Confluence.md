---
layout: post
title: agf-confluence - Ajout fonctionnalité au plugin Confluence
tags: [framework-1-33,codjo-confluence]
---
Ajout des opérations suivantes:

```
- Page getPage(String spaceKey, String pageTitle)
- Page createPage(String spaceKey, String parentId, String title, Map<String, String> metadata, String content)
- void updatePage(Page page)
- void updatePageContent(Page page, Map<String, String> metadata, String content)
```

```
- void attachFile(File file, String pageId)
- void attachFile(File file, String pageId, String newName)
```

```
- List<Page> getPagesByLabel(String spaceKey, String label)  // en remplacement de searchByLabel
- List<Page> searchPagesByMetadata(String spaceKey, Map<String, String> metadata, int maxResults)
```