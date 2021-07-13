---
description: Risposta all'altezza dell'immagine. Specifica la scala dell'immagine renderizzata in modo che l'altezza dell'immagine di risposta non sia maggiore del valore specificato, mantenendo le proporzioni dell'immagine.
solution: Experience Manager
title: hei
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '249'
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

L’immagine non viene imbottita se sono specificati sia `wid=` che `hei=` e larghezza/altezza è diversa dalle proporzioni dell’immagine.

`wid=` e  `hei=` collaborare per definire le dimensioni dell&#39;immagine restituita dal server. Se `scl=` segue `wid=` o `hei=` nell&#39;URL, annulla tali comandi e `scl=` definisce le dimensioni dell&#39;immagine restituita dal server.

Tuttavia, se `wid=` o `hei=` viene dopo `scl=` nell&#39;URL, annullano `scl=` e `wid=`/ `hei=` definiscono le dimensioni dell&#39;immagine restituita dal server.

>[!NOTE]
>
>Se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`, viene restituito un errore.

## Proprietà {#section-6cbc6acd37c847beab84c896ac25280c}

Può verificarsi in qualsiasi punto della richiesta. Il ridimensionamento dell&#39;immagine con `wid=`, `hei=` o `scl=` non modifica il valore della risoluzione di stampa incorporato nell&#39;immagine di risposta. Ignorato se `scl=` si verifica dopo `wid=` e/o `hei=` nella sequenza di comando.

## Predefinito {#section-61043f6c1f5d450883ff9e5eafd95955}

Se non vengono specificati né `wid=`, `hei=`, né `scl=`, l&#39;immagine di risposta viene ridimensionata in modo da adattarsi alle dimensioni definite da `attribute::DefaultPix`. Se `attribute::DefaultPix` è vuoto, l&#39;immagine di risposta ha le stesse dimensioni dell&#39;immagine di visualizzazione della vignetta.

## Consultate anche {#section-7ba51379f1e2421c92d3592d20a37734}

[attributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
