---
title: Convertitore vignettatura
description: Il Convertitore vignettatura (vntc) è un’utility per riga di comando utilizzata per preparare il contenuto creato con Image Authoring per la distribuzione con Image Rendering.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 9e2ad2d4-9061-41d1-941b-8be4c17a6c43
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---

# Convertitore vignettatura{#vignette-converter}

Il Convertitore vignettatura (vntc) è un’utility per riga di comando utilizzata per preparare il contenuto creato con Image Authoring per la distribuzione con Image Rendering.

[!DNL vntc] è in [!DNL *[!DNL install_root]*\ImageServer\bin]. Offre le seguenti funzionalità:

* Converte le vignettature primarie in vignettature di produzione a risoluzione singola, a più risoluzioni o piramidali (vedere [Ridimensionamento vignettatura](../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585)).
* Produce l&#39;archivio di produzione e la finestra che copre i file di stile (vedere `-resolution` e `-jpegquality`).

* Produrre diverse versioni dei file di stile di vignettature, archivi e copertine per finestre da utilizzare con le versioni precedenti di Image Rendering.
* Estrae le immagini delle visualizzazioni dalle vignettature, a risoluzione completa o con miniature (vedere `-thumbwidth` e `-image`).
* Estrae le proprietà rilevanti dal file di origine (vedere `-info`) e le invia a `stdout` o a un file di log facoltativo (vedere `-log`).

Sebbene l&#39;utilizzo di [!DNL vntc] sia facoltativo, Adobe ne consiglia l&#39;utilizzo per ottenere le migliori prestazioni del server. Il Convertitore di vignettatura implementa anche un ampio controllo degli errori e può prevenire gravi problemi del server, inclusi arresti anomali, se utilizzato con diligenza.

Durante la generazione delle vignettature di produzione, la larghezza in pixel della vignettatura di output (o 0 in caso di vignettature a piramide o a più risoluzioni) viene aggiunta al nome del file di vignettatura di output generato. Durante l&#39;elaborazione dei file di stile dell&#39;archivio, la risoluzione di output viene aggiunta al nome del file di output. Tutti i file di output, inclusi i file di miniatura, immagine e log facoltativi e il file di stile della vignettatura o dell&#39;archivio di produzione, si trovano nella stessa directory in cui si trova *[!DNL sourceFile]* (a meno che non sia specificato `-destPath`).

Per impostazione predefinita, il Convertitore di vignettatura si limita a un massimo di 3 GB di memoria. Quando vntc raggiunge questo limite, l’elaborazione viene interrotta e viene generato un errore. Questo limite può essere modificato con `-maxmem`.

>[!NOTE]
>
>Lo strumento di aggiornamento vignettatura in Image Authoring può essere utilizzato anche per preparare vignettature per l’utilizzo di Image Rendering. Analogamente, lo strumento Content Authoring può generare file di stile di archivio da utilizzare con Image Rendering. Utilizzare [!DNL vntc] se l&#39;elaborazione deve essere automatizzata. Gli strumenti di Image Authoring includono un’interfaccia grafica, quindi sono generalmente più facili da usare in modo interattivo.

## Consultate anche {#section-3c756bf17b634543904fdd928adeafb2}

Documentazione di Image Authoring
