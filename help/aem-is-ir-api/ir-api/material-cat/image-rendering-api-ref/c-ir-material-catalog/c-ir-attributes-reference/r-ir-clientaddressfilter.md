---
description: Filtro indirizzo IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.
solution: Experience Manager
title: FiltroIndirizzoClient
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 2%

---


# ClientAddressFilter{#clientaddressfilter}

Filtro indirizzo IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.

Se specificato, le richieste a questo catalogo immagini provenienti da un client con un indirizzo IP non elencato verranno rifiutate. `localhost` fa sempre parte implicita della  `ClientAddressFilter` definizione, anche se non esplicitamente specificata. Le richieste provenienti da `localhost` non vengono mai rifiutate, indipendentemente dalla specifica `ClientAddressFilter`.

## Proprietà {#section-21a2992f108d42fb8660c0d65aa61e13}

Elenco di indirizzi IP separati da virgole con maschere di rete facoltative ([Notazione CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* Indirizzo IP in  *[!DNL ddd.ddd.ddd.ddd]* formato

* *[!DNL netmask]* maschera netta (0...32)

Questo attributo viene ignorato quando viene applicata una regola di pre-elaborazione con un elemento `<addressfilter>` .

## Predefinito {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Ereditato da `default::AddressFilter` se non definito o se vuoto.

## Esempi {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Nessuna restrizione di accesso: `0.0.0.0/0`
* Concedi l’accesso a tutti gli indirizzi che iniziano con `192: 192.0.0.0/8`
* Concedi l’accesso ai 512 host con indirizzi compresi tra `192.168.12.0` e `192.168.13.255: 192.168.12.0/23`

* Concedere l’accesso a un unico indirizzo IP: `192.168.2.117` o `192.168.2.117/32`

## Consultate anche {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
