---
title: Richiedi pre-elaborazione
description: Image Rendering fornisce un semplice preprocessore per richieste basato su regole di corrispondenza e sostituzione di espressioni regolari.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
TQID: 'https://experienceleague.adobe.com/zs4izZzuO7u6wYOPmdd8AT7r4q-cUFXWUlB1MW6aV0Y'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 220
ht-degree: 0%

---

# Richiedi pre-elaborazione{#request-pre-processing}

Image Rendering fornisce un semplice preprocessore per richieste basato su regole di corrispondenza e sostituzione di espressioni regolari.

Le raccolte di regole (set di regole) possono essere associate a ciascun catalogo di materiali, incluso il catalogo predefinito. Le regole vengono specificate con file in formato XML.

Le regole di pre-elaborazione delle richieste possono modificare il percorso e le porzioni di query delle richieste prima che vengano elaborate dal parser di Image Rendering. Questo precetto include la manipolazione del percorso, l&#39;aggiunta di comandi, la modifica dei valori dei comandi e l&#39;applicazione di modelli o macro. È inoltre possibile utilizzare le regole per configurare ed eseguire l&#39;override di alcune funzionalità normalmente controllate solo con attributi di catalogo, ad esempio l&#39;impostazione della dimensione predefinita dell&#39;immagine di risposta o la limitazione del servizio HTTP a indirizzi IP client specifici.

Le regole di pre-elaborazione delle richieste sono adatte per varie applicazioni, alcune delle quali sono elencate di seguito:

* Implementa un meccanismo di *percorsi virtuali*, che consente di mappare nuovamente il percorso della richiesta su percorsi file, FTP e HTTP.
* Non consentire l&#39;utilizzo di comandi a uso intensivo di CPU per impedire l&#39;utilizzo non corretto del server.
* Controlla le impostazioni di qualità delle immagini (come qualità JPEG o nitidezza) a seconda del percorso della richiesta o del nome dell’immagine.

Informazioni dettagliate sulla creazione, l’utilizzo e la gestione dei set di regole sono disponibili in Riferimento set di regole.

Vedere anche Riferimento set di regole, attributo::RuleSetFile
