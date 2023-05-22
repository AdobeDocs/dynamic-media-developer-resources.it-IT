---
description: Se come formato di risposta è specificato del testo, i dati di risposta sono formattati in modo da essere leggibili come proprietà Java.
solution: Experience Manager
title: Proprietà testo (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 0%

---

# Proprietà testo (Java){#text-java-properties}

Se come formato di risposta è specificato del testo, i dati di risposta sono formattati in modo da essere leggibili come proprietà Java.

Una tipica risposta delle proprietà di testo ha la seguente struttura generale:

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

*`propertyValue`* può essere vuoto. Lo spazio vuoto è facoltativo all&#39;inizio e alla fine di ogni riga e prima e dopo il separatore =. È possibile utilizzare virgolette singole o doppie per racchiudere i valori stringa, ma non sono obbligatorie.

I valori stringa possono contenere caratteri di escape in stile JAVA, ad esempio `\n`, `\t`, `\:`, o `\\`.
