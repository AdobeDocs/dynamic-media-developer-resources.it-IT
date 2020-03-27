---
description: Per le applicazioni avanzate è possibile utilizzare il risultato di un'operazione di rendering come immagine materiale, proprio come un'immagine ottenuta da Image Server.
seo-description: Per le applicazioni avanzate è possibile utilizzare il risultato di un'operazione di rendering come immagine materiale, proprio come un'immagine ottenuta da Image Server.
seo-title: Richieste di rendering immagini nidificate
solution: Experience Manager
title: Richieste di rendering immagini nidificate
topic: Scene7 Image Serving - Image Rendering API
uuid: 12551bd5-ff5f-45d6-81e9-5ba0be47a425
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Richieste di rendering immagini nidificate{#nested-image-rendering-requests}

Per le applicazioni avanzate è possibile utilizzare il risultato di un&#39;operazione di rendering come immagine materiale, proprio come un&#39;immagine ottenuta da Image Server.

Una richiesta di rendering può essere utilizzata come immagine materiale specificandola nel `src=` comando come segue:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Per il `ir` token viene fatta distinzione tra maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso principale di rendering delle immagini (in genere `http:// *[!DNL server]*/ir/render/'`), ma può includere token di regole di pre-elaborazione.

I comandi seguenti vengono ignorati quando specificati in richieste nidificate (nell’URL della richiesta o in `catalog::Modifier` oppure `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Vengono inoltre ignorati `attribute::MaxPix` e `attribute::DefaultPix` del catalogo di materiali applicabile alla richiesta di rendering nidificata.

Facoltativamente, il risultato dell’immagine di una richiesta IR nidificata può essere memorizzato nella cache includendo `cache=on`. Per impostazione predefinita, il caching dei dati intermedi è disattivato. La memorizzazione nella cache deve essere abilitata solo quando è previsto che l&#39;immagine intermedia venga riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. È applicabile la gestione standard della cache lato server. I dati vengono memorizzati nella cache in un formato senza perdita di dati.
