---
description: Image Rendering fornisce un semplice pre-processore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.
seo-description: Image Rendering fornisce un semplice pre-processore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.
seo-title: Richiesta pre-elaborazione *
solution: Experience Manager
title: Richiesta pre-elaborazione *
topic: Scene7 Image Serving - Image Rendering API
uuid: ef69ea23-753c-40c8-9edd-eab9c8820c98
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---


# Richiesta pre-elaborazione *{#request-pre-processing}

Image Rendering fornisce un semplice pre-processore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.

Le raccolte di regole (set di regole) possono essere collegate a ciascun catalogo di materiali, incluso il catalogo predefinito. Le regole sono specificate con i file in formato XML.

Le regole di pre-elaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate dal parser di rendering immagini, compresa la manipolazione del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. Le regole possono essere utilizzate anche per configurare e ignorare alcune funzioni che normalmente sono controllate solo con gli attributi del catalogo, come l&#39;impostazione della dimensione predefinita dell&#39;immagine di risposta o la limitazione del servizio HTTP a indirizzi IP client specifici.

Le regole di pre-elaborazione delle richieste sono adatte a una serie di applicazioni, alcune delle quali sono elencate di seguito:

* Implementa un meccanismo *percorsi virtuali* che consente di mappare nuovamente il percorso della richiesta su file, FTP e percorsi HTTP.
* Disattivazione dell&#39;uso di comandi CPU per evitare abusi del server.
* Potete controllare le impostazioni di qualità dell’immagine (come la qualità JPEG o la nitidezza) in base al percorso o al nome dell’immagine richiesti.

Informazioni dettagliate sulla creazione, l&#39;utilizzo e la gestione dei set di regole sono disponibili in Riferimento set di regole.

Vedere anche Riferimento set di regole, attributo::RuleSetFile
