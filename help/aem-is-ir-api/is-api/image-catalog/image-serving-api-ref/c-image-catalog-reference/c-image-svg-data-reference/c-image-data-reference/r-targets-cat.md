---
description: Zoom dei dati di destinazione. Nessuna o più proprietà delle destinazioni di zoom, utilizzabili insieme al client del visualizzatore zoom.
seo-description: Zoom dei dati di destinazione. Nessuna o più proprietà delle destinazioni di zoom, utilizzabili insieme al client del visualizzatore zoom.
seo-title: Destinazioni
solution: Experience Manager
title: Destinazioni
topic: Scene7 Image Serving - Image Rendering API
uuid: ca02483a-9aa0-4b54-b6f0-4fd10d8b2b4c
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

---


# Destinazioni{#targets}

Zoom dei dati di destinazione. Nessuna o più proprietà delle destinazioni di zoom, utilizzabili insieme al client del visualizzatore zoom.

Il server restituisce il contenuto di questo campo in risposta a `req=targets`, dopo aver sostituito i token di terminazione del record &#39; `??`&#39;.

A ciascuna destinazione di zoom possono essere associate fino a quattro proprietà:

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num </span></span> </p> </td> 
  <td class="stentry"> <p>Numero destinazione di zoom (int); le destinazioni di zoom devono essere numerate sequenzialmente e consecutivamente, a partire da 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> frame </span></span> </p> </td> 
  <td class="stentry"> <p>Numero di fotogramma/pagina opzionale per il targeting di un fotogramma/pagina specifico di un set 360 gradi o di una serie di brochure; è impostata su 0 se non è specificata per l’uso da parte del visualizzatore per set 360 gradi e per brochure; ignorato dal visualizzatore zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sinistra, in alto </span></span> </p> </td> 
  <td class="stentry"> <p>Offset dei pixel dall’angolo superiore sinistro dell’immagine all’angolo superiore sinistro del rettangolo di destinazione dello zoom (int, int); deve essere uguale o superiore a 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> larghezza, altezza </span></span> </p> </td> 
  <td class="stentry"> <p>Dimensione in pixel del rettangolo di destinazione di zoom (int, int); deve essere maggiore di 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> etichetta </span></span> </p> </td> 
  <td class="stentry"> <p>Valore dei dati di testo; può essere utilizzata come etichetta di testo per un collegamento di destinazione di zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData </span></span> </p> </td> 
  <td class="stentry"> <p>Valore dei dati di testo; può essere utilizzato per trasmettere al client informazioni specifiche per la destinazione, ad esempio un valore SKU o un URL con collegamento a caldo. </p> </td> 
 </tr> 
</table>

Destinazione. *`num`*.rect è richiesto per ciascuna destinazione di zoom e deve specificare un rettangolo completamente all’interno dell’immagine. Tutte le altre proprietà sono facoltative.

*`label`* e *`userData`* partecipare alla localizzazione delle stringhe di testo. Per ulteriori informazioni, vedere Localizzazione [delle stringhe di](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) testo nella Guida di riferimento *del protocollo* HTTP.

Per le applicazioni che coinvolgono i client visualizzatore per set 360 gradi e per brochure, le destinazioni di zoom devono essere definite nello stesso record di catalogo che definisce il set di immagini. Le definizioni delle destinazioni di zoom nei record catalogo dei membri del set di immagini vengono ignorate dal visualizzatore.

I visualizzatori di Scene7 si aspettano destinazioni di zoom nelle coordinate dell’immagine a risoluzione piena già regolate dai comandi `catalog::Modifier`.

## Proprietà {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Valore dei dati](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) delle proprietà.

## Predefinito {#section-feab29f6575e482391086a57f547543c}

Nessuno.

## Consultate anche {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalogo::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) , [catalogo::Modificatore](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834), [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), Localizzazione stringa di [testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
