---
title: Richieste server immagini incorporate
description: È possibile utilizzare una richiesta Image Server (IS) come immagine materiale.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---

# Richieste server immagini incorporate{#embedded-image-server-requests}

È possibile utilizzare una richiesta Image Server (IS) come immagine materiale.

Specifica la richiesta in `src=` comando come segue:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Il `is` il token distingue tra maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso root di Image Server (in genere [!DNL http:// *[!DNL server]*/is/image/"]), ma possono includere token di regole di pre-elaborazione.

I seguenti comandi IS vengono ignorati se specificati nelle richieste nidificate (nell’URL della richiesta o in `catalog::Modifier` o `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Vengono ignorati anche i `attribute::MaxPix` e `attribute::DefaultPix` del catalogo immagini applicabile alla richiesta IS incorporata.

Se l&#39;immagine del risultato della richiesta nidificata include dati di maschera (alfa), questa viene sempre trasmessa al materiale. Utilizzate un livello immagine di sfondo a tinta unita per evitare valori alfa indesiderati.

Il risultato dell’immagine di una richiesta IS incorporata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, la memorizzazione nella cache dei dati intermedi è disabilitata. La memorizzazione in cache deve essere abilitata solo quando l’immagine intermedia viene riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. Si applica la gestione della cache lato server standard. I dati vengono memorizzati nella cache in un formato senza perdita di dati.
