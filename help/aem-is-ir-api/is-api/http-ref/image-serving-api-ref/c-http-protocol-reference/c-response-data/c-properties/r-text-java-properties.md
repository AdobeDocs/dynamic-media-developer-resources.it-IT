---
description: Se come formato di risposta è specificato del testo, i dati di risposta sono formattati in modo da essere leggibili come proprietà Java.
solution: Experience Manager
title: Proprietà testo (Java)
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
TQID: 'https://experienceleague.adobe.com/WNIuNvCPLdbeweHB5gkcFfeZu2WDDUk53us6SHtmO-A'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
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

*`propertyValue`* potrebbe essere vuoto. Lo spazio vuoto è facoltativo all&#39;inizio e alla fine di ogni riga e prima e dopo il separatore =. È possibile utilizzare virgolette singole o doppie per racchiudere i valori stringa, ma non sono obbligatorie.

I valori stringa possono contenere caratteri di escape in stile JAVA, ad esempio `\n`, `\t`, `\:` o `\\`.
