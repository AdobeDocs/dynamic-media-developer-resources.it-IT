---
description: Image Server fornisce un semplice preprocessore di richieste basato su regole di corrispondenza e sostituzione di espressioni regolari.
solution: Experience Manager
title: Pre-elaborazione della richiesta
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# Pre-elaborazione della richiesta{#request-preprocessing}

Image Server fornisce un semplice preprocessore di richieste basato su regole di corrispondenza e sostituzione di espressioni regolari.

Raccolte di regole (set di regole) possono essere associate a ciascun catalogo di immagini, incluso il catalogo predefinito. Le regole vengono specificate con file in formato XML.

Le regole di pre-elaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate dal parser di [!DNL Platform Server], inclusa la modifica del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. Le regole possono essere utilizzate anche per configurare e ignorare alcune funzioni di sicurezza che di solito sono controllate solo con attributi di catalogo, come offuscamento delle richieste, watermark, nonché per limitare il servizio HTTP a specifici indirizzi IP client.

Le regole di pre-elaborazione delle richieste sono adatte per diverse applicazioni, alcune delle quali sono elencate di seguito:

* Implementa un meccanismo di *percorsi virtuali*, che consente di mappare nuovamente il percorso della richiesta su percorsi file, FTP e HTTP.
* Applicazione selettiva di funzioni di sicurezza, ad esempio filigrana, filtrate in base al nome o al percorso dell’immagine.
* Omissione delle filigrane o di altre funzioni di sicurezza durante l’accesso al server da indirizzi IP specifici.
* Forzare l&#39;applicazione di comandi, ad esempio `defaultImage=`, a tutte le richieste o a richieste che presentano un pattern specifico nel percorso URL o nelle stringhe di query.
* Non consentire l&#39;utilizzo di comandi a uso intensivo della CPU per impedire l&#39;utilizzo non corretto del server.
* Consente di individuare le immagini di origine su server HTTP o FTP specificandole ancora nel percorso della richiesta anziché con `src=`.
* Controlla le impostazioni di qualità delle immagini (ad esempio qualità del JPEG o nitidezza) a seconda del percorso della richiesta o del nome dell’immagine.

Informazioni dettagliate sulla creazione, l&#39;utilizzo e la gestione dei set di regole sono disponibili in [Riferimento set di regole](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## Consultate anche {#see-also}

[Riferimento set regole](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [attributo::RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
