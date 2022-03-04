---
description: Filtro indirizzo IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.
solution: Experience Manager
title: FiltroIndirizzoClient
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 2%

---

# FiltroIndirizzoClient{#clientaddressfilter}

Filtro indirizzo IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.

Se specificato, le richieste a questo catalogo immagini provenienti da un client con un indirizzo IP non elencato vengono rifiutate. `localhost` fa sempre parte implicitamente del `ClientAddressFilter` definizione, anche se non esplicitamente specificata. Richieste provenienti da `localhost` non vengono mai rifiutati, indipendentemente dal `ClientAddressFilter` specifica.

## Proprietà {#section-21a2992f108d42fb8660c0d65aa61e13}

Elenco di indirizzi IP separati da virgole con maschere di rete opzionali ([Notazione CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation) è utilizzato):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* Indirizzo IP in *[!DNL ddd.ddd.ddd.ddd]* format

* *[!DNL netmask]* maschera netta (0...32)

Questo attributo viene ignorato quando una regola di pre-elaborazione con un `<addressfilter>` viene applicato.

## Predefinito {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Ereditato da `default::AddressFilter` se non definito o se vuoto.

## Esempi {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Nessuna restrizione di accesso: `0.0.0.0/0`
* Concedere l’accesso a tutti gli indirizzi che iniziano con `192: 192.0.0.0/8`
* Concedi l’accesso ai 512 host con indirizzi tra `192.168.12.0` e `192.168.13.255: 192.168.12.0/23`

* Concedere l’accesso a un unico indirizzo IP: `192.168.2.117` o `192.168.2.117/32`

## Consultate anche {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
