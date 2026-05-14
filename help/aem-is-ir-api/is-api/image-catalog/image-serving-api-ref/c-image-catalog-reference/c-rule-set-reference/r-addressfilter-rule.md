---
description: Elemento filtro indirizzi. Facoltativo negli elementi <rule> e <pathrule>.
solution: Experience Manager
title: addressfilter
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fe5df3a8-c9b2-4fad-ab9f-ca0b06016faf
TQID: 'https://experienceleague.adobe.com/NkzpvFZFbluayVtCa7qBVcSgY2aU5N7R2-rZkQCZHkw'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 121
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
