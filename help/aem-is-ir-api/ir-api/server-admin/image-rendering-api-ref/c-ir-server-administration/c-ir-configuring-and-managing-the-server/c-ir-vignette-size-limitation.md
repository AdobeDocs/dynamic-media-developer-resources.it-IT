---
title: Limite dimensioni vignettatura
description: Image Rendering applica un limite di dimensione di due megapixel per le vignettature non piramidali.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# Limite dimensioni vignettatura{#vignette-size-limitation}

Image Rendering applica un limite di dimensione di due megapixel per le vignettature non piramidali.

Modifica il valore di `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se l&#39;applicazione richiede il supporto per vignettature non piramidali con un&#39;area immagine (larghezza x altezza) superiore a questo limite.

>[!NOTE]
>
>Regolare gli attributi `attribute::MaxPix` e `IS::MaxMessageSize` per consentire dimensioni di immagine di risposta insolitamente grandi. Per ulteriori informazioni, consulta la documentazione di Image Server.
