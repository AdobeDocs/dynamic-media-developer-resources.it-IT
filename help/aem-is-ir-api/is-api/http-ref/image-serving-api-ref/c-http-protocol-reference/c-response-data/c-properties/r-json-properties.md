---
description: Se jsonp è specificato come formato di risposta, i dati di risposta vengono formattati utilizzando JSONP (JavaScript Object Notation with Padding), racchiuso in una chiamata di funzione JavaScript.
solution: Experience Manager
title: Proprietà JSONP
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# Proprietà JSONP{#jsonp-properties}

Se jsonp è specificato come formato di risposta, i dati di risposta vengono formattati utilizzando JSONP (JavaScript Object Notation with Padding), racchiuso in una chiamata di funzione JavaScript.

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

La funzione JavaScript `s7jsonResponse` deve essere definita dal client . Nella sua forma più semplice, la funzione potrebbe avere l&#39;aspetto seguente:

```
var responseData; 
S7jsonResponse(data, reqId) 
{ 
 responseData = eval(data); 
}
```

Le richieste che supportano il formato di risposta JSONP ti consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=` :

`req=...,json [&handler = reqHandler]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Il pacchetto Dynamic Media Image Serving Viewers include un&#39;utilità per richiedere e analizzare dati in formato JSONP da Image Serving.

Per ulteriori informazioni sul formato JSONP, consulta [http://en.wikipedia.org/wiki/JSONP](http://en.wikipedia.org/wiki/JSONP) .

Per ulteriori informazioni sul formato JSON, consulta [www.json.org](http://www.json.org) .

Vedere anche [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
