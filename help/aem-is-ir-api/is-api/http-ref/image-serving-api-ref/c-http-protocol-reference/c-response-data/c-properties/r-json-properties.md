---
description: Se jsonp è specificato come formato di risposta, i dati di risposta vengono formattati utilizzando JSONP (JavaScript Object Notation with Padding), racchiuso in una chiamata alla funzione JavaScript.
seo-description: Se jsonp è specificato come formato di risposta, i dati di risposta vengono formattati utilizzando JSONP (JavaScript Object Notation with Padding), racchiuso in una chiamata alla funzione JavaScript.
seo-title: Proprietà JSONP
solution: Experience Manager
title: Proprietà JSONP
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e53d75f2-9b43-4e8f-8191-66f69f344cdd
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 1%

---


# Proprietà JSONP{#jsonp-properties}

Se jsonp è specificato come formato di risposta, i dati di risposta vengono formattati utilizzando JSONP (JavaScript Object Notation with Padding), racchiuso in una chiamata alla funzione JavaScript.

Il client può specificare un identificatore di richiesta univoco opzionale ( *`reqId`*), restituito nella risposta e che consente al client di distinguere più risposte ricevute in modo asincrono. Una risposta tipica ha la seguente struttura generale:

```
/*jsonp*/s7jsonResponse({ 
   " 
<varname>
  objectName 
</varname>. 
<varname>
  propertyName 
</varname>" : " 
<varname>
  propertyValue 
</varname>", 
   ... 
 }, " 
<varname>
  reqId 
</varname>" );
```

La funzione JavaScript `s7jsonResponse` deve essere definita dal client. Nella sua forma più semplice, la funzione potrebbe essere simile alla seguente:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Il pacchetto Dynamic Media Image Serving Viewers include un’utility per richiedere e analizzare i dati in formato JSONP da Image Server.

Per ulteriori informazioni sul formato JSONP, vedere [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP).

Per ulteriori informazioni sul formato JSON, consultate [www.json.org](http://www.json.org).

Vedere anche [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
