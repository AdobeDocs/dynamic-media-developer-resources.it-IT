---
description: I file di dati di origine del rendering delle immagini includono file di vignetta, file di materiale (immagini per texture e decali ripetibili, armadio e finestre che coprono file di stile) e profili ICC.
solution: Experience Manager
title: Dati di origine
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 0%

---

# Dati di origine{#source-data}

I file di dati di origine del rendering delle immagini includono file di vignetta, file di materiale (immagini per texture e decali ripetibili, armadio e finestre che coprono file di stile) e profili ICC.

Tutti i file di dati di origine devono essere accessibili al componente di codice nativo di Image Rendering (co-posizionato con il server di immagini).

Se si tratta di un catalogo di materiali, il file specificato nel catalogo di materiali (con `vignette::Path`, `catalog::Path` o `icc::ProfilePath`) viene esaminato dal server di rendering come segue:

* Se il percorso è assoluto, viene utilizzato così come è.
* Se il percorso è relativo, viene preceduto da `catalog::RootPath` (da un catalogo di materiali denominato).
* Se il percorso è assoluto, viene utilizzato; in caso contrario, viene preceduto da `default::RootPath` (dal catalogo predefinito).
* Se il percorso è assoluto, viene utilizzato; in caso contrario, il server lo combina con il percorso specificato in [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Se il percorso è ora assoluto, viene utilizzato; in caso contrario, si presume che sia relativo a [!DNL *[!DNL install_folder]*].

Se non è coinvolto alcun catalogo di immagini, il percorso viene combinato con `default::RootPath` e quindi elaborato come sopra.

La posizione fisica dei file di dati di origine viene generalmente specificata con [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). È possibile specificare più valori per consentire la distribuzione dei file di dati di origine su più file system. Il server di rendering proverà ogni percorso nell&#39;ordine specificato fino a quando il file di dati non viene trovato.

È possibile aggiungere nuovi file di dati di qualsiasi tipo in qualsiasi momento senza interrompere il server.
