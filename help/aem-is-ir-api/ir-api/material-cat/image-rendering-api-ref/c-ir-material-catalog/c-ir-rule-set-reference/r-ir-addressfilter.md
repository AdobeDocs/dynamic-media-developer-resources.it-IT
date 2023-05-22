---
description: Elemento filtro indirizzi. Opzionale in <rule> elementi. Sostituisce l'attributo ClientAddressFilter quando viene applicata la regola.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 1%

---

# addressfilter{#addressfilter}

Elemento filtro indirizzi. Opzionale in `<rule>` elementi. Sostituisce l&#39;attributo::ClientAddressFilter quando viene applicata la regola.

## Attributi {#section-e7a0960f7f0045da91de37824aa4aeaa}

Nessuno.

## Dati {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Elenco di indirizzi IP separati da virgole. Ogni indirizzo può includere un suffisso netmask opzionale per consentire la specifica di intervalli di indirizzi IP. Consulta [attribute::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md) per i dettagli.

## Descrizione {#section-099b7839c4be40c68cbff29dad14e7d5}

L&#39;accesso a questo catalogo immagini può essere limitato a uno o più indirizzi IP specifici specificandoli in un `<addressfilter>` elemento. Se l’indirizzo IP del client non corrisponde, viene restituito al client un errore &quot;richiesta rifiutata&quot;.

L’accesso non è limitato se `<addressfilter>` è vuoto o non è specificato.

Se il `<expression>` nel `<rule>` è assente o vuoto, il `<addressfilter>` viene applicato a tutte le richieste.

`localhost` è sempre implicitamente parte del `ClientAddressFilter` definizione, anche se non esplicitamente specificata. Richieste provenienti da `localhost` non vengono mai rifiutati, a prescindere `ClientAddressFilter` specifica.

## Seeaalso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
