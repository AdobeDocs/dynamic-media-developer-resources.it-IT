---
description: Profilo colore di output.
seo-description: Profilo colore di output.
seo-title: icc
solution: Experience Manager
title: icc
topic: Scene7 Image Serving - Image Rendering API
uuid: 95a05fe5-d6b3-4118-aab4-4664ccee2850
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# icc{#icc}

Profilo colore di output.

icc= *`profile`*[, *`renderIntent`*[,*`blackpointComp`*]]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> profilo</span></span> </p></td> 
  <td class="stentry"> <p>Profilo colore ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderingIntent </span></span> </p></td> 
  <td class="stentry"> <p>percettivo| relativo| saturazione| assoluto </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span></span> </p></td> 
  <td class="stentry"> <p>1 per abilitare, 0 per disabilitare la compensazione dei punti neri. </p></td> 
 </tr> 
</table>

*`profile`* specifica il profilo dello spazio colore di output in cui deve essere convertita l’immagine di cui è stato effettuato il rendering, se è diversa dal profilo di lavoro. *`profile`* deve essere un percorso valido `icc::Name` definito nella mappa del profilo ICC di un catalogo di immagini o di un catalogo predefinito, oppure un percorso relativo a un file di profilo (in genere con [!DNL .icc]o [!DNL .icm] suffisso).

>[!NOTE]
>
>*`profile`* può non includere caratteri &#39;,&#39;, anche se con codifica HTTP.

*`renderIntent`* consente di sovrascrivere l&#39;intento di rendering predefinito.

*`blackpointComp`* attiva la compensazione dei punti neri se il profilo di output supporta questa funzione.

>[!NOTE]
>
>Non tutte le conversioni dei colori supportano tutte *`renderIntent`* e *`blackpointComp`* le scelte. In genere, queste impostazioni vengono rispettate solo quando il profilo di output ICC caratterizza una periferica di output come una stampante o un monitor. Inoltre, alcuni profili di output ICC non supportano tutte *`renderIntent`* le scelte.

## Proprietà {#section-b4042623a8ea40248c11b2153e5906b1}

Può verificarsi ovunque nella richiesta. Se il tipo di immagine specificato con `fmt=` non corrisponde, viene restituito un errore *`profile`*.

*`renderIntent`* e *`blackpointComp`* vengono ignorati se non sono compatibili con il profilo ICC specificato.

È più probabile che i profili dei dispositivi di output CMYK supportino intenti di rendering diversi.

## Predefinito {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Se la gestione del colore è abilitata e non `icc=` è specificata, il server distribuirà l&#39;immagine convertita nel profilo di output ( `attribute::IccProfile*`) corrispondente al tipo di immagine con cui è stata specificata `fmt=`.

Se non viene specificato, *`renderIntent`* viene ereditato da `attribute::IccRenderIntent`e *`blackpointComp`* viene ereditato da `attribute::IccBlackPointCompensation`.

## Consultate anche {#section-37ef83149fd74345956a98f633cc0294}

[Gestione](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d)del colore, [attributo::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attributo::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
