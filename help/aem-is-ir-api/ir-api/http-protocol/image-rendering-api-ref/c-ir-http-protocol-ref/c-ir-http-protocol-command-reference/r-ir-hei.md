---
title: hei
description: Altezza immagine di risposta. Specifica il ridimensionamento dell'immagine di cui è stato eseguito il rendering in modo che l'altezza dell'immagine di risposta non superi il valore specificato, mantenendo le proporzioni dell'immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e93aa32-b38e-46e4-be52-abd81222cfc3
TQID: 'https://experienceleague.adobe.com/-sH3rlYycsZ36DheRgEpMUm6xSuUnY7s-3awUgdfloA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 245
ht-degree: 1%

---

# hei{#hei}

Altezza immagine di risposta. Specifica il ridimensionamento dell&#39;immagine di cui è stato eseguito il rendering in modo che l&#39;altezza dell&#39;immagine di risposta non superi il valore specificato, mantenendo le proporzioni dell&#39;immagine.

`hei= *`val`*`

<table id="simpletable_C3A31CA539DC4D9F8BE50290D1AFA5CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span> </span> </p></td> 
  <td class="stentry"> <p>Altezza immagine di risposta in pixel (numero intero maggiore di 0). </p></td> 
 </tr> 
</table>

L&#39;immagine non viene imbottita se sono specificati sia `wid=` che `hei=` e la larghezza/altezza è diversa dalle proporzioni dell&#39;immagine.

`wid=` e `hei=` collaborano per definire le dimensioni dell&#39;immagine restituita dal server. Se `scl=` viene dopo `wid=` o `hei=` nell&#39;URL, questi comandi vengono annullati e `scl=` definisce la dimensione dell&#39;immagine restituita dal server.

Tuttavia, se `wid=` o `hei=` arriva dopo `scl=` nell&#39;URL, annullano `scl=` e `wid=`/ `hei=` definiscono le dimensioni dell&#39;immagine restituita dal server.

>[!NOTE]
>
>Viene restituito un errore se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`.

## Proprietà {#section-6cbc6acd37c847beab84c896ac25280c}

Può verificarsi ovunque all’interno della richiesta. Il ridimensionamento dell&#39;immagine con `wid=`, `hei=` o `scl=` non modifica il valore della risoluzione di stampa incorporato nell&#39;immagine di risposta. Ignorato se `scl=` si verifica dopo `wid=` e/o `hei=` nella sequenza di comando.

## Predefinito {#section-61043f6c1f5d450883ff9e5eafd95955}

Se `wid=`, `hei=` o `scl=` non sono specificati, l&#39;immagine di risposta viene ridimensionata in base alle dimensioni definite da `attribute::DefaultPix`. Se `attribute::DefaultPix` è vuoto, l&#39;immagine di risposta ha le stesse dimensioni dell&#39;immagine di visualizzazione della vignettatura.

## Consultate anche {#section-7ba51379f1e2421c92d3592d20a37734}

[attributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f) , [attributo::MaxPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-maxpix.md#reference-569f186bbc2840a6bd3cffa8ff3e7657), [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [scl=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-scl.md#reference-b14b51a6cbe34f0bba42880540592f29), [resMode=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-resmode.md#reference-851a5b636f8948cfb11456c9b7dab0d3)
