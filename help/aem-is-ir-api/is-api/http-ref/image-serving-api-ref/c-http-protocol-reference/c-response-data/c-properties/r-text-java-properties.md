---
description: Se il testo è specificato come formato di risposta, i dati di risposta sono formattati in modo da essere leggibili come proprietà Java.
seo-description: Se il testo è specificato come formato di risposta, i dati di risposta sono formattati in modo da essere leggibili come proprietà Java.
seo-title: Proprietà testo (Java)
solution: Experience Manager
title: Proprietà testo (Java)
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 0%

---


# Proprietà testo (Java){#text-java-properties}

Se il testo è specificato come formato di risposta, i dati di risposta sono formattati in modo da essere leggibili come proprietà Java.

Una tipica risposta delle proprietà di testo ha questa struttura generale:

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`* può essere vuoto. Lo spazio vuoto è facoltativo all&#39;inizio e alla fine di ogni riga e prima e dopo il separatore =. Le virgolette singole o doppie possono essere utilizzate per racchiudere i valori stringa, ma non sono obbligatorie.

I valori stringa possono contenere caratteri di escape stile JAVA, ad esempio `\n`, `\t`, `\:` o `\\`.
