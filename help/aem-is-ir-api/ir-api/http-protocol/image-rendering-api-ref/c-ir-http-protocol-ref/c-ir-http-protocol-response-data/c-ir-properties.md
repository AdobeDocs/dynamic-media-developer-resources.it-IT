---
title: Proprietà
description: I dati delle proprietà vengono restituiti in risposta ai seguenti req= tipi imageprop e prop.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a27ec5e4-7499-44ac-8db1-bf5d67f59632
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 2%

---

# Proprietà{#properties}

I dati delle proprietà vengono restituiti in risposta ai seguenti tipi req=: imageprops e props.

I dati di risposta sono formattati per essere leggibili come proprietà Java™. Una tipica risposta delle proprietà di testo ha la seguente struttura generale:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` Può essere vuoto. Lo spazio vuoto è facoltativo all&#39;inizio e alla fine di ogni riga e prima e dopo il separatore &#39;=&#39;. È possibile utilizzare virgolette singole o doppie per racchiudere i valori stringa, ma non sono obbligatorie.

I valori stringa possono contenere caratteri di escape in stile JAVA, ad esempio `\n`, `\t`, `\:`, o `\\`.

**Consultate anche**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
