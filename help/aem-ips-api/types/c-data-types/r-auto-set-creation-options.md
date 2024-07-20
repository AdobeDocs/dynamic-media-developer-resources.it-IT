---
description: Imposta automaticamente l’elenco degli script di generazione per i processi di caricamento. Presuppone che ogni script specificato per il caricamento sia applicato a tutte le risorse caricate.
solution: Experience Manager
title: OpzioniCreazioneImpostazioneAutomatica
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e6e969be-0410-4be7-88d6-491d715fd137
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '63'
ht-degree: 4%

---

# [!DNL AutoSetCreationOptions]{#autosetcreationoptions}

Imposta automaticamente l’elenco degli script di generazione per i processi di caricamento. Presuppone che ogni script specificato per il caricamento sia applicato a tutte le risorse caricate.

Sintassi

## Parametri {#section-0302e9238dbc4704914e938f42c881e6}

| Nome | Tipo | Descrizione |
|---|---|---|
| autoSetsArray | `types:HandleArray` | La matrice di [!DNL PropertySet] gestisce la definizione degli script di generazione automatica dei set applicati durante il caricamento. |
