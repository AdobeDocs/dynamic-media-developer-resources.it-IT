---
description: Dati utente. Il server restituisce il contenuto di questo campo al client in risposta a req=userdata.
solution: Experience Manager
title: DatiUtente
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4994c91c-52d7-473d-88ee-f136c4193c40
TQID: 'https://experienceleague.adobe.com/9jhCw--mmCQ1-j1uNGFmfTEcnkNzxbKfXJtve5GugdA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 123
ht-degree: 2%

---

# DatiUtente{#userdata}

Dati utente. Il server restituisce il contenuto di questo campo al client in risposta a req=userdata.

## Proprietà {#section-06f2002b77d54a64be07f12fff54ad13}

Valore stringa di testo. Si consiglia di utilizzare la formattazione [dati proprietà](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md). Se non si utilizza la formattazione dei dati delle proprietà, la stringa di testo non deve contenere il carattere &quot;=&quot;.

I client di visualizzazione zoom, rotazione e brochure utilizzano questo campo per la formattazione dei dati delle proprietà. Questi client utilizzano questo campo per la configurazione e la personalizzazione dei visualizzatori. Per ulteriori informazioni, consulta la documentazione del visualizzatore.

Questo campo partecipa alla localizzazione delle stringhe di testo. Per ulteriori informazioni, consultare [Text String Localization](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) nella *documentazione sul protocollo HTTP*.

## Predefinito {#section-7ee879762130467199745f2abc662f1e}

Nessuno.

## Consultate anche {#section-e07a022933b2461d9c37b1f188aa8fb5}

[req=userdata](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md) , [Localizzazione stringa di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
