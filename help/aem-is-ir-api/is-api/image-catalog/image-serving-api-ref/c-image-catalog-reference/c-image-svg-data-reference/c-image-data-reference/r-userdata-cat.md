---
description: Dati utente. Il server restituisce il contenuto di questo campo al client in risposta a req=userdata.
seo-description: Dati utente. Il server restituisce il contenuto di questo campo al client in risposta a req=userdata.
seo-title: Dati utente
solution: Experience Manager
title: Dati utente
topic: Scene7 Image Serving - Image Rendering API
uuid: cadc9f3c-c0ca-4c88-bc8a-97c28b439b01
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Dati utente{#userdata}

Dati utente. Il server restituisce il contenuto di questo campo al client in risposta a req=userdata.

## Proprietà {#section-06f2002b77d54a64be07f12fff54ad13}

Valore stringa di testo. Si consiglia di utilizzare la formattazione dei dati [delle](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) proprietà. Se la formattazione dei dati delle proprietà non è utilizzata, la stringa di testo non deve contenere il carattere &quot;=&quot;.

I client per visualizzatori zoom, 360 gradi e brochure utilizzano la formattazione dei dati delle proprietà. Questi client utilizzano questo campo per la configurazione e la personalizzazione del visualizzatore. Per informazioni dettagliate, consultate la documentazione del visualizzatore.

Questo campo partecipa alla localizzazione delle stringhe di testo. Per ulteriori informazioni, vedere Localizzazione [delle stringhe di](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) testo nella Guida di riferimento *del protocollo* HTTP.

## Predefinito {#section-7ee879762130467199745f2abc662f1e}

Nessuno.

## Consultate anche {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , Localizzazione Stringa [di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
