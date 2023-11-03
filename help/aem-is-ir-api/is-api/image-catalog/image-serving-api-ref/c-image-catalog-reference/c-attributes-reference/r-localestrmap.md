---
description: Mappa di traduzione stringa. Fa riferimento a un locId che può essere mappato a qualsiasi numero di internalLocId.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# LocaleStrMap{#localestrmap}

Mappa di traduzione stringa. Fa riferimento a un locId che può essere mappato a qualsiasi numero di internalLocId.

`*`elemento`*&#42;['|' *`elemento`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> lingua </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Locale (senza distinzione maiuscole/minuscole). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>ID delle impostazioni locali interne. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` fa riferimento a un `locId` che possono essere mappati su un numero qualsiasi di `internalLocId`.

Un campo vuoto *`locale`* il valore corrisponde a vuoto e sconosciuto `locale=` stringhe. Ciò consente di definire una regola predefinita per le lingue sconosciute.

Vuoto *`locId`* sono consentiti e seleziona l&#39;opzione *`defaultString`* (il *`defaultString`* non dispone di un identificatore di impostazioni locali). *`locId`* la ricerca dei valori viene eseguita nell&#39;ordine specificato. Viene restituita la prima corrispondenza.

La traduzione di stringhe, se abilitata, viene applicata alle stringhe di testo nei seguenti campi del catalogo immagini:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Campo catalogo</b> </td> 
   <td> <b>Elemento stringa nel campo</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::ImageSet </span> </p> </td> 
   <td> <p>Qualsiasi sottoelemento contenente una stringa traducibile (delimitata da qualsiasi combinazione di separatori ',' ';' ':' e/o l'inizio/la fine del campo). </p> <p>A <span class="codeph"> 0xrggbb </span> il valore del colore all’inizio di un campo localizzabile è escluso dalla localizzazione e trasmesso senza modifiche. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::Mappa </span> </p> </td> 
   <td> <p>Qualsiasi valore di attributo con virgolette singole o doppie, ad eccezione dei valori <span class="codeph"> coords= </span> e <span class="codeph"> shape= forma </span> attributi. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::Destinazioni </span> </p> </td> 
   <td> <p>Il valore di qualsiasi <span class="filepath"> target.*.label </span> e <span class="filepath"> target.*.userdata </span> proprietà. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalog::DatiUtente </span> </p> </td> 
   <td> <p>Il valore di qualsiasi proprietà. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8505a8525f6948ada3979f68c4081044}

Uno o più elementi separati da |, dove ogni elemento è costituito da due o più valori stringa separati da virgola.

## Consultate anche {#section-0c0516e4f83d42d38247308cab9b6708}

Supporto per la localizzazione, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalogo::Mappa](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalogo::Destinazioni](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalog::DatiUtente](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
