---
description: Filtro indirizzo IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.
seo-description: Filtro indirizzo IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 6a557795-0caf-4b5f-974e-fb4c1481a83c
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 2%

---


# ClientAddressFilter{#clientaddressfilter}

Filtro indirizzo IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.

Se specificato, le richieste a questo catalogo di immagini che provengono da un client e che si trova all’indirizzo IP non elencato verranno rifiutate.

## Proprietà {#section-d785265988324af68835410c9ba54147}

Elenco separato da virgole di indirizzi IP con netmask opzionali (è utilizzata la notazione CIDR):

`*`ipAddress`*` `[`/  *`netmask`*`]`*  `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>Indirizzo IP in formato <span class="varname"> ddd.ddd.ddd.ddd</span>. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmask</span> </p></td> 
  <td class="stentry"> <p>Maschera netta (0...32). </p></td> 
 </tr> 
</table>

Questo attributo viene ignorato quando viene applicata una regola di preelaborazione con un elemento `<addressfilter>`.

## Predefinito {#section-de26e8c9225745e985e4beac1f03f4f6}

Ereditato da `default::AddressFilter` se non definito o se vuoto.

## Esempi {#section-a955314d2b6a4213a16c12a8b18d8627}

Nessuna limitazione di accesso: `0.0.0.0/0`

Concedere l&#39;accesso a tutti gli indirizzi a partire dal 1992: `192.0.0.0/8`

Concedi l&#39;accesso ai 512 host con indirizzi compresi tra 192.168.12.0 e 192.168.13.255: `192.168.12.0/23`

Concedere l&#39;accesso a un unico indirizzo IP: `192.168.2.117` o `192.168.2.117/32`

## Consultate anche {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
