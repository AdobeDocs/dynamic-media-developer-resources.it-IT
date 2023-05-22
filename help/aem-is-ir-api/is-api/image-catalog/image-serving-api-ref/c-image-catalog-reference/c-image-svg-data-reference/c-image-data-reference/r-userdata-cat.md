---
description: Dati utente. Il server restituisce il contenuto di questo campo al client in risposta a req=userdata.
solution: Experience Manager
title: DatiUtente
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 3%

---

# DatiUtente{#userdata}

Dati utente. Il server restituisce il contenuto di questo campo al client in risposta a req=userdata.

## Proprietà {#section-06f2002b77d54a64be07f12fff54ad13}

Valore stringa di testo. Si consiglia di utilizzare [dati proprietà](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) formattazione. Se non si utilizza la formattazione dei dati delle proprietà, la stringa di testo non deve contenere il carattere &quot;=&quot;.

I client di visualizzazione zoom, rotazione e brochure utilizzano questo campo per la formattazione dei dati delle proprietà. Questi client utilizzano questo campo per la configurazione e la personalizzazione dei visualizzatori. Per ulteriori informazioni, consulta la documentazione del visualizzatore.

Questo campo partecipa alla localizzazione delle stringhe di testo. Fai riferimento a [Localizzazione stringa di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) nel *Riferimento protocollo HTTP* per i dettagli.

## Predefinito {#section-7ee879762130467199745f2abc662f1e}

Nessuno.

## Consultate anche {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [Localizzazione stringa di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
