---
description: Se come formato di risposta è specificato javascript, i dati di risposta vengono formattati per essere analizzati come file di inclusione JavaScript.
seo-description: Se come formato di risposta è specificato javascript, i dati di risposta vengono formattati per essere analizzati come file di inclusione JavaScript.
seo-title: Proprietà JavaScript
solution: Experience Manager
title: Proprietà JavaScript
uuid: 832a927e-ecaf-438c-8fbf-a702d58902d8
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---


# Proprietà JavaScript{#javascript-properties}

Se come formato di risposta è specificato javascript, i dati di risposta vengono formattati per essere analizzati come file di inclusione JavaScript.

Una tipica risposta di proprietà JavaScript presenta questa struttura generale:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* può essere vuoto. Lo spazio vuoto è facoltativo all’inizio e alla fine di ogni riga e prima e dopo il separatore = . Tutti i valori sono racchiusi tra virgolette singole. Le virgolette singole nelle stringhe vengono precedute da due virgolette singole consecutive.

Per analizzare una risposta delle proprietà JavaScript, è necessario creare qualsiasi oggetto o oggetti a cui si fa riferimento nella risposta prima che il file delle proprietà venga caricato. Di seguito è riportato un esempio per utilizzare `req=props` per ottenere la dimensione dell&#39;immagine di risposta in JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

