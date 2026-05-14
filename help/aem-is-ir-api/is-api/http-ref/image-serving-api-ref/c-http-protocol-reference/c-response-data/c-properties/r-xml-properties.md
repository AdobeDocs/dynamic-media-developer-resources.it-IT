---
description: Se xml è specificato come formato di risposta, i dati di risposta vengono formattati come documento XML che può essere analizzato da qualsiasi parser XML standard.
solution: Experience Manager
title: Proprietà XML
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
TQID: 'https://experienceleague.adobe.com/Nljy83DDIbeY6l-d6F02NlaFzyCFJny7iesxnF9mFyo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 109
ht-degree: 0%

---

# Proprietà XML{#xml-properties}

Se xml è specificato come formato di risposta, i dati di risposta vengono formattati come documento XML che può essere analizzato da qualsiasi parser XML standard.

Un tipico documento di risposta sulle proprietà ha la seguente struttura generale:

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
>È possibile specificare la codifica dei caratteri per alcuni tipi `req=`. Per ulteriori informazioni, consultare la descrizione del comando `req=` specifico.
