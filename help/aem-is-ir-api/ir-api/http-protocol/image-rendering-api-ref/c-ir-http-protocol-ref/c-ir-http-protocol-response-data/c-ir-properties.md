---
description: I dati delle proprietà vengono restituiti in risposta ai seguenti tipi req= imageprop e prop.
seo-description: I dati delle proprietà vengono restituiti in risposta ai seguenti tipi req= imageprop e prop.
seo-title: Proprietà
solution: Experience Manager
title: Proprietà
topic: Scene7 Image Serving - Image Rendering API
uuid: b4e1de52-db0a-43dc-aefe-26e8f5020e79
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 5%

---


# Proprietà{#properties}

I dati delle proprietà vengono restituiti in risposta ai seguenti tipi req=: imageprop e prop.

I dati di risposta sono formattati per essere leggibili come proprietà Java. Una tipica risposta delle proprietà di testo ha questa struttura generale:

`#S7Z OK`

`# *[!DNL timeStamp]*`

` *[!DNL objectName.propertyName]*= *[!DNL propertyValue]*`

...

` *[!DNL propertyValue]*` può essere vuoto. Lo spazio vuoto è facoltativo all&#39;inizio e alla fine di ogni riga e prima e dopo il separatore &#39;=&#39;. Le virgolette singole o doppie possono essere utilizzate per racchiudere i valori stringa, ma non sono obbligatorie.

I valori stringa possono contenere caratteri di escape stile JAVA, ad esempio `\n`, `\t`, `\:`. Oppure `\\`.

**Consultate anche**

[req=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-req.md#reference-792b1a663fb64261bd2de2a209b847fb)
