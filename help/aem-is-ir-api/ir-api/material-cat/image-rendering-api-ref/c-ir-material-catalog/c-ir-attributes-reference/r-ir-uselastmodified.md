---
description: Abilitare le intestazioni di risposta modificate per l’ultima volta. Abilita o disabilita l’inclusione dell’intestazione Ultima modifica nelle risposte HTTP memorizzabili nella cache emesse dal rendering immagine.
seo-description: Abilitare le intestazioni di risposta modificate per l’ultima volta. Abilita o disabilita l’inclusione dell’intestazione Ultima modifica nelle risposte HTTP memorizzabili nella cache emesse dal rendering immagine.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: f2ce2e04-4133-40af-ac82-cae57b253fe9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

Abilitare le intestazioni di risposta modificate per l’ultima volta. Abilita o disabilita l’inclusione dell’intestazione Ultima modifica nelle risposte HTTP memorizzabili nella cache emesse dal rendering immagine.

Il server utilizza come valore dell’intestazione Ultima modifica tutti i cataloghi di vignettatura `vignette::TimeStamp` e materiali o i record di cataloghi coinvolti in una risposta il valore più recente `catalog::TimeStamp` e il valore più recente.

Deve essere attivato solo se viene utilizzata una rete di caching distribuito, come Akamai, che non supporta le intestazioni dei tag.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>Prestate attenzione quando usate le intestazioni Ultima modifica in un ambiente con bilanciamento del carico che coinvolge più host Image Serving/Rendering. Il caching dei client potrebbe essere ignorato e il caricamento del server potrebbe aumentare se per qualche motivo i server dispongono di timestamp diversi per le stesse voci di catalogo. Tale situazione può verificarsi come segue:

* Né `catalog::TimeStamp``vignette::TimeStamp`, né `attribute::TimeStamp` è definito, in modo che il tempo di modifica del [!DNL catalog.ini] file venga utilizzato come impostazione predefinita per `catalog::TimeStamp`.

* Anziché condividere i file del catalogo dei materiali tramite un montaggio di rete, ogni server dispone di una propria istanza dei file del catalogo in un file system locale.
* Due o più istanze dello stesso [!DNL catalog.ini] file hanno date di modifica del file diverse, probabilmente causate da una copia non corretta dei file.

## Proprietà {#section-453952244193452caccfaf7f601007c1}

Flag. 0 per disattivare, 1 per abilitare le intestazioni HTTP Ultima modifica.

## Predefinito {#section-ec8fae847ca2421d8cdcde324e5a2d76}

Ereditato da `default::UseLastModified` se non definito o se vuoto.

## Consultate anche {#section-1536715169da48b0aecc4ab7326c86db}

[catalogo::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-material-data-reference/r-ir-timestamp-dataref.md#reference-6daf7973dc4f4b4e9e8165756db7c319) , [vignettatura::TimeStamp](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-vignette-map-reference/r-ir-timestamp-vignette.md#reference-d57cdd40a6a645d199dbb1d56cc85bc1)
