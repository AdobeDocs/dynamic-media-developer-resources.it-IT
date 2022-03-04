---
title: Richieste server di immagini incorporate
description: Una richiesta di Image Server (IS) può essere utilizzata come immagine materiale.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Richieste server di immagini incorporate{#embedded-image-server-requests}

Una richiesta di Image Server (IS) può essere utilizzata come immagine materiale.

Specifica la richiesta in `src=` come segue:

` …&src=is( *[!DNL imageServingRequest]*)&…`

La `is` il token è sensibile a maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso principale di Image Server (in genere [!DNL http:// *[!DNL server]*/is/image/"]), ma può includere i token delle regole di pre-elaborazione.

I seguenti comandi IS vengono ignorati quando specificati nelle richieste nidificate (nell’URL della richiesta o in `catalog::Modifier` o `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Vengono inoltre ignorati `attribute::MaxPix` e `attribute::DefaultPix` del catalogo immagini applicato alla richiesta IS incorporata.

Se l&#39;immagine del risultato della richiesta nidificata include dati maschera (alfa), viene sempre passata al materiale. Utilizza un livello immagine di sfondo a colori solidi per evitare alfa indesiderato.

Il risultato dell&#39;immagine di una richiesta IS incorporata può essere memorizzato in cache facoltativamente includendo `cache=on`. Per impostazione predefinita, la memorizzazione in cache dei dati intermedi è disabilitata. La memorizzazione in cache deve essere abilitata solo quando l&#39;immagine intermedia viene riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. Si applica la gestione standard della cache lato server. I dati vengono memorizzati nella cache in un formato senza perdita di dati.
