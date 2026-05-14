---
description: Mappa di traduzione stringa. Fa riferimento a un locId che può essere mappato a qualsiasi numero di internalLocId.
solution: Experience Manager
title: LocaleStrMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48a1c71c-78a9-43db-8b1a-4189d34b0982
TQID: 'https://experienceleague.adobe.com/tEpdZ-AEabQKLIV1Zkwh9JG7-LHV4gABlmv9PLPqz08'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---

# LocaleStrMap{#localestrmap}

Mappa di traduzione stringa. Fa riferimento a un locId che può essere mappato a qualsiasi numero di internalLocId.

`*`elemento`*&#42;['|' *`elemento`*]`

<table id="simpletable_26A9A6904C85459F89DCDD98C14139CA"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> elemento </span> </p> </td> 
  <td class="stentry"> <p> <span class="varname"> impostazioni locali </span>, <span class="varname"> locId </span>*[',' <span class="varname"> locId </span>] </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> lingua </span> </p> </td> 
  <td class="stentry"> <p>Locale (senza distinzione maiuscole/minuscole). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> locId </span> </p> </td> 
  <td class="stentry"> <p>ID delle impostazioni locali interne. </p> </td> 
 </tr> 
</table>

`LocaleStrMap` fa riferimento a un `locId` che può essere mappato a qualsiasi numero di `internalLocId`.

Un valore *`locale`* vuoto corrisponde a stringhe `locale=` vuote e sconosciute. Ciò consente di definire una regola predefinita per le lingue sconosciute.

I valori *`locId`* vuoti sono consentiti e selezionare *`defaultString`* (l&#39;identificatore delle impostazioni locali non è disponibile per *`defaultString`*). La ricerca di *`locId`* valori viene eseguita nell&#39;ordine specificato. Viene restituita la prima corrispondenza.

La traduzione di stringhe, se abilitata, viene applicata alle stringhe di testo nei seguenti campi del catalogo immagini:

<table id="table_EE0321F9890B45CA8C364178F5100D40"> 
 <tbody> 
  <tr valign="top"> 
   <td> <b>Campo catalogo</b> </td> 
   <td> <b>Elemento stringa nel campo</b> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> Catalogo <span class="codeph">::Set di immagini </span> </p> </td> 
   <td> <p>Qualsiasi sottoelemento contenente una stringa traducibile (delimitata da qualsiasi combinazione di separatori ',' ';' ':' e/o l'inizio/la fine del campo). </p> <p>Un valore di colore <span class="codeph"> 0xrggbb </span> all'inizio di un campo localizzabile è escluso dalla localizzazione e trasmesso senza modifiche. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::Mappa </span> </p> </td> 
   <td> <p>Qualsiasi valore di attributo racchiuso tra virgolette singole o doppie, ad eccezione dei valori degli attributi <span class="codeph"> coords= </span> e <span class="codeph"> shape= </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> <span class="codeph"> catalogo::Destinazioni </span> </p> </td> 
   <td> <p>Valore di qualsiasi proprietà <span class="filepath"> di destinazione.*.label </span> e <span class="filepath"> di destinazione.*.userdata </span>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td> <p> Catalogo <span class="codeph">::Dati utente </span> </p> </td> 
   <td> <p>Il valore di qualsiasi proprietà. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-8505a8525f6948ada3979f68c4081044}

Uno o più elementi separati da |, dove ogni elemento è costituito da due o più valori stringa separati da virgola.

## Consultate anche {#section-0c0516e4f83d42d38247308cab9b6708}

Supporto localizzazione, [impostazioni locali=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [catalogo::ImageSet](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-imageset-cat.md), [catalogo::Map](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-map-cat.md), [catalogo::Target](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-targets-cat.md), [catalogo::UserData](/help/aem-is-ir-api/is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-userdata-cat.md)
