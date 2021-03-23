---
description: Una richiesta di Image Server (IS) può essere utilizzata come immagine materiale.
seo-description: Una richiesta di Image Server (IS) può essere utilizzata come immagine materiale.
seo-title: Richieste server di immagini incorporate
solution: Experience Manager
title: Richieste server di immagini incorporate
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 0%

---


# Richieste server di immagini incorporate{#embedded-image-server-requests}

Una richiesta di Image Server (IS) può essere utilizzata come immagine materiale.

Specifica la richiesta nel comando `src=` come segue:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Il token `is` fa distinzione tra maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso principale di Image Server (in genere [!DNL http:// *[!DNL server]*/is/image/&quot;]), ma può includere token di regola di pre-elaborazione.

I seguenti comandi IS vengono ignorati quando specificati nelle richieste nidificate (nell&#39;URL della richiesta o in `catalog::Modifier` o `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Vengono inoltre ignorati `attribute::MaxPix` e `attribute::DefaultPix` del catalogo immagini applicabile alla richiesta IS incorporata.

Se l&#39;immagine del risultato della richiesta nidificata include dati maschera (alfa), viene sempre passata al materiale. Utilizza un livello immagine di sfondo a colori solidi per evitare alfa indesiderato.

Il risultato dell&#39;immagine di una richiesta IS incorporata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, la memorizzazione in cache dei dati intermedi è disabilitata. La memorizzazione in cache deve essere abilitata solo quando ci si aspetta che l&#39;immagine intermedia venga riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. Si applica la gestione standard della cache lato server. I dati vengono memorizzati nella cache in un formato senza perdita di dati.
