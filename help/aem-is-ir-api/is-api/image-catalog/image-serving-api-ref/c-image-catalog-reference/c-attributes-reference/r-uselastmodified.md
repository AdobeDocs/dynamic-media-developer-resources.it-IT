---
description: Abilitare le intestazioni di risposta modificate per l’ultima volta. Abilita o disabilita l’inclusione dell’intestazione Ultima modifica nelle risposte HTTP memorizzabili nella cache emesse da Image Server.
seo-description: Abilitare le intestazioni di risposta modificate per l’ultima volta. Abilita o disabilita l’inclusione dell’intestazione Ultima modifica nelle risposte HTTP memorizzabili nella cache emesse da Image Server.
seo-title: UseLastModified
solution: Experience Manager
title: UseLastModified
topic: Scene7 Image Serving - Image Rendering API
uuid: 9dae4f15-4323-4f68-917f-6d72ae52c753
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# UseLastModified{#uselastmodified}

Abilitare le intestazioni di risposta modificate per l’ultima volta. Abilita o disabilita l’inclusione dell’intestazione Ultima modifica nelle risposte HTTP memorizzabili nella cache emesse da Image Server.

Il server utilizza il `catalog::TimeStamp` valore più recente di tutti i cataloghi/record di catalogo coinvolti in una risposta come valore dell’intestazione Ultima modifica.

Deve essere attivato solo se viene utilizzata una rete di caching distribuito o un altro sistema di caching che non supporta le intestazioni dei tag.

>[!NOTE]
>
>Prestate attenzione quando usate le intestazioni Ultima modifica in un ambiente con bilanciamento del carico che coinvolge più host Image Server. Il caching dei client potrebbe essere ignorato e il caricamento del server potrebbe aumentare se per qualche motivo i server dispongono di timestamp diversi per le stesse voci di catalogo. Tale situazione può verificarsi come segue:
>
>* Né `catalog::TimeStamp` né `attribute::TimeStamp`, in modo che il tempo di modifica del [!DNL catalog.ini] file venga utilizzato come impostazione predefinita per `catalog::TimeStamp`.
   >
   >
* Anziché condividere i file del catalogo immagini tramite un sistema di rete, ogni server dispone di una propria istanza dei file del catalogo su un file system locale.
>* Due o più istanze dello stesso [!DNL catalog.ini] file hanno date di modifica del file diverse, probabilmente causate da una copia non corretta dei file.
>



## Proprietà {#section-7e26009b7d0a4a3ab234bf2a37f599e0}

Flag. 0 per disattivare, 1 per abilitare le intestazioni HTTP Ultima modifica.

## Predefinito {#section-4eb47aadab8b41609bef296a4115f9f4}

Ereditato da `default::UseLastModified` se non definito o se vuoto.

## Consultate anche {#section-4211a78f8a5b45629c62fed5ae82f1cb}

[catalogo::TimeStamp](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-image-svg-data-reference/c-image-data-reference/r-timestamp-cat.md#reference-59a27b72f4cb4a53a3baba83214c4ded)
