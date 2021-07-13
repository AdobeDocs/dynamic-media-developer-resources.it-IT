---
description: Abilita le intestazioni di risposta modificate più di recente. Abilita o disabilita l’inclusione dell’intestazione Last-Modified nelle risposte HTTP memorizzabili nella cache emesse da Image Serving.
solution: Experience Manager
title: UseLastModified
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 4908da5d-636e-44d2-bd49-40e01c8b5f79
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 1%

---

# UseLastModified{#uselastmodified}

Abilita le intestazioni di risposta modificate più di recente. Abilita o disabilita l’inclusione dell’intestazione Last-Modified nelle risposte HTTP memorizzabili nella cache emesse da Image Serving.

Il server utilizza il valore `catalog::TimeStamp` più recente di tutti i cataloghi/record di catalogo interessati da una risposta come valore di intestazione Last-Modified .

Deve essere attivato solo se viene utilizzata una rete di caching distribuita o un altro sistema di caching che non supporta le intestazioni dei tag.

>[!NOTE]
>
>Presta attenzione quando utilizzi le intestazioni Last-Modified in un ambiente con bilanciamento del carico che coinvolge più host Image Server. La memorizzazione in cache del client potrebbe essere ignorata e il caricamento del server potrebbe aumentare se per qualche motivo i server dispongono di timestamp diversi per le stesse voci di catalogo. Tale situazione può verificarsi come segue:
>
>* Né `catalog::TimeStamp` né `attribute::TimeStamp`, in modo che il tempo di modifica del file [!DNL catalog.ini] sia utilizzato come impostazione predefinita per `catalog::TimeStamp`.
   >
   >
* Invece di condividere i file di catalogo delle immagini tramite un montaggio di rete, ogni server ha la propria istanza dei file di catalogo su un file system locale.
>* Due o più istanze dello stesso file [!DNL catalog.ini] hanno date di modifica diverse, probabilmente a causa di una copia impropria dei file.

>



## Proprietà {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Bandiera. 0 per disabilitare, 1 per abilitare le intestazioni HTTP Last-Modified.

## Predefinito {#section-4eb47aadab8b41609bef296a4115f9f4}

Ereditato da `default::UseLastModified` se non definito o se vuoto.

## Consultate anche {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
