---
description: Dati set immagini da catalogo immagini. Restituisce i dati del set di immagini per la voce del catalogo immagini specificata nel percorso URL.
solution: Experience Manager
title: imageset
feature: Dynamic Media Classic,SDK/API,Image Sets
role: Developer,User
exl-id: 730e7db9-47f0-4e96-8948-18b8185a5b7a
TQID: 'https://experienceleague.adobe.com/1PbZjs--lk7GcyXU1F-AJ-vWcgwVX9JFivvbnTGrWKQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 169
ht-degree: 0%

---

# imageset{#imageset}

Dati set immagini da catalogo immagini. Restituisce i dati del set di immagini per la voce del catalogo immagini specificata nel percorso URL.

`req=imageset[,text|javascript|{xml[, *`codifica`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_86FF9E59B11D4C408F0D932D46CC2F8E"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> codifica</span></span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> requestId</span></span> </p></td> 
  <td class="stentry"> <p>Identificatore di richiesta univoco. </p></td> 
 </tr> 
</table>

Il contenuto di `catalog::ImageSet` viene restituito senza ulteriori modifiche (ad eccezione della localizzazione delle stringhe, se applicabile), seguita da un terminatore a riga singola (CR/LF). Se il percorso URL non viene risolto in una voce di catalogo valida, la risposta è costituita solo da un terminatore a riga singola.

Altri comandi nella stringa di richiesta vengono ignorati. La risposta HTTP è memorizzabile in cache con TTL basato su `catalog::NonImgExpiration`.

Richieste che supportano il formato di risposta JSONP consentono di specificare il nome del gestore di callback JS utilizzando la sintassi estesa del parametro `req=`:

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` è il nome del gestore JS presente nella risposta JSONP. Sono consentiti solo i caratteri a-z, A-Z e 0-9. Facoltativo. Il valore predefinito è `s7jsonResponse`.
