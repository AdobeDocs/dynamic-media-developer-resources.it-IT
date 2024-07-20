---
title: Richieste di rendering immagini nidificate
description: Per applicazioni avanzate, è possibile utilizzare il risultato di un'operazione di rendering come immagine di materiale, proprio come un'immagine ottenuta da Image Server.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 0%

---

# Richieste di rendering immagini nidificate{#nested-image-rendering-requests}

Per applicazioni avanzate, è possibile utilizzare il risultato di un&#39;operazione di rendering come immagine di materiale, proprio come un&#39;immagine ottenuta da Image Server.

Una richiesta di rendering può essere utilizzata come immagine materiale specificandola nel comando `src=` come segue:

` …&src=ir{ *[!DNL renderRequest]*}&…`

Il token `ir` distingue tra maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso radice di Image Rendering (in genere `http:// *[!DNL server]*/ir/render/'`), ma può includere token di regole di pre-elaborazione.

I seguenti comandi vengono ignorati se specificati nelle richieste nidificate (nell&#39;URL della richiesta oppure in `catalog::Modifier` o `catalog::PostModifier`):

* `fmt=`
* `qlt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `req=`
* `bgc=`

Vengono ignorati anche `attribute::MaxPix` e `attribute::DefaultPix` del catalogo dei materiali che si applica alla richiesta di rendering nidificata.

Il risultato immagine di una richiesta a infrarossi nidificata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, la memorizzazione nella cache dei dati intermedi è disabilitata. La memorizzazione in cache deve essere abilitata solo quando l’immagine intermedia viene riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. Si applica la gestione della cache lato server standard. I dati vengono memorizzati nella cache in un formato senza perdita di dati.
