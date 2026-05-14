---
description: Mappa di traduzione ID. Specifica le regole utilizzate per tradurre gli ID immagine generici in ID specifici per le impostazioni internazionali.
solution: Experience Manager
title: LocaleMap
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c1d74154-721b-46cc-9f0b-8dae5647b179
TQID: 'https://experienceleague.adobe.com/LqHo03WC7EWKP7jt4l1X6kJffXcOQSd8unCxbdjOig4'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 213
ht-degree: 0%

---

# LocaleMap{#localemap}

Mappa di traduzione ID. Specifica le regole utilizzate per tradurre gli ID immagine generici in ID specifici per le impostazioni internazionali.

`*`elemento`*&#42;['|' *`elemento`*]`

<table id="simpletable_A6DD1A28F8ED4178A8ADDB2F3AEFC402"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> elemento</span> </p></td> 
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

`LocaleMap` fa riferimento a un `locId` che può essere mappato a qualsiasi numero di `locSuffix`.

Sono consentiti *`locSuffix`* valori vuoti. I valori *`locSuffix`* devono essere ordinati nell&#39;ordine in cui devono essere cercati. Viene restituita la prima corrispondenza.

Image Server cerca nei valori *`locId`* una corrispondenza senza distinzione tra maiuscole e minuscole con il valore `locale=` specificato nella richiesta. Se viene trovata una corrispondenza, il primo valore *`locSuffix`* associato viene aggiunto all&#39;ID catalogo originale. Se questa voce di catalogo esiste, viene utilizzata, altrimenti viene tentato il successivo valore *`locSuffix`*. Se nessuno dei valori *`locSuffix`* corrisponde a una voce di catalogo, Image Server restituisce un errore o un&#39;immagine predefinita.

Un valore *`locId`* vuoto corrisponde a stringhe `locale=` vuote e sconosciute. Ciò consente di definire una regola predefinita per le lingue sconosciute.

La traduzione ID, se abilitata, viene applicata a tutti gli ID che fanno riferimento alle voci del catalogo immagini e del catalogo dei contenuti statici.

## Proprietà {#section-f4c6f058bc5348ee9a3fb19e394b37e3}

Uno o più elementi separati da |, dove ogni elemento è costituito da due o più valori stringa separati da virgole. *`locId`* e `locale=` vengono confrontati. Senza distinzione tra maiuscole e minuscole.

## Consultate anche {#section-19fba6d5be59439c8bf8ec7513c1a6da}

Supporto localizzazione, [lingua=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-locale.md#reference-8a846b2fbc004a12821b956ed3b25cfb), [attributo::LocaleStrMap](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-localestrmap.md#reference-98c42070a4bc4baf92537132be2b5b1e)
