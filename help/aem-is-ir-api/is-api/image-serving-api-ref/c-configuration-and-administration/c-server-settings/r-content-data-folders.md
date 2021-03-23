---
description: Utilizzare queste impostazioni del server per le cartelle di dati di contenuto.
seo-description: Utilizzare queste impostazioni del server per le cartelle di dati di contenuto.
seo-title: Cartelle dei dati di contenuto
solution: Experience Manager
title: Cartelle dei dati di contenuto
uuid: 7c4d60ca-8a8b-453c-887d-a6a16eacc883
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---


# Cartelle dei dati di contenuto{#content-data-folders}

Utilizzare queste impostazioni del server per le cartelle di dati di contenuto.

## IS::RootPath - Cartelle principali dei dati immagine {#section-5c57569514bb4d00b19de31d2e137e3b}

La posizione di tutti i dati di origine, incluse immagini, font e profili ICC. Può trattarsi di uno o più percorsi di file assoluti o relativi a *[!DNL install_folder]*, separati da punto e virgola. Se vuoto, *[!DNL install_folder]* è la radice predefinita. È possibile specificare più valori per distribuire i dati immagine su più file system. Il server di immagini proverà i percorsi principali nell&#39;ordine specificato fino a quando non verrà trovato il file richiesto.

## PS::staticContent.rootPath - Cartelle principali dei dati di contenuto statico {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

La posizione dei dati di origine dei contenuti statici che devono essere inviati tramite il contesto [!DNL /is/static]. Può essere uno o più percorsi di file assoluti o percorsi relativi a *[!DNL install_folder]*, separati da punto e virgola. Se vuoto, *[!DNL install_folder]* è la radice predefinita.

È possibile specificare più valori separati da punti e virgola per distribuire contenuti statici su più file system. In genere impostato sugli stessi valori di `IS::RootPath`.

Platform Server prova i percorsi radice nell’ordine specificato fino a quando non viene trovato il file richiesto.

>[!NOTE]
>
>Per impostazione predefinita, questo campo è intenzionalmente impostato su una posizione non esistente ( [!DNL *[!DNL install_folder]*/static]), disattivando in modo efficace il servizio di contenuti statici.

## IS::SaveDirectory - File Salva cartella principale {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Il percorso principale di `attribute::SavePath` (utilizzato da `req=saveToFile`). Il server immagini deve disporre delle autorizzazioni di accesso per la sottocartella in cui creerà i file di immagine.
