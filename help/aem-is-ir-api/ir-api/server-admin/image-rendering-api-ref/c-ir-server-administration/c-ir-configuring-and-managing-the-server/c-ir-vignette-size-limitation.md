---
description: Image Rendering applica una limitazione di due Megapixel per le vignette non piramidali.
seo-description: Image Rendering applica una limitazione di due Megapixel per le vignette non piramidali.
seo-title: Limitazione della dimensione della vignetta
solution: Experience Manager
title: Limitazione della dimensione della vignetta
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 0%

---


# Limitazione delle dimensioni della vignetta{#vignette-size-limitation}

Image Rendering applica una limitazione di due Megapixel per le vignette non piramidali.

Modifica il valore di `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se l&#39;applicazione richiede il supporto per vignette non piramidali con un&#39;area immagine (larghezza x altezza) maggiore di questo limite.

>[!NOTE]
>
>`attribute::MaxPix` e  `IS::MaxMessageSize` può anche essere necessario regolare per consentire dimensioni di immagine di risposta insolitamente grandi. Per ulteriori informazioni, consulta la documentazione di Image Serving .

