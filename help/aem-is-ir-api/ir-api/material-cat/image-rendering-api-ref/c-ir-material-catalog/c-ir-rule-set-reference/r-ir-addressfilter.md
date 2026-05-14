---
description: Elemento filtro indirizzi. Facoltativo negli elementi <rule>. Sostituisce l'attributo ClientAddressFilter quando viene applicata la regola.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0da9299b-fe14-4a69-8567-2d79ad2ce0bd
TQID: 'https://experienceleague.adobe.com/583zFF80AMZnaF4C-RQpRQI684hRlPRCuwoMPHGJ6eg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 150
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
