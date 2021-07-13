---
description: Profilo colore di output.
solution: Experience Manager
title: icc
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 4%

---

# icc{#icc}

Profilo colore di output.

`icc= *``*[, *``*[, *``*[, *`oggtrenderIntentblackpointCompdither`*]]`

<table id="simpletable_AC20916999004CDCBBB9888B3A8FB0A7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> oggetto</span> </span> </p></td> 
  <td class="stentry"> <p>Profilo colore ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> percettivo|relativo|saturazione|assoluto</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 per abilitare, 0 per disabilitare la compensazione dei punti neri. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dietesi</span></span> </p></td> 
  <td class="stentry"> <p>1 per abilitare, 0 per disabilitare il dithering. </p></td> 
 </tr> 
</table>

*`object`* specifica il profilo dello spazio colore di output in cui l’immagine deve essere convertita se è diversa dal profilo di lavoro. *`profile`* deve essere un percorso valido  `icc::Name` definito nella mappa del profilo ICC di un catalogo di immagini o di un catalogo predefinito oppure un percorso relativo a un file di profilo (in genere con  [!DNL .icc] o  [!DNL .icm] suffisso). Per ulteriori informazioni, consulta [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0).

>[!NOTE]
>
>*`object`* potrebbero non includere caratteri &#39;,&#39;, anche se codificati per HTTP.

*`renderIntent`* consente di ignorare l’intento di rendering predefinito.

*`blackpointComp`* abilita la compensazione dei punti neri se il profilo di output supporta questa funzione.

>[!NOTE]
>
>Non tutte le conversioni di colore supportano tutte le scelte *`renderIntent`* e *`blackpointComp`*. In genere, queste impostazioni vengono rispettate solo quando il profilo di output ICC caratterizza una periferica di output come una stampante o un monitor. Inoltre, alcuni profili di output ICC non supportano tutte le scelte *`renderIntent`*.

Nota

*`dither`* consente il dithering (in realtà la diffusione dell’errore), che può evitare o ridurre gli artefatti di striatura del colore.

## Proprietà {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Attributo di richiesta. Il server restituisce un errore se viene specificato un tipo di immagine con `fmt=` che non corrisponde a *`profile`*.

*`renderIntent`* e  *`blackpointComp`* vengono ignorati se non sono compatibili con il profilo ICC specificato. I profili dispositivo di output CMYK supportano più probabilità di intenti di rendering diversi.

## Predefinito {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Se la gestione del colore è abilitata e `icc=` non è specificato, il server distribuirà l&#39;immagine convertita nel profilo di output ( `attribute::IccProfile*`) corrispondente al tipo di immagine specificato con `fmt=`.

Se non viene specificato, *`renderIntent`* viene ereditato da `attribute::IccRenderIntent`, *`blackpointComp`* viene ereditato da `attribute::IccBlackPointCompensation` e *`dither`* viene ereditato da `attribute::IccDither`.

## Consultate anche {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attributo::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) ,  [attributo::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f),  [attributo::IccBlackPointCompensation](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f),  [attributo::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b),  [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a),  [oggetto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0),  [Gestione colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7),  [Riferimento mappa profilo ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c),  [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
