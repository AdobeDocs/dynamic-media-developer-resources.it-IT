---
description: I file di dati sorgente per il rendering delle immagini includono file di vignettatura, file di materiale (immagini per texture e decalcomanie ripetibili, file di stile ripiani e finestre) e profili ICC.
seo-description: I file di dati sorgente per il rendering delle immagini includono file di vignettatura, file di materiale (immagini per texture e decalcomanie ripetibili, file di stile ripiani e finestre) e profili ICC.
seo-title: Dati di origine
solution: Experience Manager
title: Dati di origine
topic: Scene7 Image Serving - Image Rendering API
uuid: 76c6419c-613e-4eff-b30f-9fea2a7daf5b
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Dati di origine{#source-data}

I file di dati sorgente per il rendering delle immagini includono file di vignettatura, file di materiale (immagini per texture e decalcomanie ripetibili, file di stile ripiani e finestre) e profili ICC.

Tutti i file di dati di origine devono essere accessibili al componente di codice nativo di Image Rendering (in co-posizione con il server immagini).

Se si tratta di un catalogo di materiali, il file specificato nel catalogo di materiali (con `vignette::Path`, `catalog::Path`o `icc::ProfilePath`) viene cercato dal server di rendering come segue:

* Se il percorso è assoluto, viene utilizzato così come è.
* Se il percorso è relativo, ha il prefisso `catalog::RootPath` (da un catalogo di materiali denominato).
* Se il percorso è assoluto, viene utilizzato; altrimenti ha il prefisso `default::RootPath` (dal catalogo predefinito).
* Se il percorso è assoluto, viene utilizzato; in caso contrario, il server lo combina con il percorso specificato in [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2).
* Se il percorso è ora assoluto, viene utilizzato; in caso contrario, si presume che sia relativo a [!DNL *[!DNL install_folder]*].

Se non è coinvolto alcun catalogo di immagini, il percorso viene combinato con `default::RootPath` e quindi elaborato come sopra.

La posizione fisica dei file di dati di origine è in genere specificata con [ir.resourceRootPaths](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-resource-root-folders.md#concept-39a34d2239934079bb396e1bf568a9c2). È possibile specificare più valori per consentire la distribuzione dei file di dati di origine tra più file system. Il server di rendering proverà ogni percorso nell&#39;ordine specificato fino a trovare il file di dati.

Nuovi file di dati di qualsiasi tipo possono essere aggiunti in qualsiasi momento senza arrestare il server.
