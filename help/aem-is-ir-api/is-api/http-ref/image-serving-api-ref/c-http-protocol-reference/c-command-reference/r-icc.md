---
description: Profilo colore di output.
seo-description: Profilo colore di output.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: cfbd18aa-cbba-4085-920d-1f54645d0f89
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

Profilo colore di output.

`icc= *``*[, *``*[, *``*[, *`objectrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span></span> </p></td> 
  <td class="stentry"> <p>Profilo colore ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderingIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> percettivo|relativo|saturazione|assoluto</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 per abilitare, 0 per disabilitare la compensazione dei punti neri. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dithering</span></span> </p></td> 
  <td class="stentry"> <p>1 per abilitare, 0 per disabilitare il dithering. </p></td> 
 </tr> 
</table>

*`object`* specifica il profilo dello spazio colore di output in cui deve essere convertita l’immagine se è diversa dal profilo di lavoro. *`profile`* deve essere un percorso valido `icc::Name` definito nella mappa del profilo ICC di un catalogo di immagini o di un catalogo predefinito, oppure un percorso relativo a un file di profilo (in genere con [!DNL .icc] o [!DNL .icm] suffisso). Consultate [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)per ulteriori informazioni.

>[!NOTE]
>
>*`object`* può non includere caratteri &#39;,&#39;, anche se con codifica HTTP.

*`renderIntent`* consente di sovrascrivere l&#39;intento di rendering predefinito.

*`blackpointComp`* attiva la compensazione dei punti neri se il profilo di output supporta questa funzione.

>[!NOTE]
>
>Non tutte le conversioni dei colori supportano tutte *`renderIntent`* e *`blackpointComp`* le scelte. In genere, queste impostazioni vengono rispettate solo quando il profilo di output ICC caratterizza una periferica di output come una stampante o un monitor. Inoltre, alcuni profili di output ICC non supportano tutte *`renderIntent`* le scelte.

Nota

*`dither`* attiva il dithering (in realtà la diffusione dell’errore), che può evitare o ridurre gli artefatti di bande dei colori.

## Proprietà {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Attributo di richiesta. Il server restituisce un errore se viene specificato un tipo di immagine `fmt=` che non corrisponde *`profile`*.

*`renderIntent`* e *`blackpointComp`* vengono ignorati se non sono compatibili con il profilo ICC specificato. È più probabile che i profili dei dispositivi di output CMYK supportino intenti di rendering diversi.

## Predefinito {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Se la gestione del colore è abilitata e non `icc=` è specificata, il server distribuirà l&#39;immagine convertita nel profilo di output ( `attribute::IccProfile*`) corrispondente al tipo di immagine con cui è stata specificata `fmt=`.

Se non viene specificato, *`renderIntent`* viene ereditato da `attribute::IccRenderIntent`, *`blackpointComp`* viene ereditato da `attribute::IccBlackPointCompensation`, e *`dither`* viene ereditato da `attribute::IccDither`.

## Consultate anche {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attributo::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attributo::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attributo::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)[](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)[](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c)[objectsack, Color Management, Riferimento mappa profilo ICC, Embed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
