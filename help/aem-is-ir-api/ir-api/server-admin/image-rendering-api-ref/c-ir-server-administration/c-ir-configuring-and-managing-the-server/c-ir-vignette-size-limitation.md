---
title: Limitazione dimensione vignettatura
description: Immagine Rendering applica un limite di dimensioni di due megapixel per le vignettature non piramidali.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '73'
ht-degree: 0%

---

# Limitazione dimensione vignettatura{#vignette-size-limitation}

Immagine Rendering applica un limite di dimensioni di due megapixel per le vignettature non piramidali.

Modificare il valore di `IrMaxNonPyrVignetteSize` in [! DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se il applicazione richiede il supporto per vignettature non piramidali con un&#39;area dell&#39;immagine (larghezza x altezza) superiore a questo limite.

>[!NOTE]
>
>Regola gli attributi `attribute::MaxPix` e `IS::MaxMessageSize` consente di ottenere dimensioni insolitamente grandi per le immagini di risposta. Per ulteriori informazioni, consulta la documentazione di Immagine Serving.
