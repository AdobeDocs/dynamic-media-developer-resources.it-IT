---
title: hei
description: Risposta all'altezza dell'immagine. Specifica la scala dell'immagine renderizzata in modo che l'altezza dell'immagine di risposta non sia maggiore del valore specificato, mantenendo le proporzioni dell'immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 2%

---

# hei{#hei}

Risposta all&#39;altezza dell&#39;immagine. Specifica la scala dell&#39;immagine renderizzata in modo che l&#39;altezza dell&#39;immagine di risposta non sia maggiore del valore specificato, mantenendo le proporzioni dell&#39;immagine.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Reply image height in pixel (numero intero maggiore di 0). </p></td> 
 </tr> 
</table>

L’immagine non viene imbottita se entrambe `wid=` e `hei=` sono specificati e larghezza/altezza è diversa dalle proporzioni dell&#39;immagine.

`wid=` e `hei=` lavorare insieme per definire le dimensioni dell&#39;immagine restituita dal server. Se `scl=` viene dopo `wid=` o `hei=` nell’URL, annulla tali comandi e `scl=` definisce le dimensioni dell&#39;immagine restituita dal server.

Tuttavia, se `wid=` o `hei=` viene dopo `scl=` nell’URL, annullano `scl=` e `wid=`/ `hei=` definire le dimensioni dell&#39;immagine restituita dal server.

>[!NOTE]
>
>Se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`.

## Proprietà {#section-6cbc6acd37c847beab84c896ac25280c}

Può verificarsi in qualsiasi punto della richiesta. Ridimensionamento dell’immagine con `wid=`, `hei=`oppure `scl=` non modifica il valore della risoluzione di stampa incorporato nell&#39;immagine di risposta. Ignorato se `scl=` si verifica dopo `wid=` e/o `hei=` nella sequenza di comando.

## Predefinito {#section-61043f6c1f5d450883ff9e5eafd95955}

Se `wid=`, `hei=`oppure `scl=` non sono specificati, l&#39;immagine di risposta viene ridimensionata per adattarsi alle dimensioni definite da `attribute::DefaultPix`. Se `attribute::DefaultPix` è vuoto, l&#39;immagine di risposta ha le stesse dimensioni dell&#39;immagine di visualizzazione della vignetta.

## Consultate anche {#section-7ba51379f1e2421c92d3592d20a37734}

[attributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
