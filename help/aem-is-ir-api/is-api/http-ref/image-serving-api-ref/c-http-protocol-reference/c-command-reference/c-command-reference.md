---
description: Questa sezione descrive i comandi del protocollo HTTP.
seo-description: Questa sezione descrive i comandi del protocollo HTTP.
seo-title: Riferimento comando
solution: Experience Manager
title: Riferimento comando
topic: Scene7 Image Serving - Image Rendering API
uuid: 72c4ed61-3436-4df5-b586-77808fb1903a
translation-type: tm+mt
source-git-commit: c5bac2c6e3f3a05bf69924072c4305dbd7ba1f4f

---


# Riferimento comando{#command-reference}

Questa sezione descrive i comandi del protocollo HTTP.

**Solo** per contenuti multimediali dinamici in AEM: Oltre alle impostazioni di base delle immagini disponibili nell’interfaccia utente, [!DNL Dynamic Media] in AEM ( [!DNL Adobe Experience Manager]) sono supportate numerose modifiche avanzate alle immagini che potete specificare nel campo Modificatori **** immagini. Questi parametri sono definiti di seguito. In AEM, tuttavia, le seguenti funzionalità non sono supportate negli elementi multimediali dinamici.

* Comandi di correzione colore: `icc=` e `iccEmbed=`.
* Comandi di base per la modellazione e il rendering del testo: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` e `textPs=`.
* Comandi di localizzazione: `locale=` e `req=xlate`.
* `req=set` non è disponibile per l&#39;uso generale.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Servizi per contenuti multimediali dinamici non core: SVG, Image Rendering e Web-stampa.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Consultate anche Opzioni [predefiniti per](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/managing-image-presets.html#image-preset-options) immagini per file multimediali dinamici nella documentazione di AEM 6.5.

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
* [estensione](r-extend.md)
* [adatta](r-fit.md)
* [riflettere](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [hide](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [Id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [layer](r-layer.md)
* [locale](r-locale.md)
* [map](r-map.md)
* [mask](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_bright](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrasto](r-op-contrast.md)
* [op_develop](r-op-grow.md)
* [op_developMask](r-op-growmask.md)
* [op_developMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_sound](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
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
* [rint](r-rgn.md)
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
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
