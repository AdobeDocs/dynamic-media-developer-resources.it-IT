---
description: Se il testo è specificato come formato di risposta, i dati di risposta vengono formattati in modo da essere leggibili come proprietà Java.
solution: Experience Manager
title: Proprietà testo (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '107'
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
