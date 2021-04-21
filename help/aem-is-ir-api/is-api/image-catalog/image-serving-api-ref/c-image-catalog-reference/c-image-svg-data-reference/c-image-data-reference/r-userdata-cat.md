---
description: Dati utente. Il server restituisce il contenuto di questo campo al client in risposta a req=userdata.
solution: Experience Manager
title: Dati utente
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 8%

---


# Dati utente{#userdata}

Dati utente. Il server restituisce il contenuto di questo campo al client in risposta a req=userdata.

## Proprietà {#section-06f2002b77d54a64be07f12fff54ad13}

Valore stringa di testo. Si consiglia di utilizzare la formattazione [dati proprietà](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md). Se la formattazione dei dati della proprietà non viene utilizzata, la stringa di testo non deve contenere il carattere &#39;=&#39;.

I client di visualizzazione dello zoom, della rotazione e della brochure presuppongono questo campo per utilizzare la formattazione dei dati delle proprietà. Questi client utilizzano questo campo per la configurazione e la personalizzazione del visualizzatore. Per ulteriori informazioni, consulta la documentazione del visualizzatore .

Questo campo partecipa alla localizzazione delle stringhe di testo. Per ulteriori informazioni, consulta [Localizzazione delle stringhe di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in *Riferimento al protocollo HTTP* .

## Predefinito {#section-7ee879762130467199745f2abc662f1e}

Nessuno.

## Consultate anche {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , localizzazione di stringhe  [di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
