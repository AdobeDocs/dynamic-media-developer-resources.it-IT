---
description: Filtro indirizzi IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.
solution: Experience Manager
title: FiltroIndirizzoClient
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 028cef35-2862-452c-872c-b953e8ccb195
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 2%

---

# FiltroIndirizzoClient{#clientaddressfilter}

Filtro indirizzi IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.

Se specificato, le richieste a questo catalogo immagini provenienti da un client che si trova in un indirizzo IP non elencato vengono rifiutate.

## Proprietà {#section-d785265988324af68835410c9ba54147}

Elenco di indirizzi IP separati da virgole con maschere di rete facoltative (viene utilizzata la notazione CIDR):

`*`ipAddress`*` `[`/ *`netmask`*`]`&#42; `[`,*`ipAddress`*`[`/*`netmask`*`]]`

<table id="simpletable_9F82BB0D42A9434883F2F70A2A92898C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> ipAddress</span> </p> </td> 
  <td class="stentry"> <p>Indirizzo IP in <span class="varname"> ddd.ddd.ddd.ddd</span> formato. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> netmask</span> </p></td> 
  <td class="stentry"> <p>Maschera di rete (0...32). </p></td> 
 </tr> 
</table>

Questo attributo viene ignorato quando una regola di preelaborazione con un `<addressfilter>` viene applicato.

## Predefinito {#section-de26e8c9225745e985e4beac1f03f4f6}

Ereditato da `default::AddressFilter` se non è definita o se è vuota.

## Esempi {#section-a955314d2b6a4213a16c12a8b18d8627}

Nessuna restrizione di accesso: `0.0.0.0/0`

Concedi l’accesso a tutti gli indirizzi a partire da 192: `192.0.0.0/8`

Concedi l’accesso ai 512 host con indirizzi compresi tra 192.168.12.0 e 192.168.13.255: `192.168.12.0/23`

Concedi l’accesso a un singolo indirizzo IP: `192.168.2.117` o `192.168.2.117/32`

## Consultate anche {#section-4ea89a7d82e14a4a800487d2d8801465}

[addressfilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/r-addressfilter-rule.md#reference-48c369f56ecd4034b410da5a94a9dfd1)
