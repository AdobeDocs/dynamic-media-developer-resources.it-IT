---
description: Image Rendering applica una limitazione di due Megapixel per le vignette non piramidali.
solution: Experience Manager
title: Limitazione della dimensione della vignetta
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '87'
ht-degree: 0%

---


# Limitazione delle dimensioni della vignetta{#vignette-size-limitation}

Image Rendering applica una limitazione di due Megapixel per le vignette non piramidali.

Modifica il valore di `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se l&#39;applicazione richiede il supporto per vignette non piramidali con un&#39;area immagine (larghezza x altezza) maggiore di questo limite.

>[!NOTE]
>
>`attribute::MaxPix` e  `IS::MaxMessageSize` può anche essere necessario regolare per consentire dimensioni di immagine di risposta insolitamente grandi. Per ulteriori informazioni, consulta la documentazione di Image Serving .

