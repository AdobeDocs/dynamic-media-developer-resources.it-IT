---
description: Se il formato xml è specificato come formato di risposta, i dati di risposta vengono formattati come documento XML che può essere analizzato da qualsiasi parser XML standard.
seo-description: Se il formato xml è specificato come formato di risposta, i dati di risposta vengono formattati come documento XML che può essere analizzato da qualsiasi parser XML standard.
seo-title: Proprietà XML
solution: Experience Manager
title: Proprietà XML
topic: Scene7 Image Serving - Image Rendering API
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Proprietà XML{#xml-properties}

Se il formato xml è specificato come formato di risposta, i dati di risposta vengono formattati come documento XML che può essere analizzato da qualsiasi parser XML standard.

Un documento di risposta con proprietà tipiche ha questa struttura generale:

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

L&#39;elemento `<prop-group>` viene utilizzato come contenitore più esterno e per raggruppare le proprietà. Se un gruppo è denominato, il nome corrisponde al nome dell&#39;oggetto Java/JavaScript.

>[!NOTE]
>
>È possibile specificare la codifica dei caratteri per alcuni tipi `req=`. Fare riferimento alla descrizione del comando specifico `req=`per ulteriori dettagli.

