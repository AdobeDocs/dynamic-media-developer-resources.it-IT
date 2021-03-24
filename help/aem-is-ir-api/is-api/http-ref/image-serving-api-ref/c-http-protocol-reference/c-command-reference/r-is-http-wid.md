---
description: Larghezza visualizzazione. Specifica la larghezza dell'immagine della risposta (visualizza immagine) quando fit= non è presente nella richiesta.
solution: Experience Manager
title: wid
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 2%

---


# wid{#wid}

Larghezza visualizzazione. Specifica la larghezza dell&#39;immagine della risposta (visualizza immagine) quando fit= non è presente nella richiesta.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val  </span> </p> </td> 
  <td class="stentry"> <p>Larghezza immagine in pixel (in numero maggiore di 0). </p> </td> 
 </tr> 
</table>

Se sono specificati sia `hei=` che `scl=`, l&#39;immagine composita può essere ritagliata in base all&#39;attributo `align=`. Quando `fit=` è presente, `wid=` specifica la larghezza esatta, la minima o la massima dell&#39;immagine di risposta; per ulteriori informazioni, fare riferimento alla descrizione di `fit=` .

Se `scl=` non è specificato, l&#39;immagine composita viene ridimensionata per adattarsi. Se sono specificati sia `wid=` che `hei=` e `scl=` non è specificato, l&#39;immagine viene ridimensionata in modo da adattarsi interamente al rettangolo wid/hei, lasciando il minor spazio di sfondo possibile esposto. In questo caso, l&#39;immagine viene posizionata all&#39;interno del rettangolo di visualizzazione in base all&#39;attributo `align=`.

>[!NOTE]
>
>Se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`, viene restituito un errore.

## Predefinito {#section-976d4c8554a34c899f85d172f6ac6f58}

Se non vengono specificati né `wid=`, `hei=`, né `scl=`, l&#39;immagine di risposta avrà le dimensioni dell&#39;immagine composita o `attribute::DefaultPix`, a seconda di quale dimensione è inferiore.

## Proprietà {#section-c93b7ce1b0d2475f80b06264b45d1285}

Visualizza attributo. Si applica indipendentemente dall&#39;impostazione del livello corrente.

## Esempio {#section-82bc98b7c15a451bbe9b915d414c0470}

Richiedere un&#39;immagine per inserirla in un rettangolo 200x200; allineate l&#39;immagine in alto a destra se non è quadrata. Ogni area di sfondo viene riempita con `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

La stessa immagine, distribuita a una larghezza fissa di 200 pixel, ma con un&#39;altezza variabile per mantenere le proporzioni dell&#39;immagine. In questo caso, l&#39;immagine restituita non ha mai aree di riempimento di sfondo. Tieni presente che in questo caso align= non avrebbe alcun effetto.

` http:// *`server`*/myRootId/myImageId?wid=200`

## Consultate anche {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) ,  [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989),  [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc),  [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7),  [attributo::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1),  [attributo::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
