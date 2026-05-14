---
title: UseLastModified
description: Abilita le intestazioni di risposta dell’ultima modifica. Abilita o disabilita l'inclusione dell'intestazione Last-Modified nelle risposte HTTP memorizzabili nella cache emesse da Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 31dfbc55-0efd-417b-be4a-67c878772388
TQID: 'https://experienceleague.adobe.com/X-d-02WckbxVyDxRvZDIcOghkk8Z8yYbGOZ3Aigx4ts'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Abilita le intestazioni di risposta dell’ultima modifica. Abilita o disabilita l&#39;inclusione dell&#39;intestazione Last-Modified nelle risposte HTTP memorizzabili nella cache emesse da Image Rendering.

Il server utilizza come valore di intestazione Ultima modifica i valori `vignette::TimeStamp` e `catalog::TimeStamp` più recenti di tutti i cataloghi/record di catalogo di vignettatura e materiali coinvolti in una risposta.

Deve essere abilitato solo se si utilizza una rete di caching distribuito, come Akamai, che non supporta le intestazioni etag.

>[!NOTE]
>
>Presta attenzione quando utilizzi le intestazioni Last-Modified in un ambiente con carico bilanciato che coinvolge più host Image Server/Rendering. La memorizzazione nella cache del client può essere annullata e il carico del server può aumentare se per qualche motivo i server hanno marche temporali diverse per le stesse voci di catalogo. Tale situazione può verificarsi nel modo seguente:

* `catalog::TimeStamp`, `vignette::TimeStamp` o `attribute::TimeStamp` non è definito, pertanto l&#39;ora di modifica del file [!DNL catalog.ini] viene utilizzata come predefinita per `catalog::TimeStamp`.

* Anziché condividere i file di catalogo dei materiali tramite un montaggio di rete, ogni server dispone di una propria istanza dei file di catalogo in un file system locale.
* Due o più istanze dello stesso file [!DNL catalog.ini] hanno date di modifica del file diverse, probabilmente causate da una copia non corretta dei file.

## Proprietà {#section-453952244193452caccfaf7f601007c1}

Bandiera. 0 per disabilitare, 1 per abilitare le intestazioni HTTP Last-Modified.

## Predefinito {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Ereditato da `default::UseLastModified` se non definito o se vuoto.

## Consultate anche {#section-1536715169da48b0aecc4ab7326c86db}

[catalogo::Timestamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignettatura::Timestamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
