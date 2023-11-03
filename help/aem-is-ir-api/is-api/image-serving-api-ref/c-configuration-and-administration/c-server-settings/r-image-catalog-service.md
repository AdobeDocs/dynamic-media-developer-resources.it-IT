---
description: Utilizzare queste impostazioni server per il servizio catalogo immagini.
solution: Experience Manager
title: Servizio catalogo immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c089ef35-47a1-4921-8a5e-1ca78f29794d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---

# Servizio catalogo immagini{#image-catalog-service}

Utilizzare queste impostazioni server per il servizio catalogo immagini.

## CS::catalog.rootPath - Cartella catalogo immagini {#section-02d107f157384b18835f884f24fea3aa}

Posizione della cartella del catalogo immagini (dove tutti [!DNL catalog.ini] i file devono essere individuati). Può essere un percorso assoluto o un percorso relativo al *[!DNL install_folder]*. Il server monitora continuamente questa cartella e carica o ricarica i cataloghi quando viene creato un nuovo file di catalogo principale (con [!DNL .ini] file) o quando l&#39;ora dell&#39;ultima modifica di un file di catalogo principale esistente è cambiata.

## CS::catalog.cacheRoot - Cartella cache catalogo {#section-73e499c3a5974f1aa4251e70272ff503}

Cartella radice per la cache del sistema di cataloghi. Può essere impostato sullo stesso valore di una delle cartelle in `PS::cache.rootPaths`. La cartella deve essere creata manualmente prima di modificare questa impostazione.

## CS::catalog.modificationWaitTime - Ritardo analisi file catalogo {#section-7348065bcc124cb68ea947bf1b9b0845}

Tempo in millisecondi di attesa del servizio di catalogo dopo un [!DNL catalog.ini] finché non vengono caricati i file di catalogo secondari. Questo ritardo assicura che tutti i file di catalogo secondari siano aggiornati prima che il servizio catalogo tenti di caricarli. Valore intero in msec.

## CS::catalog.refreshInterval - Frequenza di controllo file catalogo {#section-517fefc1d8784777a1026abec8630d58}

Frequenza con cui il servizio catalogo verifica la presenza di modifiche ai cataloghi di immagini. Valore intero in msec.
