---
description: Usate queste impostazioni del server per il servizio Catalogo immagini.
seo-description: Usate queste impostazioni del server per il servizio Catalogo immagini.
seo-title: Servizio catalogo immagini
solution: Experience Manager
title: Servizio catalogo immagini
topic: Scene7 Image Serving - Image Rendering API
uuid: 601b1c30-7d51-448b-97b5-5ad9cb383975
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# Servizio catalogo immagini{#image-catalog-service}

Usate queste impostazioni del server per il servizio Catalogo immagini.

## CS::catalog.rootPath - Cartella catalogo immagini {#section-02d107f157384b18835f884f24fea3aa}

Posizione della cartella del catalogo immagini (in cui devono trovarsi tutti i file [!DNL catalog.ini]). Può essere un percorso assoluto di file o un percorso relativo a *[!DNL install_folder]*. Il server controlla continuamente questa cartella e carica o ricarica i cataloghi quando viene rilevato un nuovo file catalogo principale (con suffisso di file [!DNL .ini]) o quando viene modificata l&#39;ultima modifica di un file catalogo principale esistente.

## CS::catalog.cacheRoot - Cartella cache catalogo {#section-73e499c3a5974f1aa4251e70272ff503}

Cartella principale per la cache del sistema di catalogo. Può essere impostato sullo stesso valore di una delle cartelle in `PS::cache.rootPaths`. Prima di modificare questa impostazione, è necessario creare manualmente la cartella.

## CS::catalog.changeWaitTime - Ritardo analisi file catalogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tempo in msec che il servizio catalogo attende dopo che un file [!DNL catalog.ini] è stato modificato fino a quando non carica i file del catalogo secondario. Questo ritardo garantisce che tutti i file di catalogo secondari siano aggiornati prima che il servizio di catalogo tenti di caricarli. Valore intero in msec.

## CS::catalog.refreshInterval - Frequenza controllo file catalogo {#section-517fefc1d8784777a1026abec8630d58}

Frequenza con cui il servizio catalogo controllerà la presenza di modifiche ai cataloghi di immagini. Valore intero in msec.
