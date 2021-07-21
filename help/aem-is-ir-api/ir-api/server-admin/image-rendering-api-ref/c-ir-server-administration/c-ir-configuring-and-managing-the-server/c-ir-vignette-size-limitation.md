---
description: Image Rendering applica una limitazione di due Megapixel per le vignette non piramidali.
solution: Experience Manager
title: Limitazione della dimensione della vignetta
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin,User
exl-id: 69116b7f-45c0-42ed-9114-d01db3ce16be
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '83'
ht-degree: 0%

---

# Limitazione della dimensione della vignetta{#vignette-size-limitation}

Image Rendering applica una limitazione di due Megapixel per le vignette non piramidali.

Modifica il valore di `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se l&#39;applicazione richiede il supporto per vignette non piramidali con un&#39;area immagine (larghezza x altezza) maggiore di questo limite.

>[!NOTE]
>
>`attribute::MaxPix` e  `IS::MaxMessageSize` può anche essere necessario regolare per consentire dimensioni di immagine di risposta insolitamente grandi. Per ulteriori informazioni, consulta la documentazione di Image Serving .
