---
description: Mappa di traduzione stringa. Si riferisce a un locId che può essere mappato a qualsiasi numero di internalLocId.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---

# LocaleStrMap{#localestrmap}

Mappa di traduzione stringa. Si riferisce a un locId che può essere mappato a qualsiasi numero di internalLocId.

`*``*&#42;['|' *`elemento`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> item </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> locale  </span>,  <span class="varname"> locId  </span>*[','  <span class="varname"> locId  </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locale </span> </p> </td> 
  <td class="stentry"> <p>Impostazioni internazionali (senza distinzione maiuscole/minuscole). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId  </span> </p> </td> 
  <td class="stentry"> <p>ID locale interno. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` si riferisce a un  `locId` che può essere mappato a qualsiasi numero di  `internalLocId`.

Un valore vuoto *`locale`* corrisponde a stringhe vuote e sconosciute `locale=`. Questo consente di definire una regola predefinita per le impostazioni internazionali sconosciute.

I valori vuoti *`locId`* sono consentiti e selezionare *`defaultString`* (il *`defaultString`* non dispone di un identificatore locale). *`locId`* la ricerca dei valori viene eseguita nell&#39;ordine specificato. Viene restituita la prima corrispondenza.

La traduzione di stringhe, se abilitata, viene applicata alle stringhe di testo nei seguenti campi del catalogo immagini:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Campo catalogo</b> </td> 
   <td> <b>Elemento stringa nel campo</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::ImageSet  </span> </p> </td> 
   <td> <p>Qualsiasi sottoelemento contenente una stringa traducibile (delimitata da qualsiasi combinazione di separatori ',' ';' ':' e/o l'inizio/fine del campo). </p> <p>Un valore di colore <span class="codeph"> 0xrggbb </span> all'inizio di un campo localizzabile è escluso dalla localizzazione e trasmesso senza modifiche. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::Mappa  </span> </p> </td> 
   <td> <p>Qualsiasi valore di attributo tra virgolette singole o doppie, ad eccezione dei valori degli attributi <span class="codeph"> coords= </span> e <span class="codeph"> shape= </span> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::Target  </span> </p> </td> 
   <td> <p>Il valore di qualsiasi destinazione <span class="filepath">.*.label </span> e <span class="filepath"> target.*.userdata </span> proprietà . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::UserData  </span> </p> </td> 
   <td> <p>Il valore di qualsiasi proprietà. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8505a8525f6948ada3979f68c4081044}

Uno o più elementi separati con |, dove ogni elemento è costituito da due o più valori stringa separati da virgole.

## Consultate anche {#section-0c0516e4f83d42d38247308cab9b6708}

Supporto per la localizzazione, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalogo::Targets](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalogo::UserData&lt;a 11/2011](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
