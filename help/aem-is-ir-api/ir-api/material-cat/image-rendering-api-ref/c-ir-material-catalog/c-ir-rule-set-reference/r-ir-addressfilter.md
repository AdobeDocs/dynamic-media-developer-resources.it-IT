---
description: Elemento filtro indirizzi. Facoltativo negli elementi <rule> . Sostituisce l'attributo ClientAddressFilter quando la regola viene applicata.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 2%

---


# addressfilter{#addressfilter}

Elemento filtro indirizzi. Facoltativo negli elementi `<rule>`. Sostituisce l&#39;attributo::ClientAddressFilter quando la regola viene applicata.

## Attributi {#section-e7a0960f7f0045da91de37824aa4aeaa}

Nessuno.

## Dati {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Elenco degli indirizzi IP separati da virgole. Ogni indirizzo individuale può includere un suffisso netmask opzionale per consentire la specifica di intervalli di indirizzi IP. Per ulteriori informazioni, vedere ` [attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)` .

## Descrizione {#section-099b7839c4be40c68cbff29dad14e7d5}

L’accesso a questo catalogo immagini può essere limitato a uno o più indirizzi IP specifici specificandoli in un elemento `<addressfilter>` . Se l’indirizzo IP del client non corrisponde, viene restituito al client un errore di &quot;richiesta rifiutata&quot;.

L&#39;accesso non è limitato se `<addressfilter>` è vuoto o non è specificato.

Se l’ `<expression>` nell’elemento `<rule>` è assente o vuoto, il `<addressfilter>` viene applicato a tutte le richieste.

`localhost` fa sempre parte implicita della  `ClientAddressFilter` definizione, anche se non esplicitamente specificata. Le richieste provenienti da `localhost` non vengono mai rifiutate, indipendentemente dalla specifica `ClientAddressFilter`.

## SeeaAltra {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attributo::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
