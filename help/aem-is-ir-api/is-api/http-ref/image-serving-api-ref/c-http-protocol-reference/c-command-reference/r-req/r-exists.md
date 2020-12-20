---
description: L'immagine esiste.
seo-description: L'immagine esiste.
seo-title: exists
solution: Experience Manager
title: exists
topic: Scene7 Image Serving - Image Rendering API
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 10%

---


# exists{#exists}

L&#39;immagine esiste.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* identificativo univoco della richiesta

Restituisce una singola proprietà denominata `catalogRecord.exists`. Il valore della proprietà è impostato su &quot;1&quot; se la voce di catalogo specificata esiste nel catalogo predefinito o dell&#39;immagine, altrimenti è impostata su &quot;0&quot;. `req=exists` le richieste contestuali indicano la presenza o l&#39;assenza di un record specificato nel catalogo del contenuto statico.  `/is/content` 

Altri comandi nella stringa di richiesta vengono ignorati. La risposta HTTP può essere memorizzata nella cache con TTL basato su `attribute::NonImgExpiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
