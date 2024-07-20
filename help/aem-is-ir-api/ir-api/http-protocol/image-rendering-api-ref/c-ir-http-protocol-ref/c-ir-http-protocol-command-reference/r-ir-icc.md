---
title: icc
description: Profilo colore di output.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39b25f7c-ed3c-4132-8241-e7f3aab07b00
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '234'
ht-degree: 1%

---

# icc{#icc}

Profilo colore di output.

icc= *`profile`**`renderIntent`*[,*`blackpointComp`*]

<table id="simpletable_DF1914FD351E4F2BA61372A52F0CFFBF"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> profilo</span></span> </p></td> 
  <td class="stentry"> <p>Profilo colore ICC. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> renderIntent </span> </span> </p></td> 
  <td class="stentry"> <p>percettivo | relativo | saturazione | assoluto </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> blackpointComp</span> </span> </p></td> 
  <td class="stentry"> <p>1 per attivare, 0 per disattivare la compensazione del punto nero. </p></td> 
 </tr> 
</table>

*`profile`* Specifica il profilo dello spazio colore di output in cui deve essere convertita l&#39;immagine di cui è stato eseguito il rendering, se diversa dal profilo di lavoro. *`profile`* Deve essere un `icc::Name` valido definito nella mappa del profilo ICC di un catalogo immagini o di un catalogo predefinito oppure un percorso relativo di un file di profilo (in genere con suffisso [!DNL `.icc`] o [!DNL `.icm`]).

>[!NOTE]
>
>*`profile`* potrebbe non includere &#39;,&#39; caratteri, anche se codificati HTTP.

*`renderIntent`* Consente di ignorare l&#39;intento di rendering predefinito.

*`blackpointComp`* Abilita la compensazione del punto nero se il profilo di output supporta questa funzione.

>[!NOTE]
>
>Non tutte le conversioni colore supportano tutte le scelte *`renderIntent`* e *`blackpointComp`*. In genere, queste impostazioni vengono rispettate solo quando il profilo di output ICC caratterizza una periferica di output come una stampante o un monitor. Inoltre, alcuni profili di output ICC non supportano tutte le scelte *`renderIntent`*.

## Proprietà {#section-b4042623a8ea40248c11b2153e5906b1}

Può verificarsi ovunque all’interno della richiesta. Viene restituito un errore se il tipo di immagine specificato con `fmt=` non corrisponde a *`profile`*.

Sia *`renderIntent`* che *`blackpointComp`* vengono ignorati se non sono compatibili con il profilo ICC specificato.

I profili dei dispositivi di output CMYK supportano con maggiore probabilità intenti di rendering diversi.

## Predefinito {#section-bbd3206fdcac4dc48a08fc9eba14fc90}

Se la gestione del colore è abilitata e `icc=` non è specificato, il server distribuisce l&#39;immagine convertita nel profilo di output ( `attribute::IccProfile*`) corrispondente al tipo di immagine specificato con `fmt=`.

Se non specificato, *`renderIntent`* viene ereditato da `attribute::IccRenderIntent` e *`blackpointComp`* da `attribute::IccBlackPointCompensation`.

## Consultate anche {#section-37ef83149fd74345956a98f633cc0294}

[Gestione colore](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-color-management.md#concept-7bac7c2c41be42c1b301eae80abe6b8d), [attributo::IccProfile*](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccprofilecmyk.md#reference-55aead2d924847ffbd1be4c46add7127), [iccEmbed=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-iccembed.md#reference-47a433138c7c4b29b9b29871b2491a7f), [fmt=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-fmt.md#reference-4c743f67d56b47c5b774fcc900ff758c), [attributo::IccRenderIntent](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccrenderintent.md#reference-3b80b7a4c25545a593c5076f318b5c40), [attributo::IccBlackPointCompensation](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-iccblackpointcompensation.md#reference-d939b0cdf6564baaa88deb1059e3b7f0)
