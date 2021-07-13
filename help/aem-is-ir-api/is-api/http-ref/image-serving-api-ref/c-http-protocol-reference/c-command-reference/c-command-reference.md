---
description: Questa sezione descrive i comandi del protocollo HTTP.
solution: Experience Manager
title: Riferimento comando
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 7%

---

# Riferimento comando{#command-reference}

Questa sezione descrive i comandi del protocollo HTTP.

**Solo** per Dynamic Media in AEM: Oltre alle impostazioni di base dell’immagine disponibili nell’interfaccia utente,  [!DNL Dynamic Media] in AEM (  [!DNL Adobe Experience Manager]) supporta numerose modifiche avanzate dell’immagine che puoi specificare nel campo  **Image** Modifiersfield. Questi parametri sono definiti di seguito. Tuttavia, tieni presente che le seguenti funzionalità non sono supportate in Dynamic Media in AEM.

* Comandi di correzione del colore: `icc=` e `iccEmbed=`.
* Comandi di base per il modello e il rendering del testo: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` e `textPs=`.
* Comandi di localizzazione: `locale=` e `req=xlate`.
* `req=set` non è disponibile per l&#39;utilizzo generale.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Servizi Dynamic Media non principali: SVG, Image Rendering e Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Consulta anche Dynamic Media [Image Preset Options](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) nella documentazione di AEM 6.5.

* [allinea](r-align.md)
* [ancoraggio](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [Ritaglia](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [effetto](r-effect.md)
* [effectMask](r-effectmask.md)
* [estendere](r-extend.md)
* [adatta](r-fit.md)
* [capovolgere](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [nascondere](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [Id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [strato](r-layer.md)
* [locale](r-locale.md)
* [map](r-map.md)
* [maschera](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_bright](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrasto](r-op-contrast.md)
* [op_grow](r-op-grow.md)
* [op_growMask](r-op-growmask.md)
* [op_growMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_rumore](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opaca](r-opac.md)
* [origine](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [prospettiva](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [quantificare](r-is-http-quantize.md)
* [rect](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rassegnare](r-rgn.md)
* [rotate](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
* [size](r-size-reference.md)
* [src](r-src.md)
* [template](r-template.md)
* [Testo](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [Testo](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
