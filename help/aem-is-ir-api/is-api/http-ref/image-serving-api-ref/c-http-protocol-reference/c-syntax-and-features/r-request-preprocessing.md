---
description: Image Serving fornisce un semplice preprocessore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.
seo-description: Image Serving fornisce un semplice preprocessore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.
seo-title: Richiesta preelaborazione
solution: Experience Manager
title: Richiesta preelaborazione
topic: Scene7 Image Serving - Image Rendering API
uuid: 375bbca2-7a4a-49a9-9577-86e6b2f19990
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Richiesta preelaborazione{#request-preprocessing}

Image Serving fornisce un semplice preprocessore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.

Le raccolte di regole (set di regole) possono essere collegate a ciascun catalogo di immagini, incluso il catalogo predefinito. Le regole sono specificate con i file in formato XML.

Le regole di preelaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate dal parser del server della piattaforma, compresa la manipolazione del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. Le regole possono essere utilizzate anche per configurare e ignorare alcune funzioni di sicurezza che normalmente sono controllate solo con gli attributi del catalogo, come l&#39;offuscamento della richiesta, il marchiamento dell&#39;acqua, nonché per limitare il servizio HTTP a specifici indirizzi IP del client.

Le regole di preelaborazione delle richieste sono adatte a una varietà di applicazioni, alcune delle quali sono elencate di seguito:

* Implementa un meccanismo *percorsi virtuali* che consente di mappare nuovamente il percorso della richiesta su file, FTP e percorsi HTTP.
* Applicazione selettiva di funzioni di protezione, come la filigrana, filtrate per nome o percorso dell’immagine.
* Mancando filigrane o altre funzioni di protezione quando si accede al server da indirizzi IP specifici.
* Applicazione forzata di comandi, come `defaultImage=`, a tutte le richieste o alle richieste che presentano un pattern specifico nel percorso URL o nelle stringhe di query.
* Disattivazione dell&#39;uso di comandi con molta CPU per evitare abusi da parte del server.
* Consente di individuare le immagini sorgente su server HTTP o FTP pur continuando a specificarle nel percorso della richiesta anziché con `src=`.
* Potete controllare le impostazioni di qualità dell’immagine (come la qualità JPEG o la nitidezza) in base al percorso o al nome dell’immagine richiesti.

Informazioni dettagliate sulla creazione, l&#39;utilizzo e la gestione dei set di regole sono disponibili in [Riferimento set di regole](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Consultate anche {#see-also}

[Riferimento](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e) set di regole,  [attributo::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
