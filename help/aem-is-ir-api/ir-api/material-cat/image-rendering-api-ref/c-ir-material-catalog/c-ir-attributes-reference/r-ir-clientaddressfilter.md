---
description: Filtro indirizzo IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.
seo-description: Filtro indirizzo IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.
seo-title: ClientAddressFilter
solution: Experience Manager
title: ClientAddressFilter
topic: Scene7 Image Serving - Image Rendering API
uuid: b68f527b-7fa7-43e3-9517-57a6c3700b06
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 2%

---


# ClientAddressFilter{#clientaddressfilter}

Filtro indirizzo IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.

Se specificato, le richieste a questo catalogo di immagini che provengono da un client e che si trova all’indirizzo IP non elencato verranno rifiutate. `localhost` fa sempre parte implicitamente della  `ClientAddressFilter` definizione, anche se non esplicitamente specificata. Le richieste provenienti da `localhost` non vengono mai rifiutate, indipendentemente dalla specifica `ClientAddressFilter`.

## Proprietà {#section-21a2992f108d42fb8660c0d65aa61e13}

Elenco separato da virgole di indirizzi IP con netmask opzionali ([Notazione CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* *[!DNL ipAddress]* Indirizzo IP in  *[!DNL ddd.ddd.ddd.ddd]* formato

* *[!DNL netmask]* maschera di rete (0...32)

Questo attributo viene ignorato quando viene applicata una regola di pre-elaborazione con un elemento `<addressfilter>`.

## Predefinito {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Ereditato da `default::AddressFilter` se non definito o se vuoto.

## Esempi {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Nessuna limitazione di accesso: `0.0.0.0/0`
* Concedere l&#39;accesso a tutti gli indirizzi a partire da `192: 192.0.0.0/8`
* Concedere l&#39;accesso ai 512 host con indirizzi compresi tra `192.168.12.0` e `192.168.13.255: 192.168.12.0/23`

* Concedere l&#39;accesso a un unico indirizzo IP: `192.168.2.117` o `192.168.2.117/32`

## Consultate anche {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
