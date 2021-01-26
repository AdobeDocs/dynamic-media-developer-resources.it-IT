---
description: Tutti i file di registro vengono scritti nella stessa cartella di registro specificata con la directory TC.
solution: Experience Manager
title: Registrazione server
topic: Dynamic Media Image Serving - Image Rendering API
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 1%

---


# Registrazione server{#server-logging}

Tutti i file di registro vengono scritti nella stessa cartella di registro specificata con TC::directory.

I file di registro vengono in genere creati e ruotati su base giornaliera. I file di registro precedenti nella cartella di registro vengono eliminati automaticamente dopo un numero specificato di giorni ( `TC::maxDays`).

Importante È necessario riservare una quantità sufficiente di spazio su disco ai file di registro per evitare che lo spazio su disco sia esaurito. Potrebbero essere necessari 1-2 GB al giorno per un server utilizzato e per le impostazioni di registro predefinite.

Server piattaforme e server immagini creano i tre tipi di file di registro descritti di seguito.

Altri componenti Image Server e alcuni altri pacchetti Dynamic Media, come i visualizzatori Dynamic Media, possono anche creare file di registro nella stessa cartella. Questi file di registro sono per uso interno di Dynamic Media e possono essere richiesti dal supporto tecnico di Dynamic Media a scopo di risoluzione dei problemi.

* [Registro di accesso](c-access-log.md)
* [Registro di traccia](c-trace-log.md)
* [Registro server immagini](c-image-server-log.md)

## Consultate anche {#section-5ff5e46031b1461c92de24e632610d6d}

[Registrazione](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f) di accesso,  [debug/registrazione traccia](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
