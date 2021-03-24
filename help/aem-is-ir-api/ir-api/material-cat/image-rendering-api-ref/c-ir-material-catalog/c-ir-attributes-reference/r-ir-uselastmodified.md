---
description: Abilita le intestazioni di risposta modificate più di recente. Abilita o disabilita l’inclusione dell’intestazione Last-Modified nelle risposte HTTP memorizzabili nella cache emesse da Image Rendering.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

Abilita le intestazioni di risposta modificate più di recente. Abilita o disabilita l’inclusione dell’intestazione Last-Modified nelle risposte HTTP memorizzabili nella cache emesse da Image Rendering.

Il server utilizza il valore `vignette::TimeStamp` e `catalog::TimeStamp` più recente di tutte le vignette e di tutti i cataloghi di materiali/record di catalogo coinvolti in una risposta come valore dell&#39;intestazione Last-Modified.

Deve essere abilitato solo se viene utilizzata una rete di caching distribuita, come Akamai, che non supporta le intestazioni etag.

>[!NOTE]
>
>Presta attenzione quando utilizzi le intestazioni Last-Modified in un ambiente con bilanciamento del carico che coinvolge più host Image Serving/Rendering. La memorizzazione in cache del client potrebbe essere ignorata e il caricamento del server potrebbe aumentare se per qualche motivo i server dispongono di timestamp diversi per le stesse voci di catalogo. Tale situazione può verificarsi come segue:

* Né `catalog::TimeStamp`, `vignette::TimeStamp`, né `attribute::TimeStamp` sono definiti, in modo che l&#39;ora di modifica del file [!DNL catalog.ini] sia utilizzata come impostazione predefinita per `catalog::TimeStamp`.

* Invece di condividere i file di catalogo del materiale tramite un montaggio di rete, ogni server ha la propria istanza dei file di catalogo su un file system locale.
* Due o più istanze dello stesso file [!DNL catalog.ini] hanno date di modifica diverse, probabilmente a causa di una copia impropria dei file.

## Proprietà {#section-453952244193452caccfaf7f601007c1}

Bandiera. 0 per disabilitare, 1 per abilitare le intestazioni HTTP Last-Modified.

## Predefinito {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Ereditato da `default::UseLastModified` se non definito o se vuoto.

## Consultate anche {#section-1536715169da48b0aecc4ab7326c86db}

[catalogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vignetta::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
