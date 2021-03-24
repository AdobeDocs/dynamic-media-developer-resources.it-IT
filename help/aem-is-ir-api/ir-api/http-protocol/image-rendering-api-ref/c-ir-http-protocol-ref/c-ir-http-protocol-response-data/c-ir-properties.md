---
description: I dati della proprietà vengono restituiti in risposta ai seguenti req= types imageprops e prop.
solution: Experience Manager
title: Proprietà
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 4%

---


# Proprietà{#properties}

I dati della proprietà vengono restituiti in risposta ai seguenti tipi req=: immagini e proprietà.

I dati di risposta vengono formattati in modo da essere leggibili come proprietà Java. Una risposta tipica delle proprietà di testo ha questa struttura generale:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` può essere vuoto. Lo spazio vuoto è facoltativo all&#39;inizio e alla fine di ogni riga e prima e dopo il separatore &#39;=&#39;. Le virgolette singole o doppie possono essere utilizzate per racchiudere i valori stringa, ma non sono obbligatorie.

I valori stringa possono contenere caratteri di escape in stile JAVA, ad esempio `\n`, `\t`, `\:`. Oppure `\\`.

**Consultate anche**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
