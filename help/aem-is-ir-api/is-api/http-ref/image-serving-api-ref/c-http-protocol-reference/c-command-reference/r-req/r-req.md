---
description: Tipo di richiesta. Specifica il tipo di richiesta.
solution: Experience Manager
title: req
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
TQID: 'https://experienceleague.adobe.com/-WzHmELeamQBbVFlzXNKbDE3fKVXw4x6pSoEz0LHav4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 90
ht-degree: 0%

---

# req{#req}

Tipo di richiesta. Specifica il tipo di richiesta.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`opzioni`*]`

* [catalogprops](r-catalogprops.md)
* [esiste](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [mappa](r-map-req.md)
* [maschera](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [messaggio](r-message.md)
* [prop](r-props.md)
* [risolvere](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [set](r-set.md)
* [target](r-targets.md)
* [tmb](r-tmb.md)
* [userdata](r-userdata.md)
* [convalida](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

Se non diversamente specificato nelle descrizioni dettagliate, il server restituisce `text` risposte con tipo MIME `text/plain`. Molti tipi di richiesta consentono di specificare un tipo di risposta, ad esempio `text` che è in genere il valore predefinito, `javascript`, `xml` o `json`. I tipi MIME di risposta associati sono rispettivamente `text/plain`, `text/javascript`, `text/xml` e `text/javascript`.

Se non diversamente specificato, le risposte formattano la risposta come un set di `name=value` coppie.

Vedi [Proprietà](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
