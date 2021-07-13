---
description: Utilizzare queste impostazioni del server per le cartelle di dati di contenuto.
solution: Experience Manager
title: Cartelle dei dati di contenuto
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '229'
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
