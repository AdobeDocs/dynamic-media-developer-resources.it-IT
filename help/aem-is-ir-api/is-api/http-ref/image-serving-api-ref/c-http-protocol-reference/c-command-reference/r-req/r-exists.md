---
description: L'immagine esiste.
seo-description: L'immagine esiste.
seo-title: esiste
solution: Experience Manager
title: esiste
uuid: 5490e4c7-b52a-4b2e-b002-34afaa242c08
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 9%

---


# exists{#exists}

L&#39;immagine esiste.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* identificatore di richiesta univoco

Restituisce una singola proprietà denominata `catalogRecord.exists`. Il valore della proprietà è impostato su &quot;1&quot; se la voce di catalogo specificata esiste nell&#39;immagine o nel catalogo predefinito, altrimenti è impostata su &quot;0&quot;. `req=exists` le richieste in base al  `/is/content` contesto indicano la presenza o l&#39;assenza di un record specificato nel catalogo dei contenuti statici.

Altri comandi nella stringa di richiesta vengono ignorati. La risposta HTTP può essere memorizzata nella cache con TTL basato su `attribute::NonImgExpiration`.

Le richieste che supportano il formato di risposta JSONP ti consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=` :

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
