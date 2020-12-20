---
description: Vignettatura Converter (vntc) è un'utilità della riga di comando utilizzata per preparare il contenuto creato con Image Authoring per la distribuzione con Image Rendering.
seo-description: Vignettatura Converter (vntc) è un'utilità della riga di comando utilizzata per preparare il contenuto creato con Image Authoring per la distribuzione con Image Rendering.
seo-title: Convertitore vignettatura
solution: Experience Manager
title: Convertitore vignettatura
topic: Scene7 Image Serving - Image Rendering API
uuid: b32a30d6-ae4a-406f-88a9-e8b0eec394c9
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Convertitore vignettatura{#vignette-converter}

Vignettatura Converter (vntc) è un&#39;utilità della riga di comando utilizzata per preparare il contenuto creato con Image Authoring per la distribuzione con Image Rendering.

[!DNL vntc] si trova in [!DNL  *[!DNL install_root]*\ImageServing\bin]. Dispone delle seguenti funzionalità:

* Converte le vignettature primarie in vignettature di produzione a risoluzione singola, a risoluzione multipla o piramidale (vedere [Ridimensionamento vignettatura](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produce archivi di produzione e finestre che coprono i file di stile (vedere `-resolution` e `-jpegquality`).

* Può produrre diverse versioni di file di stile di vignettature, cabinet e rivestimenti di finestre da usare con versioni precedenti di Image Rendering.
* Gli estratti visualizzano le immagini dalle vignettature, a risoluzione completa o dalle miniature (vedere `-thumbwidth` e `-image`).
* Estrae le proprietà pertinenti dal file di origine (vedere `-info`) e le invia a `stdout` o a un file di registro facoltativo (vedere `-log`).

Anche se l&#39;utilizzo di [!DNL vntc] è opzionale, è vivamente consigliato per ottenere prestazioni ottimali sul server. [!DNL vntc] implementa inoltre un controllo esteso degli errori e può impedire gravi problemi del server, compresi gli arresti anomali, se utilizzati con diligenza.

Durante la generazione delle vignettature di produzione, al nome del file di vignettatura di output generato viene aggiunta la larghezza in pixel della vignettatura di output (o 0 nel caso di vignettature a piramide o a più risoluzioni). Quando si elaborano file di stile cabinet, la risoluzione di output viene aggiunta al nome del file di output. Tutti i file di output, inclusi i file di miniatura, immagine e registro facoltativi, nonché il file di vignettatura di produzione o di stile cabinet, vengono inseriti nella stessa directory in cui si trova *[!DNL sourceFile]* (a meno che non sia specificato `-destPath`).

[!DNL vntc] per impostazione predefinita si limita a un massimo di 3 GB di memoria. Quando Vntc raggiunge questo limite, interrompe l&#39;elaborazione e genera un errore. Questo limite può essere modificato utilizzando `-maxmem`.

>[!NOTE]
>
>Lo strumento di aggiornamento della vignettatura in Image Authoring può essere utilizzato anche per preparare le vignettature da usare per il rendering delle immagini. Allo stesso modo, lo strumento di creazione dei contenuti è in grado di generare file di stile cabinet da usare con il rendering delle immagini. Per automatizzare l&#39;elaborazione, utilizzare [!DNL vntc]. Gli strumenti di Image Authoring includono un’interfaccia utente grafica, che in genere risulta più semplice da usare in modo interattivo.

## Consultate anche {#section-3c756bf17b634543904fdd928adeafb2}

Documentazione sull’authoring delle immagini
