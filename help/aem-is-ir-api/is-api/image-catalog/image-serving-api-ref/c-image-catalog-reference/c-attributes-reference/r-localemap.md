---
description: Mappa di traduzione ID. Specifica le regole utilizzate per tradurre gli ID immagine generici in ID specifici per le impostazioni internazionali.
seo-description: Mappa di traduzione ID. Specifica le regole utilizzate per tradurre gli ID immagine generici in ID specifici per le impostazioni internazionali.
seo-title: Mappa lingua
solution: Experience Manager
title: Mappa lingua
topic: Scene7 Image Serving - Image Rendering API
uuid: 3609a595-2948-43a4-ba8c-fd1a9ea4e26e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Mappa lingua{#localemap}

Mappa di traduzione ID. Specifica le regole utilizzate per tradurre gli ID immagine generici in ID specifici per le impostazioni internazionali.

` *``*&#42;['|' *`item`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> item</span> </p></td> 
  <td class="stentry"> <p><span class="varname"> locId</span>,<span class="varname"> locSuffix</span>*[','<span class="varname"> locSuffix</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locId</span> </p></td> 
  <td class="stentry"> <p>ID lingua (senza distinzione tra maiuscole e minuscole). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> locSuffix</span> </p></td> 
  <td class="stentry"> <p>Suffisso delle impostazioni internazionali. </p></td> 
 </tr> 
</table>

`LocaleMap` si riferisce a un `locId` oggetto che può essere mappato a qualsiasi numero di `locSuffix`.

Empty *`locSuffix`* values are permitted. *`locSuffix`* i valori devono essere ordinati nell&#39;ordine in cui devono essere cercati. Viene restituita la prima corrispondenza.

Image Server cerca nei *`locId`* valori una corrispondenza senza distinzione tra maiuscole e minuscole con il `locale=` valore specificato nella richiesta. Se viene trovata una corrispondenza, il primo *`locSuffix`* valore associato viene aggiunto all’ID catalogo originale. Se esiste già, viene utilizzato, altrimenti viene provato il *`locSuffix`* valore successivo. Se nessuno dei *`locSuffix`* valori corrisponde a una voce di catalogo, Image Server restituisce un errore o un&#39;immagine predefinita.

Un *`locId`* valore vuoto corrisponde a stringhe vuote e sconosciute `locale=` . Questo consente di definire una regola predefinita per le lingue sconosciute.

Quando abilitata, la traduzione ID viene applicata a tutti gli ID che fanno riferimento a voci di catalogo immagini e di catalogo di contenuti statici.

## Proprietà {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Uno o più elementi, separati da|, in cui ogni elemento è costituito da due o più valori stringa separati da virgole. *`locId`* e `locale=` vengono confrontati. Senza distinzione tra maiuscole e minuscole.

## Consultate anche {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Supporto per la localizzazione, [locale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attributo::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
