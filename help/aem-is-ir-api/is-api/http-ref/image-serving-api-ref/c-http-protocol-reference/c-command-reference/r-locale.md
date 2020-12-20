---
description: ID lingua traduzione. Specifica l'ID delle impostazioni internazionali per la richiesta.
seo-description: ID lingua traduzione. Specifica l'ID delle impostazioni internazionali per la richiesta.
seo-title: locale
solution: Experience Manager
title: locale
topic: Scene7 Image Serving - Image Rendering API
uuid: 82acc0bb-fd94-44c9-8ff9-3b9cefab4627
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 5%

---


# locale{#locale}

ID lingua traduzione. Specifica l&#39;ID delle impostazioni internazionali per la richiesta.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>ID lingua (stringa). </p></td> 
 </tr> 
</table>

Utilizzando questo ID e le regole specificate con `attribute::LocaleMap` e `attribute::LocaleStrMap`, Image Server applica la traduzione ID catalogo e la localizzazione delle stringhe facoltative.

## Proprietà {#section-1854a9902b884d9b8e8e713b6635723f}

Richiedi, comando. Si applica all’intera richiesta, incluse le richieste nidificate/incorporate, indipendentemente da dove è specificata. `locId` devono includere solo caratteri ASCII stampabili. Ignorato se nel catalogo principale di questa richiesta non sono definiti mappe di localizzazione. Viene restituito un errore se è specificato vuoto o non valido `locId` e non è definita alcuna regola predefinita in `attribute::DefaultLocale`.

## Predefinito {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` viene utilizzato quando locale= non è specificato.

## Consultate anche {#section-28a586d43ac4429d98e318a580c92af4}

[attributo::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) ,  [attributo::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318),  [attributo::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), supporto della localizzazione
