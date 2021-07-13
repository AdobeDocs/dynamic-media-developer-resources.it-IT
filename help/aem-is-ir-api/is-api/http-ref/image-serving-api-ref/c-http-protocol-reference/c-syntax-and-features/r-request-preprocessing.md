---
description: Image Serving fornisce un semplice preprocessore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.
solution: Experience Manager
title: Pre-elaborazione delle richieste
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# Pre-elaborazione delle richieste{#request-preprocessing}

Image Serving fornisce un semplice preprocessore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.

Le raccolte di regole (set di regole) possono essere collegate a ciascun catalogo di immagini, incluso il catalogo predefinito. Le regole vengono specificate con file in formato XML.

Le regole di preelaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate dal parser di Platform Server, inclusa la manipolazione del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. È inoltre possibile utilizzare le regole per configurare e sostituire alcune funzioni di sicurezza che sono normalmente controllate solo con attributi di catalogo, come l’offuscamento della richiesta, il watermarking e la limitazione del servizio HTTP a specifici indirizzi IP client.

Le regole di preelaborazione delle richieste sono adatte a diverse applicazioni, alcune delle quali sono elencate di seguito:

* Implementa un meccanismo *percorsi virtuali* che consente di mappare nuovamente il percorso della richiesta a percorsi di file, FTP e HTTP.
* Applicazione selettiva delle funzioni di sicurezza, ad esempio il watermarking, filtrate per nome o percorso dell&#39;immagine.
* Eliminazione di filigrane o altre funzioni di sicurezza quando si accede al server da indirizzi IP specifici.
* Applicazione forzata di comandi, come `defaultImage=`, a tutte le richieste o alle richieste che presentano un pattern specifico nel percorso URL o nelle stringhe di query.
* Disabilitazione dell&#39;uso di comandi ad alta intensità di CPU per evitare abusi del server.
* Consente di posizionare le immagini di origine su server HTTP o FTP pur specificando tali immagini nel percorso della richiesta anziché con `src=`.
* Controlla le impostazioni di qualità dell&#39;immagine (come la qualità JPEG o la nitidezza) a seconda del percorso della richiesta o del nome dell&#39;immagine.

Informazioni dettagliate sulla creazione, l&#39;utilizzo e la gestione dei set di regole sono disponibili in [Riferimento set di regole](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Consultate anche {#see-also}

[Riferimento](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e) set di regole,  [attributo::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
