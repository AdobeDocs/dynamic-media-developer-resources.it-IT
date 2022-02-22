---
title: mappa lucida
description: Immagine mappa Gloss. Consente il controllo pixel per pixel della lucidità di una texture, carta da parati/bordo o decal ripetibili.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 922fc527-be19-4d7a-b265-7bdb1de80990
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 3%

---

# mappa lucida {#glossmap}

Immagine mappa Gloss. Consente il controllo pixel per pixel della lucidità di una texture, carta da parati/bordo o decal ripetibili.

`glossmap={ *`glossMapFile`*| *`embeddedReq`*}`

<table id="simpletable_6AFC3DEB61D647339525C7CFFA052608"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> embeddedReq</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">&amp;parentesi graffa;'is&amp;lbrace;'<span class="varname"> isReq</span>&amp;parentesi graffa;'&amp;race;|&amp;lparentesi graffa;'&amp;lbrace;'<span class="varname"> foreignReq</span>&amp;parentesi graffa;' </span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> glossMapFile</span> </span> </p></td> 
  <td class="stentry"> <p>Gloss map image file (scala di grigi). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> isReq</span> </span> </p></td> 
  <td class="stentry"> <p>Richiedi a Image Server. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> foreignReq </span> </span> </p></td> 
  <td class="stentry"> <p>Richiedi a un server esterno. </p></td> 
 </tr> 
</table>

Applicabile a materiali quali effetti di vernice metallica, sfondi e bordi di lamiera tagliata e tessuti metallici.

L&#39;immagine della mappa lucida deve essere in scala di grigi a 8 bit e avere le stesse dimensioni dell&#39;immagine primaria specificata con `src=`. Fai riferimento alla descrizione di [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) per ulteriori informazioni.

## Proprietà {#section-26375672d69849be9b026cc93c3bc558}

Attributo materiale. Supportato da texture ripetibili, sfondi e bordi e decalcomanie. Ignorati da materiali di rivestimento in tinta unita, armadio e finestre. Vedi [ `gloss=`](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca) per ulteriori informazioni.

## Predefinito {#section-d9ac031fb2f94482ac3fe2283d7cb168}

Nessuno.

## Consultate anche {#section-33953fc1be82452da37141f2e541e00c}

[gloss=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-gloss.md#reference-325aef2ee51e4e1584a06047427340ca), [src=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272)
