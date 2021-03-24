---
description: Utilizza queste impostazioni del server per il servizio catalogo immagini.
solution: Experience Manager
title: Servizio catalogo immagini
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---


# Servizio catalogo immagini{#image-catalog-service}

Utilizza queste impostazioni del server per il servizio catalogo immagini.

## CS::catalog.rootPath - Cartella catalogo immagini {#section-02d107f157384b18835f884f24fea3aa}

Posizione della cartella del catalogo delle immagini (in cui devono trovarsi tutti i file [!DNL catalog.ini]). Può essere un percorso assoluto di file o un percorso relativo a *[!DNL install_folder]*. Il server controlla continuamente questa cartella e carica o ricarica i cataloghi quando viene rilevato un nuovo file di catalogo principale (con suffisso di file [!DNL .ini]) o quando è cambiata l&#39;ultima modifica di un file di catalogo principale esistente.

## CS::catalog.cacheRoot - Cartella cache del catalogo {#section-73e499c3a5974f1aa4251e70272ff503}

Cartella principale per la cache del sistema di catalogo. Può essere impostato sullo stesso di una delle cartelle in `PS::cache.rootPaths`. La cartella deve essere creata manualmente prima di modificare questa impostazione.

## CS::catalog.modificationWaitTime - Ritardo di analisi dei file del catalogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tempo in msec in cui il servizio catalogo attende dopo la modifica di un file [!DNL catalog.ini] fino al caricamento dei file di catalogo secondari. Questo ritardo garantisce che tutti i file di catalogo secondari siano aggiornati prima che il servizio di catalogo tenti di caricarli. Valore intero in msec.

## CS::catalog.refreshInterval - Frequenza di controllo del file del catalogo {#section-517fefc1d8784777a1026abec8630d58}

Frequenza con cui il servizio catalogo verificherà la presenza di modifiche ai cataloghi di immagini. Valore intero in msec.
