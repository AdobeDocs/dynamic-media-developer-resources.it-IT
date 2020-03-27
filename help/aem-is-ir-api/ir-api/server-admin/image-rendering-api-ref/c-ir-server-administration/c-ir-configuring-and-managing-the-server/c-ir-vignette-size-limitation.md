---
description: Il rendering delle immagini applica un limite di due megapixel per le vignettature non piramidali.
seo-description: Il rendering delle immagini applica un limite di due megapixel per le vignettature non piramidali.
seo-title: Limitazione dimensione vignettatura
solution: Experience Manager
title: Limitazione dimensione vignettatura
topic: Scene7 Image Serving - Image Rendering API
uuid: 218e8c7e-f313-47cb-af42-30c585d4ec12
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Limitazione dimensione vignettatura{#vignette-size-limitation}

Il rendering delle immagini applica un limite di due megapixel per le vignettature non piramidali.

Modificate il valore di `IrMaxNonPyrVignetteSize` in [!DNL *[!DNL install_root]* /ImageServing/conf /ImageServerRegistry.conf] se l&#39;applicazione richiede il supporto per vignettature non piramidali con un&#39;area immagine (larghezza x altezza) maggiore di questo limite.

>[!NOTE] {class=&quot;- topic/note &quot;}
>
>`attribute::MaxPix` e `IS::MaxMessageSize` potrebbe essere necessario regolare per consentire immagini di risposta di dimensioni insolitamente grandi. Per ulteriori informazioni, consultate la documentazione di Image Server.

