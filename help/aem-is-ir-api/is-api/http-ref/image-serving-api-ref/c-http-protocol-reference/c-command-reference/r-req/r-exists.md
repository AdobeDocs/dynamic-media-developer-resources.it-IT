---
description: L'immagine esiste.
solution: Experience Manager
title: esiste
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 810453f0-7b35-4eed-8b23-6b59a8300c50
TQID: 'https://experienceleague.adobe.com/JyGNYH5-vW7FbZbMcMk2mQFB7rrrzYd0FpvsBbI-Zi4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 126
ht-degree: 0%

---

# esiste{#exists}

L&#39;immagine esiste.

`req=exists[,text|javascript|xml|{json[&id= *`reqId`*]}]`

Identificatore di richiesta univoco *`reqId`*

Restituisce una singola proprietà denominata `catalogRecord.exists`. Il valore della proprietà è impostato su &quot;1&quot; se la voce di catalogo specificata esiste nell&#39;immagine o nel catalogo predefinito, altrimenti è impostato su &quot;0&quot;. `req=exists` richieste nel contesto `/is/content` indicano la presenza o l&#39;assenza di un record specificato nel catalogo dei contenuti statici.

Altri comandi nella stringa di richiesta vengono ignorati. La risposta HTTP è memorizzabile in cache con TTL basato su `attribute::NonImgExpiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
