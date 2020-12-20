---
description: Tutti i file di registro vengono scritti nella stessa cartella di registro specificata con la directory TC.
seo-description: Tutti i file di registro vengono scritti nella stessa cartella di registro specificata con la directory TC.
seo-title: Registrazione server
solution: Experience Manager
title: Registrazione server
topic: Scene7 Image Serving - Image Rendering API
uuid: f6145737-e4c3-4533-9be5-5b5a0202fe33
translation-type: tm+mt
source-git-commit: 5717550d2dea8ec086875e770ff8f200aaa75ff3
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Registrazione server{#server-logging}

Tutti i file di registro vengono scritti nella stessa cartella di registro specificata con TC::directory.

I file di registro vengono in genere creati e ruotati su base giornaliera. I file di registro precedenti nella cartella di registro vengono eliminati automaticamente dopo un numero specificato di giorni ( `TC::maxDays`).

Importante È necessario riservare una quantità sufficiente di spazio su disco ai file di registro per evitare che lo spazio su disco sia esaurito. Potrebbero essere necessari 1-2 GB al giorno per un server utilizzato e per le impostazioni di registro predefinite.

Server piattaforme e server immagini creano i tre tipi di file di registro descritti di seguito.

Altri componenti Image Server e alcuni altri pacchetti Scene7, come i visualizzatori Scene7, possono anche creare file di registro nella stessa cartella. Questi file di registro sono per uso interno di Scene7 e possono essere richiesti dal supporto di Scene7 a scopo di risoluzione dei problemi.

* [Registro di accesso](c-access-log.md)
* [Registro di traccia](c-trace-log.md)
* [Registro server immagini](c-image-server-log.md)

## Consultate anche {#section-5ff5e46031b1461c92de24e632610d6d}

[Registrazione](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f) di accesso,  [debug/registrazione traccia](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
