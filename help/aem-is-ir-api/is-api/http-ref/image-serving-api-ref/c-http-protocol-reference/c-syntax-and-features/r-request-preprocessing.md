---
description: Image Serving fornisce un semplice preprocessore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.
solution: Experience Manager
title: Pre-elaborazione delle richieste
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Pre-elaborazione delle richieste{#request-preprocessing}

Image Serving fornisce un semplice preprocessore di richiesta basato su regole di corrispondenza e sostituzione delle espressioni regolari.

Le raccolte di regole (set di regole) possono essere collegate a ciascun catalogo di immagini, incluso il catalogo predefinito. Le regole vengono specificate con file in formato XML.

Le regole di preelaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate da [!DNL Platform Server]parser, che include la manipolazione del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. Le regole possono anche essere utilizzate per configurare e sostituire alcune funzioni di sicurezza che sono normalmente controllate solo con attributi di catalogo, come l’offuscamento della richiesta, il watermarking e la limitazione del servizio HTTP a specifici indirizzi IP del client.

Le regole di preelaborazione delle richieste sono adatte a diverse applicazioni, alcune delle quali sono elencate di seguito:

* Implementare un *percorsi virtuali* , che consente di mappare nuovamente il percorso della richiesta a percorsi di file, FTP e HTTP.
* Applicazione selettiva delle funzioni di sicurezza, ad esempio il watermarking, filtrate per nome o percorso dell&#39;immagine.
* Eliminazione di filigrane o altre funzioni di sicurezza quando si accede al server da indirizzi IP specifici.
* Applicazione forzata di comandi quali `defaultImage=`, a tutte le richieste o a quelle che presentano un pattern specifico nel percorso URL o nelle stringhe di query.
* Disabilitazione dell&#39;uso di comandi ad alta intensità di CPU per evitare abusi del server.
* Consentire alle immagini di origine di trovarsi su server HTTP o FTP mentre le specificano ancora sul percorso della richiesta anziché con `src=`.
* Controlla le impostazioni di qualità dell&#39;immagine (ad esempio la qualità o la nitidezza dei JPEG) in base al percorso della richiesta o al nome dell&#39;immagine.

Informazioni dettagliate sulla creazione, l&#39;utilizzo e la gestione dei set di regole sono disponibili nella sezione [Riferimento set di regole](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Consultate anche {#see-also}

[Riferimento set di regole](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attributo::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
