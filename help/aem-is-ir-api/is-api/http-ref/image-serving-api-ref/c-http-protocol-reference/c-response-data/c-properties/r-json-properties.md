---
title: Proprietà JSONP
description: Se si specifica jsonp come formato di risposta, i dati di risposta vengono formattati utilizzando JSONP (JavaScript Object Notation with Padding), racchiuso in una chiamata di funzione JavaScript.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2294eb37-b362-438f-94bc-eb24ca641752
source-git-commit: d1df6e943747f9db12c08003647aee840fdfcc0a
workflow-type: tm+mt
source-wordcount: '200'
ht-degree: 0%

---

# Proprietà JSONP{#jsonp-properties}

Se si specifica jsonp come formato di risposta, i dati di risposta vengono formattati utilizzando JSONP (JavaScript Object Notation with Padding), racchiuso in una chiamata di funzione JavaScript.

Il client può specificare un identificatore di richiesta univoco facoltativo ( *`reqId`*) restituito nella risposta e che consente al client di distinguere più risposte ricevute in modo asincrono. Una risposta tipica ha la seguente struttura generale:

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

La sintassi `<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.

Il pacchetto dei visualizzatori Image Server di Dynamic Medie include un’utility per richiedere ed analizzare i dati in formato JSONP da Image Server.

Per ulteriori informazioni sul formato JSONP, consulta [https://en.wikipedia.org/wiki/JSONP](https://en.wikipedia.org/wiki/JSONP).

Per ulteriori informazioni sul formato JSON, consulta [www.json.org](https://www.json.org/json-en.html).

Vedi anche [req](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md#reference-907cdb4a97034db7ad94695f25552e76).
