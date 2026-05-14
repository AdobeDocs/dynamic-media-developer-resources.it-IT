---
description: I file di dati di origine di Image Rendering includono file di vignettatura, file di materiale (immagini per texture e decalcomanie ripetibili, file di stile per cabinet e finestre) e profili ICC.
solution: Experience Manager
title: Dati Source
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: de2d8fa2-6793-49ba-b873-adf723369cce
TQID: 'https://experienceleague.adobe.com/lvrZxGOZbo6ORttqcBhCTuYPzbiD9xei5qkRwnapIh8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 258
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
