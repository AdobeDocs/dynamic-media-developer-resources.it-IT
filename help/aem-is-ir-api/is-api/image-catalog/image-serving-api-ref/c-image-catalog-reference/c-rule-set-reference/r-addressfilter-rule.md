---
description: Elemento filtro indirizzi. Facoltativo negli elementi <rule> e <pathrule>.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 2%

---

# addressfilter{#addressfilter}

Elemento filtro indirizzi. Facoltativo negli elementi `<rule>` e `<pathrule>`.

Sostituisce `attribute::ClientAddressFilter` quando la regola viene applicata.

## Attributi {#section-31e9ad29e9934933ac154bccbc729172}

Nessuno.

## Dati {#section-c762bdfe425140d689ea5abf25e9a48a}

Elenco di indirizzi IP separati da virgole. Ogni indirizzo può includere un suffisso netmask opzionale per consentire la specifica di intervalli di indirizzi IP. Per i dettagli, vedere `attribute::ClientAddressFilter`.

## Descrizione {#section-d561b2485e004ef8a2085997d0f4bca6}

L&#39;accesso a questo catalogo immagini può essere limitato a uno o più indirizzi IP client specifici specificandoli in un elemento `<addressfilter>`. Se l’indirizzo IP del client non corrisponde, viene restituito al client un errore &quot;richiesta rifiutata&quot;.

L&#39;accesso non è limitato se `<addressfilter>` è vuoto o non è specificato.

Se `<expression>` nell&#39;elemento `<rule>` è assente o vuoto, `<addressfilter>` viene applicato a tutte le richieste.

## Consultate anche {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attribute::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
