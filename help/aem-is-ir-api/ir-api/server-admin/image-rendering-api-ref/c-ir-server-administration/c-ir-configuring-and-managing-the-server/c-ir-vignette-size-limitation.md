---
description: Image Rendering applica un limite di dimensione di due megapixel per le vignettature non piramidali.
solution: Experience Manager
title: Limite dimensioni vignettatura
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '78'
ht-degree: 0%

---

# Limite dimensioni vignettatura{#vignette-size-limitation}

Image Rendering applica un limite di dimensione di due megapixel per le vignettature non piramidali.

Modifica il valore di `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se l&#39;applicazione richiede il supporto per vignettature non piramidali con un&#39;area immagine (larghezza x altezza) superiore a questo limite.

>[!NOTE]
>
>`attribute::MaxPix` e `IS::MaxMessageSize` potrebbe essere necessario regolare anche per consentire dimensioni dell&#39;immagine di risposta insolitamente grandi. Per ulteriori informazioni, consulta la documentazione di Image Server.
