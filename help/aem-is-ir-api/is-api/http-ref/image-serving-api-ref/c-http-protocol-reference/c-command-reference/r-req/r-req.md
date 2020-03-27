---
description: Tipo di richiesta. Specifica il tipo di richiesta.
seo-description: Tipo di richiesta. Specifica il tipo di richiesta.
seo-title: req
solution: Experience Manager
title: req
topic: Scene7 Image Serving - Image Rendering API
uuid: b888be10-89e5-4b41-a2bd-f83533ea2481
translation-type: tm+mt
source-git-commit: 94a26628ec619076f0942e9278165cc591f1c150

---


# req{#req}

Tipo di richiesta. Specifica il tipo di richiesta.

`req={catalogprops|exists|imageprops|imageset|img|loadcache|map|mask|mbrSet|message|props|resolve|saveToFile|set|targets|tmb|userdata|validate|xlate|xmp}[, *`di nitidezza`*]`

* [catalogprops](r-catalogprops.md)
* [exists](r-exists.md)
* [imageprop](r-imageprops.md)
* [imageset](r-imageset-req.md)
* [img](r-img.md)
* [loadcache](r-loadcache.md)
* [map](r-map-req.md)
* [mask](r-mask-req.md)
* [mbrSet](r-mbrset.md)
* [message](r-message.md)
* [prop](r-props.md)
* [resolve](r-resolve.md)
* [saveToFile](r-savetofile.md)
* [set](r-set.md)
* [target](r-targets.md)
* [tmb](r-tmb.md)
* [userdata](r-userdata.md)
* [validate](r-is-http-validate.md)
* [xlate](r-xlate.md)
* [xmp](r-xmp.md)

Salvo diversa indicazione nelle descrizioni dettagliate, il server restituirà `text` le risposte con tipo MIME `text/plain`. Molti tipi di richiesta consentono di specificare un tipo di risposta, ad esempio `text`, tipicamente quello predefinito, `javascript`, `xml`o `json`. I tipi MIME di risposta associati sono `text/plain`, `text/javascript`, `text/xml`e `text/javascript`, rispettivamente.

Salvo diversa indicazione, le risposte formattano la risposta come un insieme di `name=value` coppie.

Consultate [Proprietà](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-response-data/c-properties/c-properties.md#concept-49c609fd6de942cab422ee412353c9d9).
