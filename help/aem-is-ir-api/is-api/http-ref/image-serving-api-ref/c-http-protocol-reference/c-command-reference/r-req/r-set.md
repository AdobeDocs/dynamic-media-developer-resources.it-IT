---
description: Informazioni sul set di file multimediali.
solution: Experience Manager
title: set
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: bc69f094-ff21-4dd7-9e10-daddb3de0c65
TQID: 'https://experienceleague.adobe.com/nfNdFeRk7TDhSYHdy05x6fxNKMBhTF7f11xoji13VP4'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 144
ht-degree: 0%

---

# set{#set}

Informazioni sul set di file multimediali.

req=set[,xml[, *`encoding`*]|{json[&amp;id=*`reqId`*]}]

<table id="simpletable_02C955F4EBAD4251A728F0FC68F432B5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> codifica</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> reqId</span> </p></td> 
  <td class="stentry"> <p>Identificatore di richiesta univoco </p></td> 
 </tr> 
</table>

Restituisce informazioni su immagini, video, campioni e vari metadati associati a catalog::ImageSet per la voce del catalogo immagini specificata nel percorso URL. Questa risposta è una struttura gerarchica determinata dal tipo di set fornito. Quando viene richiesto il formato &#39;xml&#39; o &#39;json&#39; viene applicata la formattazione appropriata.

La risposta HTTP è memorizzabile in cache con TTL basato su `catalog::NonImgExpiration`.

>[!NOTE]
>
>Il carattere due punti non è consentito nelle richieste req=set.

Richieste che supportano il formato di risposta JSON consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
