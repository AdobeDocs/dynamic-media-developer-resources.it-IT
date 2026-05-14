---
description: Durata predefinita cache client. Specifica un intervallo di scadenza predefinito se un record catalogo non contiene un valore Expiration valido per il catalogo.
solution: Experience Manager
title: Scade
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c9dccf8d-56b3-4608-ac05-9c17babc609e
TQID: 'https://experienceleague.adobe.com/NkQ-Bj-gHGksaD4Tmt7k8fYVEYfe67ACo4oWS25dKOE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 124
ht-degree: 2%

---

# Scade{#expiration}

Durata predefinita cache client. Specifica un intervallo di scadenza predefinito nel caso in cui un record catalogo non contenga un valore catalog::Expiration valido.

## Proprietà {#section-063be3b2f13a48a3a5ab8080718e9812}

Numero reale, 0 o superiore. Numero di ore mancanti alla scadenza dalla generazione dei dati di risposta. Impostate questo valore su 0 per far scadere immediatamente l&#39;immagine di risposta, disattivando di fatto la memorizzazione in cache del client. Imposta su -1 per contrassegnare come `never expire`.

## Predefinito {#section-f55308b195c04083996f6717c8537634}

Ereditato da `default::Expiration` se non definito o se vuoto.

TTL (Time-To-Live) è la durata prima della scadenza della cache. Il valore TTL predefinito è 10 ore.

## Consultate anche {#section-b2411d99ddb14115ad475d506efd8967}

[catalogo::Expiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-expiration-cat.md#reference-a7afd668ecbb4d2da65d86259aa6a28a) , [attributo::DefaultExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-defaultexpiration.md#reference-0526166fab654fceb243b75d1ea4f0cf), [attributo::NonImgExpiration](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-nonimgexpiration.md#reference-a8066cd0d24b4ea98100ade4821f1f9d)
