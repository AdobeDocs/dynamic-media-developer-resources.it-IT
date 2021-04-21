---
description: Tutti i file di log vengono scritti nella stessa cartella di log specificata con la directory TC.
solution: Experience Manager
title: Registrazione server
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# Registrazione server{#server-logging}

Tutti i file di log vengono scritti nella stessa cartella di log specificata con TC::directory.

I file di registro vengono generalmente creati e ruotati su base giornaliera. I file di registro precedenti nella cartella di registro vengono eliminati automaticamente dopo un numero specificato di giorni ( `TC::maxDays`).

Importante È necessario riservare una quantità sufficiente di spazio su disco per i file di registro per evitare di esaurire lo spazio su disco. 1-2 GB/giorno possono essere necessari per un server e per le impostazioni di registro predefinite.

Platform Server e Image Server creano i tre tipi di file di registro descritti di seguito.

Anche altri componenti Image Server e alcuni altri pacchetti Dynamic Media, come i visualizzatori Dynamic Media, possono creare file di registro nella stessa cartella. Questi file di log sono per uso interno di Dynamic Media e possono essere richiesti dal supporto tecnico Dynamic Media per scopi di risoluzione dei problemi.

* [Registro di accesso](c-access-log.md)
* [Registro di traccia](c-trace-log.md)
* [Registro server immagini](c-image-server-log.md)

## Consultate anche {#section-5ff5e46031b1461c92de24e632610d6d}

[Registrazione](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-access-logging.md#reference-5d175921c12a48a6be7f722517615d0f) degli accessi,  [Debug/Trace Logging](../../../../is-api/image-serving-api-ref/c-configuration-and-administration/c-server-settings/r-debug-trace-logging.md#reference-4b372f81001849f5b495457da7af8e82)
