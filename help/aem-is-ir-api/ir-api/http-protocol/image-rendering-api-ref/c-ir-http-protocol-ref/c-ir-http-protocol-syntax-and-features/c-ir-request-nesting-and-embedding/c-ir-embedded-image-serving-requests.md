---
description: Una richiesta di Image Server (IS) può essere utilizzata come immagine materiale.
seo-description: Una richiesta di Image Server (IS) può essere utilizzata come immagine materiale.
seo-title: Richieste server immagini incorporate
solution: Experience Manager
title: Richieste server immagini incorporate
topic: Scene7 Image Serving - Image Rendering API
uuid: dd72880d-8824-40b3-a5da-0f6ff4922939
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Richieste server immagini incorporate{#embedded-image-server-requests}

Una richiesta di Image Server (IS) può essere utilizzata come immagine materiale.

Specificate la richiesta nel `src=` comando come segue:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Per il `is` token viene fatta distinzione tra maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso principale di Image Server (in genere [!DNL http:// *[!DNL server]*/is/image/&quot;]), ma può includere token di regole di pre-elaborazione.

I seguenti comandi IS vengono ignorati quando specificati in richieste nidificate (nell’URL della richiesta o in `catalog::Modifier` o `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Vengono inoltre ignorati `attribute::MaxPix` e `attribute::DefaultPix` del catalogo immagini applicato alla richiesta IS incorporata.

Se l&#39;immagine del risultato della richiesta nidificata include dati di maschera (alfa), viene sempre passata al materiale. Usate un livello dell’immagine di sfondo in tinta unita per evitare l’effetto alfa indesiderato.

Facoltativamente, il risultato dell&#39;immagine di una richiesta IS incorporata può essere memorizzato nella cache includendo `cache=on`. Per impostazione predefinita, il caching dei dati intermedi è disattivato. La memorizzazione nella cache deve essere abilitata solo quando è previsto che l&#39;immagine intermedia venga riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. È applicabile la gestione standard della cache lato server. I dati vengono memorizzati nella cache in un formato senza perdita di dati.
