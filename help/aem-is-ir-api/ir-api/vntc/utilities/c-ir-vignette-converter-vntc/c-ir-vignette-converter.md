---
description: Vignette Converter (vntc) è un'utilità della riga di comando utilizzata per preparare il contenuto creato con Image Authoring per la distribuzione con Image Rendering.
solution: Experience Manager
title: Convertitore vignetta
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 0%

---


# Convertitore vignetta{#vignette-converter}

Vignette Converter (vntc) è un&#39;utilità della riga di comando utilizzata per preparare il contenuto creato con Image Authoring per la distribuzione con Image Rendering.

[!DNL vntc] si trova in [!DNL  *[!DNL install_root]*\ImageServing\bin]. Dispone delle seguenti funzionalità:

* Converte le vignette primarie in vignette di produzione a risoluzione singola, a risoluzione multipla o a piramide (vedi [Scala vignetta](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produce archivi e finestre di produzione che coprono i file di stile (vedere `-resolution` e `-jpegquality`).

* Può produrre diverse versioni di file di stile di vignette, armadi e rivestimenti per finestre da utilizzare con le versioni precedenti di Image Rendering.
* Estrae le immagini visualizzate dalle vignette, a risoluzione completa o dalle miniature (vedi `-thumbwidth` e `-image`).
* Estrae le proprietà rilevanti dal file di origine (vedi `-info`) e le invia a `stdout` o a un file di registro facoltativo (vedi `-log`).

Anche se l’utilizzo di [!DNL vntc] è facoltativo, è vivamente consigliato per le migliori prestazioni del server. [!DNL vntc] implementa anche un controllo esteso degli errori e può impedire gravi problemi del server, compresi gli arresti anomali, quando utilizzato diligentemente.

Quando si generano vignette di produzione, la larghezza in pixel della vignetta di output (o 0 in caso di vignette a piramide o a più risoluzioni) viene aggiunta al nome del file di vignetta di output generato. Quando si elaborano file di stile cabinet, la risoluzione di output viene aggiunta al nome del file di output. Tutti i file di output, inclusi i file di miniatura, immagine e registro facoltativi, nonché la vignetta di produzione o il file di stile dell&#39;archivio, vengono inseriti nella stessa directory in cui si trova *[!DNL sourceFile]* (a meno che non sia specificato `-destPath`).

[!DNL vntc] per impostazione predefinita si limita a un massimo di 3 GB di memoria. Quando Vntc raggiunge questo limite, interrompe l’elaborazione e genera un errore. Questo limite può essere modificato utilizzando `-maxmem`.

>[!NOTE]
>
>Lo strumento di aggiornamento della vignetta in Image Authoring può anche essere utilizzato per preparare vignette per l&#39;uso Image Rendering. Allo stesso modo, lo strumento Content Authoring è in grado di generare file di stile cabinet da utilizzare con Image Rendering. Utilizza [!DNL vntc] per automatizzare l&#39;elaborazione. Gli strumenti di authoring delle immagini includono un’interfaccia utente grafica, che generalmente è più semplice da utilizzare in modo interattivo.

## Consultate anche {#section-3c756bf17b634543904fdd928adeafb2}

Documentazione sull’authoring delle immagini
