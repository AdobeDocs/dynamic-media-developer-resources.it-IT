---
description: Utilizzate queste impostazioni del server per le cartelle dei dati di contenuto.
seo-description: Utilizzate queste impostazioni del server per le cartelle dei dati di contenuto.
seo-title: Cartelle dei dati di contenuto
solution: Experience Manager
title: Cartelle dei dati di contenuto
topic: Scene7 Image Serving - Image Rendering API
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%

---


# Cartelle dei dati di contenuto{#content-data-folders}

Utilizzate queste impostazioni del server per le cartelle dei dati di contenuto.

## IS::RootPath - Image Data Root Folders {#section-5c57569514bb4d00b19de31d2e137e3b}

La posizione di tutti i dati di origine, incluse immagini, font e profili ICC. Può trattarsi di uno o più percorsi di file assoluti o relativi a *[!DNL install_folder]*, separati da punto e virgola. Se vuoto, *[!DNL install_folder]* è la radice predefinita. È possibile specificare più valori per distribuire i dati immagine su più file system. Il server immagini proverà i percorsi principali nell’ordine specificato fino a trovare il file richiesto.

## PS::staticContent.rootPath - Cartelle principali dei dati di contenuto statico {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

La posizione dei dati di origine del contenuto statico che devono essere inviati tramite il contesto [!DNL /is/static]. Può essere uno o più percorsi di file assoluti o relativi a *[!DNL install_folder]*, separati da punto e virgola. Se vuoto, *[!DNL install_folder]* è la radice predefinita.

È possibile specificare più valori separati da punti e virgola per distribuire contenuti statici su più file system. In genere, impostate gli stessi valori di `IS::RootPath`.

Il server piattaforme tenta i percorsi principali nell&#39;ordine specificato fino a trovare il file richiesto.

>[!NOTE]
>
>Per impostazione predefinita, questo campo è intenzionalmente impostato su una posizione non esistente ( [!DNL *[!DNL install_folder]*/static]), disattivando in modo efficace il servizio di contenuto statico.

## IS::SaveDirectory - File Save Root Folder {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Il percorso principale per `attribute::SavePath` (utilizzato da `req=saveToFile`). Il server immagini deve disporre di autorizzazioni di accesso per la sottocartella in cui creare i file immagine.
