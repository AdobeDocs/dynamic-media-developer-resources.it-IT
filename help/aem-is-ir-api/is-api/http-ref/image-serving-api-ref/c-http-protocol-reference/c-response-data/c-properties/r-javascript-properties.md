---
title: Proprietà JavaScript
description: Se JavaScript è specificato come formato di risposta, i dati di risposta vengono formattati in modo che vengano analizzati come file JavaScript&trade; include.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Proprietà JavaScript{#javascript-properties}

Se JavaScript è specificato come formato di risposta, i dati di risposta vengono formattati in modo da essere analizzati come file di inclusione di JavaScript.

Una tipica risposta delle proprietà di JavaScript ha la seguente struttura generale:

```
           
<varname> 
 objectName.propertyName 
</varname>=' 
<varname>
  propertyValue 
</varname>' 
...
```

*`propertyValue`* può essere vuoto. Lo spazio vuoto è facoltativo all&#39;inizio e alla fine di ogni riga e prima e dopo il separatore =. Tutti i valori sono racchiusi tra virgolette singole. Le virgolette singole nelle stringhe sono precedute da due apici singoli consecutivi.

Per analizzare una risposta delle proprietà di JavaScript, è necessario creare uno o più oggetti a cui si fa riferimento nella risposta prima di caricare il file delle proprietà. Di seguito è riportato un esempio di utilizzo di `req=props` per ottenere le dimensioni dell&#39;immagine di risposta in JavaScript:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```
