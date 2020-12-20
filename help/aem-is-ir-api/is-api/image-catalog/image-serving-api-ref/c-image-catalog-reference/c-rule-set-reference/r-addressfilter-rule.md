---
description: Elemento filtro indirizzo. Facoltativo negli elementi <rule> e <pathrule>.
seo-description: Elemento filtro indirizzo. Facoltativo negli elementi <rule> e <pathrule>.
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
topic: Scene7 Image Serving - Image Rendering API
uuid: 677eb19f-fd1a-4f74-8d55-6045baf01bf5
translation-type: tm+mt
source-git-commit: 4439103ccd0d63afdd9ec20bd475560e8f84dcba
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 4%

---


# addressfilter{#addressfilter}

Elemento filtro indirizzo. Facoltativo negli elementi `<rule>` e `<pathrule>`.

Sostituisce `attribute::ClientAddressFilter` quando la regola viene applicata.

## Attributi {#section-31e9ad29e9934933ac154bccbc729172}

Nessuno.

## Dati {#section-c762bdfe425140d689ea5abf25e9a48a}

Elenco degli indirizzi IP separati da virgole. Ogni singolo indirizzo può includere un suffisso di netmask facoltativo per consentire la specifica degli intervalli di indirizzi IP. Vedere `attribute::ClientAddressFilter` per informazioni dettagliate.

## Descrizione {#section-d561b2485e004ef8a2085997d0f4bca6}

L&#39;accesso a questo catalogo immagini può essere limitato a uno o più indirizzi IP client specifici specificandoli in un elemento `<addressfilter>`. Se l&#39;indirizzo IP del client non corrisponde, viene restituito al client un errore &quot;richiesta rifiutata&quot;.

L&#39;accesso non è limitato se `<addressfilter>` è vuoto o non è specificato.

Se la `<expression>` nell&#39;elemento `<rule>` è assente o vuota, la `<addressfilter>` viene applicata a tutte le richieste.

## Consultate anche {#section-6f51ec2218d9450bb7642f9fdad1988a}

[attributo::ClientAddressFilter](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-clientaddressfilter.md#reference-7000c1f77b134462a1f06b733f29ba68)
