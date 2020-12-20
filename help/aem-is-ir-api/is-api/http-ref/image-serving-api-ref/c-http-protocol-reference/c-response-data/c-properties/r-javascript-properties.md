---
description: Se come formato di risposta è specificato javascript, i dati di risposta vengono formattati in modo da essere analizzati come file di inclusione JavaScript.
seo-description: Se come formato di risposta è specificato javascript, i dati di risposta vengono formattati in modo da essere analizzati come file di inclusione JavaScript.
seo-title: Proprietà JavaScript
solution: Experience Manager
title: Proprietà JavaScript
topic: Scene7 Image Serving - Image Rendering API
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 0%

---


# Proprietà JavaScript{#javascript-properties}

Se come formato di risposta è specificato javascript, i dati di risposta vengono formattati in modo da essere analizzati come file di inclusione JavaScript.

Una tipica risposta alle proprietà JavaScript ha questa struttura generale:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* può essere vuoto. Lo spazio vuoto è facoltativo all&#39;inizio e alla fine di ogni riga e prima e dopo il separatore =. Tutti i valori sono racchiusi tra virgolette singole. Le virgolette singole nelle stringhe vengono precedute da due virgolette singole consecutive.

Per analizzare la risposta relativa alle proprietà JavaScript, è necessario creare qualsiasi oggetto a cui si fa riferimento nella risposta prima del caricamento del file delle proprietà. Di seguito è riportato un esempio per utilizzare `req=props` per ottenere le dimensioni dell&#39;immagine di risposta in JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

