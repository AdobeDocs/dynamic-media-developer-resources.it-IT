---
title: Richieste di rendering immagini nidificate
description: Per applicazioni avanzate, è possibile utilizzare il risultato di un'operazione di rendering come immagine di materiale, proprio come un'immagine ottenuta da Image Server.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 52c12786-bbe7-4410-87bb-6245d782a68c
TQID: 'https://experienceleague.adobe.com/Fqiu-HsaRtrWMjBQudUBzr1iu3WLg7173Kf-71ikejI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
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
