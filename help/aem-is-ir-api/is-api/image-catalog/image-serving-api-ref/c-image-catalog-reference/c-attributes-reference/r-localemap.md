---
description: Mappa di traduzione ID. Specifica le regole utilizzate per tradurre gli ID immagine generici in ID specifici per le impostazioni internazionali.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 1%

---

# LocaleMap{#localemap}

Mappa di traduzione ID. Specifica le regole utilizzate per tradurre gli ID immagine generici in ID specifici per le impostazioni internazionali.

`*`elemento`*&#42;['|' *`elemento`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> item</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>ID lingua (senza distinzione maiuscole/minuscole). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Suffisso locale. </p></td> 
 </tr> 
</table>

`LocaleMap` fa riferimento a un `locId` che possono essere mappati su un numero qualsiasi di `locSuffix`.

Vuoto *`locSuffix`* sono consentiti. *`locSuffix`* i valori devono essere ordinati nell&#39;ordine in cui devono essere cercati. Viene restituita la prima corrispondenza.

Image Server esegue ricerche nella *`locId`* valori per una corrispondenza senza distinzione tra maiuscole e minuscole con `locale=` valore specificato nella richiesta. Se viene trovata una corrispondenza, la prima *`locSuffix`* il valore viene aggiunto all’id catalogo originale. Se questa voce di catalogo esiste, viene utilizzata, altrimenti viene utilizzata la voce successiva *`locSuffix`* valore è stato tentato. Se nessuna delle *`locSuffix`* corrisponde a una voce di catalogo; Image Server restituisce un errore o un’immagine predefinita.

Un campo vuoto *`locId`* il valore corrisponde a vuoto e sconosciuto `locale=` stringhe. Ciò consente di definire una regola predefinita per le lingue sconosciute.

La traduzione ID, se abilitata, viene applicata a tutti gli ID che fanno riferimento alle voci del catalogo immagini e del catalogo dei contenuti statici.

## Proprietà {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Uno o più elementi separati da |, dove ogni elemento è costituito da due o più valori stringa separati da virgole. *`locId`* e `locale=` vengono confrontati. Senza distinzione tra maiuscole e minuscole.

## Consultate anche {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Supporto per la localizzazione, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attribute::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
