---
description: Se il testo è specificato come formato di risposta, i dati di risposta vengono formattati in modo da essere leggibili come proprietà Java.
seo-description: Se il testo è specificato come formato di risposta, i dati di risposta vengono formattati in modo da essere leggibili come proprietà Java.
seo-title: Proprietà testo (Java)
solution: Experience Manager
title: Proprietà testo (Java)
uuid: 5dba4cf7-9172-4195-968e-9ef76c25e90c
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 0%

---


# Proprietà testo (Java){#text-java-properties}

Se il testo è specificato come formato di risposta, i dati di risposta vengono formattati in modo da essere leggibili come proprietà Java.

Una risposta tipica delle proprietà di testo ha questa struttura generale:

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

*`propertyValue`* può essere vuoto. Lo spazio vuoto è facoltativo all’inizio e alla fine di ogni riga e prima e dopo il separatore = . Le virgolette singole o doppie possono essere utilizzate per racchiudere i valori stringa, ma non sono obbligatorie.

I valori stringa possono contenere caratteri di escape in stile JAVA, ad esempio `\n`, `\t`, `\:` o `\\`.
