---
title: locale
description: ID lingua traduzione. Specifica l'ID delle impostazioni locali per la richiesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d937dfa5-95dd-49fd-ac23-e77e07b0642c
source-git-commit: 7a07ec9550c0685c908191dd6806d5b84678820d
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# locale{#locale}

ID lingua traduzione. Specifica l&#39;ID delle impostazioni locali per la richiesta.

`locale=[ *`locId`*]`

<table id="simpletable_C1899AD02C984ED3896B7620916637E7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> locId</span></span> </p> </td> 
  <td class="stentry"> <p>ID lingua (stringa). </p></td> 
 </tr> 
</table>

Utilizzo di questo ID e delle regole specificate con `attribute::LocaleMap` e `attribute::LocaleStrMap`, Image Server applica la traduzione facoltativa dell’ID catalogo e la localizzazione delle stringhe.

## Proprietà {#section-1854a9902b884d9b8e8e713b6635723f}

Comando di richiesta. Si applica all’intera richiesta, incluse le richieste nidificate/incorporate, indipendentemente da dove è specificata. `locId` deve includere solo caratteri ASCII stampabili. Ignorato se non sono definite mappe di localizzazione nel catalogo principale di questa richiesta. Se vuoto o non valido, viene restituito un errore `locId` è specificato e nessuna regola predefinita è definita in `attribute::DefaultLocale`.

## Predefinito {#section-9699fbc26de6453e9029e0003c79a7ef}

`attribute::DefaultLocale` viene utilizzato quando locale= non è specificato.

## Consultate anche {#section-28a586d43ac4429d98e318a580c92af4}

[attribute::DefaultLocale](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultlocale.md#reference-69462ad9923f464f80c2c012342a6b6b) , [attribute::LocaleMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localemap.md#reference-49bbf598f8ea47c3a563755cef306318), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e), Supporto per la localizzazione
