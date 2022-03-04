---
title: Richiedi pre-elaborazione
description: Image Rendering fornisce un semplice pre-processore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 20f4922402bd31c71ae650a01597b574220809fa
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# Richiedi pre-elaborazione{#request-pre-processing}

Image Rendering fornisce un semplice pre-processore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.

Le raccolte di regole (set di regole) possono essere collegate a ciascun catalogo di materiali, incluso il catalogo predefinito. Le regole vengono specificate con file in formato XML.

Le regole di pre-elaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate dal parser Image Rendering. Questo precetto include la manipolazione del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. Le regole possono anche essere utilizzate per configurare e sostituire alcune funzioni che sono normalmente controllate solo con gli attributi del catalogo, ad esempio per impostare la dimensione predefinita dell’immagine di risposta o per limitare il servizio HTTP a specifici indirizzi IP del client.

Le regole di pre-elaborazione delle richieste sono adatte a varie applicazioni, alcune delle quali sono elencate di seguito:

* Implementare un *percorsi virtuali* , che consente di mappare nuovamente il percorso della richiesta a percorsi di file, FTP e HTTP.
* Disabilitare l&#39;uso di comandi che richiedono un uso intensivo della CPU per evitare abusi del server.
* Controlla le impostazioni di qualità dell&#39;immagine (ad esempio la qualità o la nitidezza dei JPEG) in base al percorso della richiesta o al nome dell&#39;immagine.

Informazioni dettagliate sulla creazione, l&#39;utilizzo e la gestione dei set di regole sono disponibili in Riferimento set di regole.

Vedi anche Riferimento set di regole, attributo::RuleSetFile
