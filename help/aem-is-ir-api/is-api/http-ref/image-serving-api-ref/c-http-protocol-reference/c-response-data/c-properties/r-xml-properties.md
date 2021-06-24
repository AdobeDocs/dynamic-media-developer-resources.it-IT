---
description: Se il formato xml è specificato come formato di risposta, i dati di risposta vengono formattati come documento XML che può essere analizzato da qualsiasi parser XML standard.
solution: Experience Manager
title: Proprietà XML
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# Proprietà XML{#xml-properties}

Se il formato xml è specificato come formato di risposta, i dati di risposta vengono formattati come documento XML che può essere analizzato da qualsiasi parser XML standard.

Un documento di risposta delle proprietà tipiche ha questa struttura generale:

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

L’elemento `<prop-group>` viene utilizzato come contenitore più esterno e per raggruppare le proprietà. Se un gruppo è denominato, il nome corrisponde al nome dell&#39;oggetto Java/JavaScript.

>[!NOTE]
>
>È possibile specificare la codifica dei caratteri per alcuni tipi `req=`. Per ulteriori informazioni, fare riferimento alla descrizione del comando `req=`specifico.
