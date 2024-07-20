---
title: FiltroIndirizzoClient
description: Filtro indirizzi IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 24046950-1dba-4352-a549-43994e799748
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 2%

---

# FiltroIndirizzoClient{#clientaddressfilter}

Filtro indirizzi IP client. Consente di specificare uno o più indirizzi IP o intervalli di indirizzi.

Se specificato, le richieste a questo catalogo immagini generate da un client non presente nell&#39;elenco degli indirizzi IP vengono rifiutate. `localhost` fa sempre parte implicitamente della definizione di `ClientAddressFilter`, anche se non specificato in modo esplicito. Le richieste provenienti da `localhost` non vengono mai rifiutate, indipendentemente dalla specifica `ClientAddressFilter`.

## Proprietà {#section-21a2992f108d42fb8660c0d65aa61e13}

Elenco di indirizzi IP separati da virgole con netmask facoltative ([viene utilizzata la notazione CIDR](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing#CIDR_notation)):

` *[!DNL ipAddress]*[/ *[!DNL netmask]*]&#42;[, *[!DNL ipAddress]*[/ *[!DNL netmask]*]]`

* Indirizzo IP *[!DNL ipAddress]* in formato *[!DNL ddd.ddd.ddd.ddd]*

* *[!DNL netmask]* maschera di rete (0...32)

Questo attributo viene ignorato quando viene applicata una regola di pre-elaborazione con un elemento `<addressfilter>`.

## Predefinito {#section-beddaa18ed6c4f3ba1eb2d4471267712}

Ereditato da `default::AddressFilter` se non definito o se vuoto.

## Esempi {#section-72b4a3615bff4a5f8b03d83c6489aaba}

* Nessuna restrizione di accesso: `0.0.0.0/0`
* Concedi l&#39;accesso a tutti gli indirizzi che iniziano con `192: 192.0.0.0/8`
* Concedi l&#39;accesso ai 512 host con indirizzi compresi tra `192.168.12.0` e `192.168.13.255: 192.168.12.0/23`

* Concedi l&#39;accesso a un singolo indirizzo IP: `192.168.2.117` o `192.168.2.117/32`

## Consultate anche {#section-6198780c7b3045aabd211eefb38bc565}

[addressfilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
