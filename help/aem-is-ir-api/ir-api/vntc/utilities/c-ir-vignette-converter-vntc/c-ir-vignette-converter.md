---
description: Il Convertitore vignettatura (vntc) è un’utility per riga di comando utilizzata per preparare il contenuto creato con Image Authoring per la distribuzione con Image Rendering.
solution: Experience Manager
title: Convertitore vignettatura
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---

# Convertitore vignettatura{#vignette-converter}

Il Convertitore vignettatura (vntc) è un’utility per riga di comando utilizzata per preparare il contenuto creato con Image Authoring per la distribuzione con Image Rendering.

[!DNL vntc] si trova in [!DNL *[!DNL install_root]*\ImageServing\bin]. Offre le seguenti funzionalità:

* Converte le vignettature primarie in vignettature di produzione a risoluzione singola, multirisoluzione o piramidale (vedere [Ridimensionamento vignettatura](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produce un archivio di produzione e una finestra che copre i file di stile (vedere `-resolution` e `-jpegquality`).

* Può produrre diverse versioni di file di stile di vignettature, archivi e copertine per finestre da utilizzare con versioni precedenti di Image Rendering.
* Estrae le immagini di visualizzazione dalle vignettature, a risoluzione completa o in miniatura (vedere `-thumbwidth` e `-image`).
* Estrae le proprietà rilevanti dal file di origine (vedere `-info`) e li invia a `stdout` o un file di registro opzionale (vedere `-log`).

Mentre l&#39;utilizzo di [!DNL vntc] è opzionale, è fortemente consigliato per ottenere prestazioni server ottimali. [!DNL vntc] implementa inoltre un esteso controllo degli errori e, se utilizzato con diligenza, può evitare gravi problemi del server, inclusi arresti anomali.

Durante la generazione delle vignettature di produzione, la larghezza in pixel della vignettatura di output (o 0 in caso di vignettature a piramide o a più risoluzioni) viene aggiunta al nome del file di vignettatura di output generato. Durante l&#39;elaborazione dei file di stile dell&#39;archivio, la risoluzione di output viene aggiunta al nome del file di output. Tutti i file di output, inclusi i file di miniatura, immagine e registro facoltativi e il file di stile della vignettatura o dell&#39;archivio di produzione, si trovano nella stessa directory in cui *[!DNL sourceFile]* si trova (a meno che `-destPath` è specificato).

[!DNL vntc] si limita per impostazione predefinita a un massimo di 3 GB di memoria. Quando Vntc raggiunge questo limite, l’elaborazione si interrompe e viene generato un errore. Questo limite può essere modificato tramite `-maxmem`.

>[!NOTE]
>
>Lo strumento di aggiornamento vignettatura in Image Authoring può essere utilizzato anche per preparare vignettature per l’utilizzo di Image Rendering. Analogamente, lo strumento Content Authoring è in grado di generare file di stile archivio da utilizzare con Image Rendering. Utilizzare [!DNL vntc] se l’elaborazione deve essere automatizzata. Gli strumenti di Image Authoring includono un’interfaccia grafica, quindi sono generalmente più facili da usare in modo interattivo.

## Consultate anche {#section-3c756bf17b634543904fdd928adeafb2}

Documentazione di Image Authoring
