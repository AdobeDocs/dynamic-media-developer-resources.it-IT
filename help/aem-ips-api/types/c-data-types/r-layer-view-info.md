---
description: Proprietà della vista livello.
solution: Experience Manager
title: InfoVistaLivello
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 25199c86-1df0-41af-b210-e7668a60295e
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '46'
ht-degree: 6%

---

# [!DNL LayerViewInfo]{#layerviewinfo}

Proprietà della vista livello.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| url | `xsd:string` | URL del server immagini che rappresenta il modello. Combina `urlModifier` e `urlPostAp- plyModifier` campi. |
| urlModifier | `xsd:string` | Comandi del protocollo Image Server da applicare prima della richiesta o di `urlPostApplyModifier` comandi. |
| urlPostApplyModifier | `xsd:string` | Comandi del protocollo Image Server da applicare dopo `urlModifier` e richiedere comandi. |
