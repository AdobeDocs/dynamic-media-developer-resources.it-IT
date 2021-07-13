---
description: Se il testo è specificato come formato di risposta, i dati di risposta vengono formattati in modo da essere leggibili come proprietà Java.
solution: Experience Manager
title: Proprietà testo (Java)
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '104'
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
