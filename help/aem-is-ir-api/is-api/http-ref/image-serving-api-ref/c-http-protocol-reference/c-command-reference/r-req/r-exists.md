---
description: L'immagine esiste.
solution: Experience Manager
title: esiste
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '121'
ht-degree: 10%

---

# esiste{#exists}

L&#39;immagine esiste.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

*`reqId`* identificatore di richiesta univoco

Restituisce una singola proprietà denominata `catalogRecord.exists`. Il valore della proprietà è impostato su &quot;1&quot; se la voce di catalogo specificata esiste nell&#39;immagine o nel catalogo predefinito, altrimenti è impostato su &quot;0&quot;. `req=exists` richieste contro `/is/content` context (contesto) indica la presenza o l&#39;assenza di un record specificato nel catalogo dei contenuti statici.

Altri comandi nella stringa di richiesta vengono ignorati. La risposta HTTP può essere memorizzata nella cache con TTL basato su `attribute::NonImgExpiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa di `req=` parametro:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
