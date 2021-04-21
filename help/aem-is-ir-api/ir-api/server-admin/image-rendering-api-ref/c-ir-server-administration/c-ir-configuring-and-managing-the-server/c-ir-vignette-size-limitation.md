---
description: Image Rendering applica una limitazione di due Megapixel per le vignette non piramidali.
solution: Experience Manager
title: Limitazione della dimensione della vignetta
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
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

