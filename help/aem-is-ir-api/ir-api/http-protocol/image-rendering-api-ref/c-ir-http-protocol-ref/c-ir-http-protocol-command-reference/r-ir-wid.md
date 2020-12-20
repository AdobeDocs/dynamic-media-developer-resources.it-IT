---
description: Rispondi alla larghezza dell’immagine. Specifica il ridimensionamento dell'immagine di cui è stato effettuato il rendering in modo che l'immagine di risposta non sia più alta del valore specificato, mantenendo le proporzioni dell'immagine.
seo-description: Rispondi alla larghezza dell’immagine. Specifica il ridimensionamento dell'immagine di cui è stato effettuato il rendering in modo che l'immagine di risposta non sia più alta del valore specificato, mantenendo le proporzioni dell'immagine.
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 9a58a5d2-43ac-44db-9959-ba166006b7df
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 2%

---


# wid{#wid}

Rispondi alla larghezza dell’immagine. Specifica il ridimensionamento dell&#39;immagine di cui è stato effettuato il rendering in modo che l&#39;immagine di risposta non sia più alta del valore specificato, mantenendo le proporzioni dell&#39;immagine.

`wid= *`val`*`

<table id="simpletable_1C898A7B99114BE986EC5553F6A31E82"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> val</span> </p> </td> 
  <td class="stentry"> <p>Larghezza immagine in pixel (in numero maggiore di 0). </p></td> 
 </tr> 
</table>

L&#39;immagine non viene imbottita se sono specificate sia `wid=` che `hei=` e `wid`/ `hei` sono diverse dalle proporzioni dell&#39;immagine.

`wid=` e  `hei=` collaborare per definire le dimensioni dell&#39;immagine restituita dal server. Se `scl=` viene dopo `wid=` o `hei=` nell&#39;URL, tali comandi vengono annullati e `scl=` definisce le dimensioni dell&#39;immagine restituita dal server.

Tuttavia, se `wid=` o `hei=` viene dopo `scl=` nell&#39;URL, l&#39;annullamento di `scl=` e `wid=`/ `hei=` definisce le dimensioni dell&#39;immagine restituita dal server.

>[!NOTE]
>
>Se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`, viene restituito un errore.

## Proprietà {#section-2d067c6d371748e19cb157684700a49d}

Può verificarsi ovunque nella richiesta. Il ridimensionamento dell&#39;immagine con `wid=`, `hei=` o `scl=` non modifica il valore della risoluzione di stampa incorporato nell&#39;immagine di risposta. Ignorato se `scl=` si verifica dopo `wid=` o `hei=` nella sequenza di comandi.

## Predefinito {#section-c7c6efa03d864592a3398b6f1de5a0b0}

Se non vengono specificati né `wid=`, `hei=`, né `scl=`, l&#39;immagine di risposta viene ridimensionata in modo da rientrare nella dimensione definita da `attribute::DefaultPix`. Se `attribute::DefaultPix` è vuoto, l&#39;immagine di risposta avrà le stesse dimensioni dell&#39;immagine di visualizzazione della vignettatura.

## Consultate anche {#section-450dfc12b1d440e2a3172a69d91db51f}

[attribute::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) ,  [attributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657),  [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478),  [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29),  [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
