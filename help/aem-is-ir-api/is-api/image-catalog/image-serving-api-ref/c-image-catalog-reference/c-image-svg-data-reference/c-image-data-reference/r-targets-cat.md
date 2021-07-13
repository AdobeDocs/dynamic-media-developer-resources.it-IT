---
description: Zoom dei dati di destinazione. Nessuna o più proprietà di destinazione dello zoom, utilizzabili insieme al client del visualizzatore di zoom.
solution: Experience Manager
title: Destinazioni
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b882ba01-a1ef-4179-95c7-964c2578aad1
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 2%

---

# Destinazioni{#targets}

Zoom dei dati di destinazione. Nessuna o più proprietà di destinazione dello zoom, utilizzabili insieme al client del visualizzatore di zoom.

Il server restituisce il contenuto di questo campo in risposta a `req=targets`, dopo aver sostituito i token di terminazione dei record &#39; `??`&#39;.

A ciascuna destinazione di zoom possono essere associate fino a quattro proprietà:

` Target. *``*.frame= *`numframe`*`

` Target. *``*.rect= *`numleft,top,width,height`*`

` Target. *``*.label= *`numlabel`*`

` Target. *``*.userData= *`numuserData`*`

<table id="simpletable_4C20157A7A444DEB9959B335CAFBAEC8"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> num  </span> </span> </p> </td> 
  <td class="stentry"> <p>Zoom del numero di destinazione (int); le destinazioni di zoom devono essere numerate sequenzialmente e consecutivamente, a partire da 1. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> cornice  </span> </span> </p> </td> 
  <td class="stentry"> <p>Numero opzionale di fotogramma/pagina per il targeting di un frame/pagina specifico di un set 360 gradi o di brochure; viene impostato su 0 se non specificato per l'uso del visualizzatore di spin e brochure; ignorato dal visualizzatore zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sinistra, in alto  </span> </span> </p> </td> 
  <td class="stentry"> <p>Offset pixel dall'alto a sinistra dell'immagine all'alto a sinistra del rettangolo di destinazione dello zoom (int, int); deve essere maggiore o uguale a 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> larghezza, altezza  </span> </span> </p> </td> 
  <td class="stentry"> <p>Dimensioni dei pixel del rettangolo di destinazione dello zoom (int, int); deve essere maggiore di 0. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> etichetta  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore dei dati di testo; può essere utilizzata come etichetta di testo per un collegamento di destinazione zoom. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> userData  </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore dei dati di testo; può essere utilizzato per trasmettere informazioni specifiche di target al client, ad esempio un valore SKU o un URL di collegamento rapido. </p> </td> 
 </tr> 
</table>

Destinazione. *`num`* Per ciascuna destinazione di zoom è necessario .rect e specificare un rettangolo completamente all’interno dell’immagine. Tutte le altre proprietà sono facoltative.

*`label`* e  *`userData`* partecipare alla localizzazione delle stringhe di testo. Per ulteriori informazioni, consulta [Localizzazione delle stringhe di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md) in *Riferimento al protocollo HTTP* .

Per le applicazioni che coinvolgono i client di visualizzazione di spin e brochure, le destinazioni di zoom devono essere definite nello stesso record di catalogo che definisce il set di immagini. Tutte le definizioni di destinazione di zoom nei record di catalogo dei membri del set di immagini vengono ignorate dal visualizzatore.

I visualizzatori Dynamic Media si aspettano che le destinazioni di zoom nelle coordinate dell&#39;immagine a risoluzione piena già regolate dai comandi di `catalog::Modifier`.

## Proprietà {#section-b3f8eba4985f4b00bb935d592fe770f9}

[Valore ](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-common-data-types/r-property-data.md) dati proprietà.

## Predefinito {#section-feab29f6575e482391086a57f547543c}

Nessuno.

## Consultate anche {#section-83dea73b1dbf4aa1b64b0aae2933e6e1}

[catalogo::ImageSet](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md#reference-4764d347afd64afdaede9a74c7565256) ,  [catalogo::Modificatore](../../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-modifier-cat.md#reference-d2c6884b3a2248fab81a112d27969834),  [req=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-req/r-req.md), Localizzazione stringa  [di testo](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-text-string-localization.md)
