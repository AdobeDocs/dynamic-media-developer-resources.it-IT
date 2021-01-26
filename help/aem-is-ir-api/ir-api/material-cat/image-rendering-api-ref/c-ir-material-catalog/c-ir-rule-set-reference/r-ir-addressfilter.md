---
description: Elemento filtro indirizzo. Facoltativo negli elementi <rule>. Sostituisce l'attributo ClientAddressFilter quando la regola viene applicata.
seo-description: Elemento filtro indirizzo. Facoltativo negli elementi <rule>. Sostituisce l'attributo ClientAddressFilter quando la regola viene applicata.
seo-title: addressfilter
solution: Experience Manager
title: addressfilter
topic: Dynamic Media Image Serving - Image Rendering API
uuid: e5702c6e-a49c-4da6-a29c-26e16bfdcad1
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# addressfilter{#addressfilter}

Elemento filtro indirizzo. Facoltativo negli elementi `<rule>`. Sostituisce attributo::ClientAddressFilter quando la regola viene applicata.

## Attributi {#section-e7a0960f7f0045da91de37824aa4aeaa}

Nessuno.

## Dati {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Elenco degli indirizzi IP separati da virgole. Ogni singolo indirizzo può includere un suffisso di netmask facoltativo per consentire la specifica degli intervalli di indirizzi IP. Vedere ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` per informazioni dettagliate.

## Descrizione {#section-099b7839c4be40c68cbff29dad14e7d5}

L&#39;accesso a questo catalogo immagini può essere limitato a uno o più indirizzi IP specifici specificandoli in un elemento `<addressfilter>`. Se l&#39;indirizzo IP del client non corrisponde, viene restituito al client un errore &quot;richiesta rifiutata&quot;.

L&#39;accesso non è limitato se `<addressfilter>` è vuoto o non è specificato.

Se la `<expression>` nell&#39;elemento `<rule>` è assente o vuota, la `<addressfilter>` viene applicata a tutte le richieste.

`localhost` fa sempre parte implicitamente della  `ClientAddressFilter` definizione, anche se non esplicitamente specificata. Le richieste provenienti da `localhost` non vengono mai rifiutate, indipendentemente dalla specifica `ClientAddressFilter`.

## SeeaAltra {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attributo::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
