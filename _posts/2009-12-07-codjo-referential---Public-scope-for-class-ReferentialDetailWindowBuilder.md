---
layout: post
title: agf-referential - Public scope for class ReferentialDetailWindowBuilder
tags: [framework-1-125,codjo-referential]
---
<u>Context</u>:

In Oscar, we need to get direct access to the detail gui, and thus bypass the referential main GUI.

<u>Description:</u>

The class ```ReferentialDetailWindowBuilder``` has now a public scope&nbsp;which allows building the detail frame.

<u>Example</u> :&nbsp;
``` public JInternalFrame buildFrame() {
            ReferentialGuiConfiguration guiConfiguration = referentialGuiPlugin.getConfiguration();
            ReferentialMapping referentialMapping = guiConfiguration.getReferentialMapping();
            Referential referential= referentialMapping.getReferentialsByPreferenceId().get(getPreferenceId());
            ReferentialDetailWindowBuilder builder = new ReferentialDetailWindowBuilder(null, frameName, referential);
            ..
            return builder.buildFrame(detailDataSource, preference);
    }
```see : [[codjo-referential - Utilisation|http://wp-confluence/confluence/display/framework/Utilisation<u>de</u>agf-referential|Utilisation de agf-referential]]