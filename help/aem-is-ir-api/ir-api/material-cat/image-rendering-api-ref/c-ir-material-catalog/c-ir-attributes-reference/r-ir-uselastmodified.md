---
description: Abilitare le intestazioni di risposta modificate per l’ultima volta. Abilita o disabilita l’inclusione dell’intestazione Ultima modifica nelle risposte HTTP memorizzabili nella cache emesse dal rendering immagine.
seo-description: Abilitare le intestazioni di risposta modificate per l’ultima volta. Abilita o disabilita l’inclusione dell’intestazione Ultima modifica nelle risposte HTTP memorizzabili nella cache emesse dal rendering immagine.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 1%

---


# UseLastModified{#uselastmodified}

Abilitare le intestazioni di risposta modificate per l’ultima volta. Abilita o disabilita l’inclusione dell’intestazione Ultima modifica nelle risposte HTTP memorizzabili nella cache emesse dal rendering immagine.

Il server utilizza il valore più recente `vignette::TimeStamp` e `catalog::TimeStamp` di tutti i cataloghi di vignettature e materiali/record di cataloghi coinvolti in una risposta come valore dell&#39;intestazione Ultima modifica.

Deve essere attivato solo se viene utilizzata una rete di caching distribuito, come Akamai, che non supporta le intestazioni dei tag.

>[!NOTE]
>
>Prestate attenzione quando usate le intestazioni Ultima modifica in un ambiente con bilanciamento del carico che coinvolge più host Image Serving/Rendering. Il caching dei client potrebbe essere ignorato e il caricamento del server potrebbe aumentare se per qualche motivo i server dispongono di timestamp diversi per le stesse voci di catalogo. Tale situazione può verificarsi come segue:

* Non è definito né `catalog::TimeStamp`, `vignette::TimeStamp`, né `attribute::TimeStamp`, in modo che il tempo di modifica del file [!DNL catalog.ini] sia utilizzato come impostazione predefinita per `catalog::TimeStamp`.

* Anziché condividere i file del catalogo dei materiali tramite un montaggio di rete, ogni server dispone di una propria istanza dei file del catalogo in un file system locale.
* Due o più istanze dello stesso file [!DNL catalog.ini] hanno date di modifica diverse, probabilmente causate da una copia non corretta dei file.

## Proprietà {#section-453952244193452caccfaf7f601007c1}

Flag. 0 per disattivare, 1 per abilitare le intestazioni HTTP Ultima modifica.

## Predefinito {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Ereditato da `default::UseLastModified` se non definito o se vuoto.

## Consultate anche {#section-1536715169da48b0aecc4ab7326c86db}

[catalogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) ,  [vignettatura::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
