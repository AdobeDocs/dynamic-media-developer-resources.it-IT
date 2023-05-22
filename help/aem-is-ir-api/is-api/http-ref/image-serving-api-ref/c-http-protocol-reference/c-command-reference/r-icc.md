---
description: Profilo colore di output.
solution: Experience Manager
title: icc
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8be7be8c-a23d-4a5b-93e4-44231155616b
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 3%

---

# icc{#icc}

Profilo colore di output.

`icc= *`oggetto`*[, *`renderIntent`*[, *`blackpointComp`*[, *`dithering`*]]`

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
  <td class="stentry"> <p>1 per attivare, 0 per disattivare la compensazione del punto nero. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> dithering</span></span> </p></td> 
  <td class="stentry"> <p>1 per attivare, 0 per disattivare il dithering. </p></td> 
 </tr> 
</table>

*`object`* specifica il profilo dello spazio colore di output in cui deve essere convertita l&#39;immagine, se diverso dal profilo di lavoro. *`profile`* deve essere un `icc::Name` definito nella mappa di profilo ICC di un catalogo immagini o di un catalogo predefinito, oppure un percorso relativo di un file di profilo (in genere con [!DNL .icc] o [!DNL .icm] suffisso). Consulta [ *`object`*](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0)per ulteriori informazioni.

>[!NOTE]
>
>*`object`* non può includere i caratteri &quot;,&quot;, anche se con codifica HTTP.

*`renderIntent`* consente di ignorare l’intento di rendering predefinito.

*`blackpointComp`* abilita la compensazione del punto nero se il profilo di output supporta questa funzione.

>[!NOTE]
>
>Non tutte le conversioni colore supportano tutte *`renderIntent`* e *`blackpointComp`* scelte. In genere, queste impostazioni vengono rispettate solo quando il profilo di output ICC caratterizza una periferica di output come una stampante o un monitor. Inoltre, alcuni profili di output ICC non supportano tutti *`renderIntent`* scelte.

Nota

*`dither`* consente il dithering (ovvero la diffusione di errori), che può evitare o ridurre gli artefatti di striature di colore.

## Proprietà {#section-9fcd3e7bd1fd43c887b0f18a2f3c7259}

Attributo della richiesta. Il server restituirà un errore se viene specificato un tipo di immagine con `fmt=` che non corrisponde *`profile`*.

*`renderIntent`* e *`blackpointComp`* vengono ignorati se non compatibili con il profilo ICC specificato. I profili dei dispositivi di output CMYK supportano con maggiore probabilità intenti di rendering diversi.

## Predefinito {#section-0b9fe2eb428447df8ae9948f11ab5aae}

Se la gestione del colore è abilitata e `icc=` non è specificato, il server distribuirà l&#39;immagine convertita nel profilo di output ( `attribute::IccProfile*`) corrisponde al tipo di immagine specificato con `fmt=`.

Se non specificato, *`renderIntent`* viene ereditato da `attribute::IccRenderIntent`, *`blackpointComp`* viene ereditato da `attribute::IccBlackPointCompensation`, e *`dither`* viene ereditato da `attribute::IccDither`.

## Consultate anche {#section-37f16b0c2c4b48f3a39dcde2a350f91e}

[attribute::IccProfile*](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccprofilecmyk.md#reference-db89f9dac33e447cadb359ec1ba27ee0) , [attribute::IccRenderIntent](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccrenderintent.md#reference-012f207f28bd4406a5368d23ed95a51f), [attribute::Compensazione punto nero Icc](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccblackpointcompensation.md#reference-357626375ee140d1807f0c05171c733f), [attribute::IccDither](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-iccdither.md#reference-914d0d0567364246b4016d45c0ada85b), [fmt=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-fmt.md#reference-cdf10043423b45ba9fe15157fb3ae37a), [oggetto](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-object.md#reference-2591bd24548d462782c68d138ef795a0), [Gestione colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7), [Riferimento mappa profilo ICC](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-icc-profile-map-reference/c-icc-profile-map-reference.md#concept-57b9148ce55249cd825cb7ee19ed057c), [iccEmbed=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-iccembed.md#reference-e3b774fb322046a2a6dde3a7bab5583e)
