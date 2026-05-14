---
title: Richieste server immagini incorporate
description: È possibile utilizzare una richiesta Image Server (IS) come immagine materiale.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4ece9738-45e0-43c0-ba1c-2a05ef1f39be
TQID: 'https://experienceleague.adobe.com/dt-baBh9jAyJdjqopFR3AoqRvz5zqLzi8B3SnE04xEs'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 183
ht-degree: 0%

---

# Richieste server immagini incorporate{#embedded-image-server-requests}

È possibile utilizzare una richiesta Image Server (IS) come immagine materiale.

Specificare la richiesta nel comando `src=` nel modo seguente:

` …&src=is( *[!DNL imageServingRequest]*)&…`

Il token `is` distingue tra maiuscole e minuscole.

La richiesta nidificata non deve includere il percorso radice di Image Server (in genere  [!DNL http:// *[!DNL server]*/is/image/"]), ma può includere token di regole di pre-elaborazione.

I seguenti comandi IS vengono ignorati se specificati nelle richieste nidificate (nell&#39;URL della richiesta oppure in `catalog::Modifier` o `catalog::PostModifier`):

* `bgc=`
* `fmt=`
* `icc=`
* `iccEmbed=`
* `printRes=`
* `qlt=`
* `quantize=`
* `req=`

Vengono ignorati anche `attribute::MaxPix` e `attribute::DefaultPix` del catalogo immagini che si applica alla richiesta IS incorporata.

Se l&#39;immagine del risultato della richiesta nidificata include dati di maschera (alfa), questa viene sempre trasmessa al materiale. Utilizzate un livello immagine di sfondo a tinta unita per evitare valori alfa indesiderati.

Il risultato immagine di una richiesta IS incorporata può essere memorizzato nella cache facoltativamente includendo `cache=on`. Per impostazione predefinita, la memorizzazione nella cache dei dati intermedi è disabilitata. La memorizzazione in cache deve essere abilitata solo quando l’immagine intermedia viene riutilizzata in una richiesta diversa entro un periodo di tempo ragionevole. Si applica la gestione della cache lato server standard. I dati vengono memorizzati nella cache in un formato senza perdita di dati.
