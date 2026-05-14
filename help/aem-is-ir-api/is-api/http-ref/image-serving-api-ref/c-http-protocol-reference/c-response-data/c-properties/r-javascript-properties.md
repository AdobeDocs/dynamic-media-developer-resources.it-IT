---
title: Proprietà JavaScript
description: Se JavaScript è specificato come formato di risposta, i dati di risposta vengono formattati in modo che vengano analizzati come file JavaScript&trade; include.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 12e69221-4a2c-4ec6-b38b-0a8d98d3c4a6
TQID: 'https://experienceleague.adobe.com/T6xqUHtT9XX4b9bP-wi-b0dDBe2LHE3vcBcJI6cMKqE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
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
