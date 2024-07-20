---
description: I file di dati di origine di Image Rendering includono file di vignettatura, file di materiale (immagini per texture e decalcomanie ripetibili, file di stile per cabinet e finestre) e profili ICC.
solution: Experience Manager
title: Dati Source
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# Dati Source{#source-data}

I file di dati di origine di Image Rendering includono file di vignettatura, file di materiale (immagini per texture e decalcomanie ripetibili, file di stile per cabinet e finestre) e profili ICC.

Tutti i file di dati di origine devono essere accessibili al componente codice nativo di Image Rendering (che si trova in co-posizione con il server immagini).

Se è coinvolto un catalogo dei materiali, il file specificato nel catalogo dei materiali (con `vignette::Path`, `catalog::Path` o `icc::ProfilePath`) viene cercato dal server di rendering come segue:

* Se il percorso è assoluto, viene utilizzato così come è.
* Se il percorso è relativo, viene aggiunto il prefisso `catalog::RootPath` (da un catalogo di materiali con nome).
* Se il percorso è assoluto, viene utilizzato; in caso contrario, viene aggiunto il prefisso `default::RootPath` (dal catalogo predefinito).
* Se il percorso è assoluto, viene utilizzato. In caso contrario, il server lo combina con il percorso specificato in [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Se il percorso è ora assoluto, verrà utilizzato; in caso contrario, verrà considerato relativo a [!DNL *[!DNL install_folder]*].

Se non è coinvolto alcun catalogo di immagini, il percorso viene combinato con `default::RootPath` e quindi elaborato come sopra.

Il percorso fisico dei file di dati di origine viene in genere specificato con [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). È possibile specificare più valori per consentire la distribuzione dei file di dati di origine tra più file system. Il server di rendering tenta ogni percorso nell&#39;ordine specificato finché non viene trovato il file di dati.

È possibile aggiungere nuovi file di dati di qualsiasi tipo in qualsiasi momento senza arrestare il server.
