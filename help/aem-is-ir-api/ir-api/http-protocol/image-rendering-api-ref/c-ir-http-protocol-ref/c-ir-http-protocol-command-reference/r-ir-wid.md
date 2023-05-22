---
title: wid
description: Larghezza immagine di risposta. Specifica il ridimensionamento dell'immagine di cui è stato eseguito il rendering in modo che l'immagine di risposta non sia più alta del valore specificato, mantenendo le proporzioni dell'immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a77b71c3-8600-4d7a-ba52-e158cf9668eb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 2%

---

# wid{#wid}

Larghezza immagine di risposta. Specifica il ridimensionamento dell&#39;immagine di cui è stato eseguito il rendering in modo che l&#39;immagine di risposta non sia più alta del valore specificato, mantenendo le proporzioni dell&#39;immagine.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Larghezza immagine in pixel (int maggiore di 0). </p></td> 
 </tr> 
</table>

L’immagine non viene imbottita se entrambi `wid=` e `hei=` è specificato e `wid`/ `hei` è diverso dalle proporzioni dell&#39;immagine.

`wid=` e `hei=` definisci insieme le dimensioni dell&#39;immagine restituita dal server. Se `scl=` viene dopo `wid=` o `hei=` nell&#39;URL, annulla tali comandi e `scl=` definisce la dimensione dell&#39;immagine restituita dal server.

Tuttavia, se `wid=` o `hei=` viene dopo `scl=` nell’URL, annullano `scl=` e `wid=`/ `hei=` definisci le dimensioni dell&#39;immagine restituita dal server.

>[!NOTE]
>
>Viene restituito un errore se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`.

## Proprietà {#section-2d067c6d371748e19cb157684700a49d}

Può verificarsi ovunque all’interno della richiesta. Ridimensionamento dell&#39;immagine con `wid=`, `hei=`, o `scl=` non modifica il valore della risoluzione di stampa incorporato nell&#39;immagine di risposta. Ignorato se `scl=` si verifica dopo `wid=` o `hei=` nella sequenza di comando.

## Predefinito {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Se `wid=`, `hei=`, o `scl=` non sono specificati, l&#39;immagine di risposta viene ridimensionata in base alle dimensioni definite da `attribute::DefaultPix`. Se `attribute::DefaultPix` è vuoto, l’immagine di risposta ha le stesse dimensioni dell’immagine di visualizzazione della vignettatura.

## Consultate anche {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
