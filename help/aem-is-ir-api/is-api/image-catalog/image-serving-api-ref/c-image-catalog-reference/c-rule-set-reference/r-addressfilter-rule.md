---
description: Elemento filtro indirizzi. Facoltativo negli elementi <rule> e <pathrule> .
seo-description: Elemento filtro indirizzi. Facoltativo negli elementi <rule> e <pathrule> .
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 4%

---


# addressfilter{#addressfilter}

Elemento filtro indirizzi. Facoltativo negli elementi `<rule>` e `<pathrule>`.

Sostituisce `attribute::ClientAddressFilter` quando la regola viene applicata.

## Attributi {#section-31e9ad29e9934933ac154bccbc729172}

Nessuno.

## Dati {#section-c762bdfe425140d689ea5abf25e9a48a}

Elenco degli indirizzi IP separati da virgole. Ogni indirizzo individuale può includere un suffisso netmask opzionale per consentire la specifica di intervalli di indirizzi IP. Per ulteriori informazioni, vedere `attribute::ClientAddressFilter` .

## Descrizione {#section-d561b2485e004ef8a2085997d0f4bca6}

L’accesso a questo catalogo immagini può essere limitato a uno o più indirizzi IP client specifici specificandoli in un elemento `<addressfilter>` . Se l’indirizzo IP del client non corrisponde, viene restituito al client un errore di &quot;richiesta rifiutata&quot;.

L&#39;accesso non è limitato se `<addressfilter>` è vuoto o non è specificato.

Se l’ `<expression>` nell’elemento `<rule>` è assente o vuoto, il `<addressfilter>` viene applicato a tutte le richieste.

## Consultate anche {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attributo::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
