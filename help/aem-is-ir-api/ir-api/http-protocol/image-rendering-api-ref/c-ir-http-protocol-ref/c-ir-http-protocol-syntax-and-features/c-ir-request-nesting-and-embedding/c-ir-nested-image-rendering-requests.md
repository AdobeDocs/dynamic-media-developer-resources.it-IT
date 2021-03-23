---
description: Per le applicazioni avanzate è possibile utilizzare il risultato di un'operazione di rendering come immagine di materiale, proprio come un'immagine ottenuta da Image Serving.
seo-description: Per le applicazioni avanzate è possibile utilizzare il risultato di un'operazione di rendering come immagine di materiale, proprio come un'immagine ottenuta da Image Serving.
seo-title: Richieste di rendering immagini nidificate
solution: Experience Manager
title: Richieste di rendering immagini nidificate
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%

---


# Richieste di rendering immagini nidificate{#nested-image-rendering-requests}

Per le applicazioni avanzate è possibile utilizzare il risultato di un&#39;operazione di rendering come immagine di materiale, proprio come un&#39;immagine ottenuta da Image Serving.

Una richiesta di rendering può essere utilizzata come immagine materiale specificandola nel comando `src=` come segue:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Il token `ir` fa distinzione tra maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso principale Image Rendering (in genere `http:// *[!DNL server]*/ir/render/'`), ma può includere token della regola di pre-elaborazione.

I seguenti comandi vengono ignorati quando specificati nelle richieste nidificate (nell’url della richiesta o in `catalog::Modifier` o `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Vengono inoltre ignorati `attribute::MaxPix` e `attribute::DefaultPix` del catalogo dei materiali applicabile alla richiesta di rendering nidificata.

Il risultato immagine di una richiesta IR nidificata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, la memorizzazione in cache dei dati intermedi è disabilitata. La memorizzazione in cache deve essere abilitata solo quando ci si aspetta che l&#39;immagine intermedia venga riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. Si applica la gestione standard della cache lato server. I dati vengono memorizzati nella cache in un formato senza perdita di dati.
