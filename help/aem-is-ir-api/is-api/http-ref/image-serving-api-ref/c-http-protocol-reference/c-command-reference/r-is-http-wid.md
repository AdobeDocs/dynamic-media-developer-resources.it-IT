---
description: Larghezza visualizzazione. Specifica la larghezza dell’immagine della risposta (immagine di visualizzazione) quando fit= non è presente nella richiesta.
seo-description: Larghezza visualizzazione. Specifica la larghezza dell’immagine della risposta (immagine di visualizzazione) quando fit= non è presente nella richiesta.
seo-title: wid
solution: Experience Manager
title: wid
topic: Scene7 Image Serving - Image Rendering API
uuid: 30aeeea0-c8c9-40b9-a244-2802a7102dd6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# wid{#wid}

Larghezza visualizzazione. Specifica la larghezza dell’immagine della risposta (immagine di visualizzazione) quando fit= non è presente nella richiesta.

` wid= *`val`*`

<table id="simpletable_E217453246F5441C896C1F69EA4D4218"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> val </span> </p> </td> 
  <td class="stentry"> <p>Larghezza immagine in pixel (in numero maggiore di 0). </p> </td> 
 </tr> 
</table>

Se `hei=` e `scl=` sono specificati, l&#39;immagine composita può essere ritagliata in base all&#39; `align=` attributo. Se `fit=` è presente, `wid=` specifica la larghezza esatta, minima o massima dell’immagine di risposta; fare riferimento alla descrizione di `fit=` per maggiori dettagli.

Se non `scl=` viene specificato, l&#39;immagine composita viene ridimensionata per adattarsi. Se vengono specificati `wid=` e `hei=` non `scl=` vengono specificati, l’immagine viene ridimensionata in modo da rientrare interamente all’interno del rettangolo wid/hei, lasciando il minor numero possibile di aree di sfondo. In questo caso, l&#39;immagine viene posizionata all&#39;interno del rettangolo di visualizzazione in base all&#39; `align=` attributo.

>[!NOTE]
>
>Se la dimensione dell&#39;immagine di risposta calcolata o predefinita è maggiore di `attribute::MaxPix`, viene restituito un errore.

## Predefinito {#section-976d4c8554a34c899f85d172f6ac6f58}

Se non `wid=`, `hei=`e non `scl=` vengono specificati, l&#39;immagine di risposta avrà la dimensione dell&#39;immagine composita o, `attribute::DefaultPix`se inferiore, quella dell&#39;immagine.

## Proprietà {#section-c93b7ce1b0d2475f80b06264b45d1285}

Visualizza attributo. Si applica indipendentemente dall’impostazione del livello corrente.

## Esempio {#section-82bc98b7c15a451bbe9b915d414c0470}

Richiedete un’immagine da inserire in un rettangolo da 200x200; allineate l’immagine in alto a destra se non è quadrata. Ogni area di sfondo viene riempita con `attribute::BkgColor`.

` http:// *`server`*/myRootId/myImageId?wid=200&hei=200&align=1,-1`

La stessa immagine, trasmessa a una larghezza fissa di 200 pixel, ma con un&#39;altezza variabile per mantenere le proporzioni dell&#39;immagine. In questo caso, l&#39;immagine restituita non ha mai aree di riempimento di sfondo. In questo caso, align= non avrà alcun effetto.

` http:// *`server`*/myRootId/myImageId?wid=200`

## Consultate anche {#section-4e9659238d6545498378ca8b1f3ec4ae}

[hei=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-hei.md#reference-6d6f556ccc0e4b98a815e8a5c1944a96) , [fit=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-fit.md#reference-f11bff6d93d143d6b135de3a923bc989), [scl=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-scl.md#reference-b2a74e493d0d407e98fe350551ba3fcc), [align=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-align.md#reference-b7d6b87c75124d78884f916dd6544bc7), [attribute::DefaultPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultpix.md#reference-996b2c22b30f4fd9b970c84063306df1), [attribute::MaxPix](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-maxpix.md#reference-e167d396ac794079ba8b5e6eb16eeda5)
