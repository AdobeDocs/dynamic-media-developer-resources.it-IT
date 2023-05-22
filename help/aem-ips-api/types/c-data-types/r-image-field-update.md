---
description: Aggiorna il campo immagine associato a una risorsa immagine.
solution: Experience Manager
title: ImageFieldUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82bc016b-8a2b-4811-a0b4-1e2a93add3b6
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '56'
ht-degree: 5%

---

# [!DNL ImageFieldUpdate]{#imagefieldupdate}

Aggiorna il campo immagine associato a una risorsa immagine.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| assetHandle | `xsd:string` | Handle risorsa. |
| [!DNL resolution] | `xsd:double` | Risoluzione immagine in pixel per pollice. |
| [!DNL anchorX] | `xsd:int` | Ancoraggio immagine asse X. |
| [!DNL anchorY] | `xsd:int` | Ancoraggio immagine asse Y. |
| [!DNL userData] | `xsd:string` | Valore di `userData` campo di metadati, pubblicato nel campo del catalogo dati utente di image server. |
