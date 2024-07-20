---
description: Utilizza queste impostazioni del server per le cartelle di dati sul contenuto.
solution: Experience Manager
title: Cartelle di dati del contenuto
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 9aa4121f-25f8-49d0-a304-7ae756c046f5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---

# Cartelle di dati del contenuto{#content-data-folders}

Utilizza queste impostazioni del server per le cartelle di dati sul contenuto.

## IS::RootPath - Cartelle radice dati immagine {#section-5c57569514bb4d00b19de31d2e137e3b}

Posizione di tutti i dati di origine, inclusi immagini, font e profili ICC. Può trattarsi di uno o più percorsi di file assoluti relativi a *[!DNL install_folder]*, separati da punto e virgola. Se vuoto, *[!DNL install_folder]* è la radice predefinita. È possibile specificare più valori per distribuire i dati immagine in più file system. Il server immagini tenta i percorsi radice nell&#39;ordine specificato fino a quando non viene trovato il file richiesto.

## PS::staticContent.rootPath - Cartelle radice dati di contenuto statico {#section-a4f5b6942b7b4abdbf825b1f2e932cfe}

Percorso dei dati dell&#39;origine di contenuto statico che deve essere consegnato tramite il contesto [!DNL /is/static]. Può essere uno o più percorsi di file assoluti relativi a *[!DNL install_folder]*, separati da punto e virgola. Se vuoto, *[!DNL install_folder]* è la radice predefinita.

È possibile specificare più valori separati da punti e virgola per distribuire contenuti statici in più file system. In genere è impostato sugli stessi valori di `IS::RootPath`.

[!DNL Platform Server] tenta i percorsi radice nell&#39;ordine specificato finché non viene trovato il file richiesto.

>[!NOTE]
>
>Per impostazione predefinita, questo campo è impostato intenzionalmente su una posizione non esistente ( [!DNL *[!DNL install_folder]*/static]), disabilitando in modo efficace il servizio di contenuti statici.

## IS::SaveDirectory - File Salva cartella principale {#section-1c517f8d49ce4cb8b9013e520bf309c9}

Percorso della directory principale per `attribute::SavePath` (utilizzato da `req=saveToFile`). Il server immagini deve disporre delle autorizzazioni di accesso per la creazione della sottocartella in cui vengono creati i file di immagine.
