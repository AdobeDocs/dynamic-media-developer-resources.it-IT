---
description: Elemento filtro indirizzi. Facoltativo negli elementi <rule>. Sostituisce l'attributo ClientAddressFilter quando viene applicata la regola.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---

# addressfilter{#addressfilter}

Elemento filtro indirizzi. Facoltativo negli elementi `<rule>`. Sostituisce l&#39;attributo::ClientAddressFilter quando viene applicata la regola.

## Attributi {#section-e7a0960f7f0045da91de37824aa4aeaa}

Nessuno.

## Dati {#section-eb138f192516418a9ef2ab9a38c9ee9e}

Elenco di indirizzi IP separati da virgole. Ogni indirizzo può includere un suffisso netmask opzionale per consentire la specifica di intervalli di indirizzi IP. Per ulteriori informazioni, vedere [attribute::ClientAddressFilter](/help/aem-is-ir-api/ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md).

## Descrizione {#section-099b7839c4be40c68cbff29dad14e7d5}

L&#39;accesso a questo catalogo immagini può essere limitato a uno o più indirizzi IP specifici specificandoli in un elemento `<addressfilter>`. Se l’indirizzo IP del client non corrisponde, viene restituito al client un errore &quot;richiesta rifiutata&quot;.

L&#39;accesso non è limitato se `<addressfilter>` è vuoto o non è specificato.

Se `<expression>` nell&#39;elemento `<rule>` è assente o vuoto, `<addressfilter>` viene applicato a tutte le richieste.

`localhost` fa sempre parte implicitamente della definizione di `ClientAddressFilter`, anche se non specificato in modo esplicito. Le richieste provenienti da `localhost` non vengono mai rifiutate, indipendentemente dalla specifica `ClientAddressFilter`.

## Seeaalso {#section-02056065e0c042e1b155b2f3e5b84ef7}

[attribute::ClientAddressFilter](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-clientaddressfilter.md#reference-52a541cec0b0424faf263d1fb4946b5f)
