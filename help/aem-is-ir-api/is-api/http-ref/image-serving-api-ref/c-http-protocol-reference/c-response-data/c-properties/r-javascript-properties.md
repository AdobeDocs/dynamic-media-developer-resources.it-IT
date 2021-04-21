---
description: Se JavaScript™ è specificato come formato di risposta, i dati di risposta vengono formattati per essere analizzati come file di inclusione JavaScript™.
solution: Experience Manager
title: Proprietà JavaScript™
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---


# Proprietà JavaScript™{#javascript-properties}

Se JavaScript™ è specificato come formato di risposta, i dati di risposta vengono formattati per essere analizzati come file di inclusione JavaScript™.

La tipica risposta alle proprietà JavaScript™ presenta questa struttura generale:

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

Per analizzare una risposta alle proprietà JavaScript™, è necessario creare qualsiasi oggetto o oggetto a cui si fa riferimento nella risposta prima del caricamento del file delle proprietà. Di seguito è riportato un esempio per utilizzare `req=props` per ottenere la dimensione dell&#39;immagine di risposta in JavaScript™:

```
<script> image = new Object; </script> 
<script 
src='http://myServer/is/image/myImage?req=props,javascript'> 
<script> alert("Size: " + image.width + " , " + 
image.height); </script>
```

