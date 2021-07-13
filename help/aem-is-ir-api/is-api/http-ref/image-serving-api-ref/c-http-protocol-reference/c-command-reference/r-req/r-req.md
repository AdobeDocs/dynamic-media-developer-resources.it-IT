---
description: Tipo di richiesta. Specifica il tipo di richiesta.
solution: Experience Manager
title: req
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 546b8b3f-9e37-4e8d-bf0c-db8c12696b2b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 1%

---

# req{#req}

Tipo di richiesta. Specifica il tipo di richiesta.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`di nitidezza`*]`

* [catalogprops](r-catalogprops.md)
* [esiste](r-exists.md)
* [imageprops](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [map](r-map-req.md)
* [maschera](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [message](r-message.md)
* [proprietà](r-props.md)
* [risolvere](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [set](r-set.md)
* [target](r-targets.md)
* [tam](r-tmb.md)
* [dati utente](r-userdata.md)
* [validate](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

Se non diversamente indicato nelle descrizioni dettagliate, il server restituisce `text` risposte con tipo MIME `text/plain`. Molti tipi di richiesta consentono di specificare un tipo di risposta, ad esempio `text`, tipicamente predefinito, `javascript`, `xml` o `json`. I tipi MIME di risposta associati sono rispettivamente `text/plain`, `text/javascript`, `text/xml` e `text/javascript`.

Se non diversamente indicato, le risposte formattano la risposta come un set di coppie `name=value`.

Vedere [Proprietà](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
