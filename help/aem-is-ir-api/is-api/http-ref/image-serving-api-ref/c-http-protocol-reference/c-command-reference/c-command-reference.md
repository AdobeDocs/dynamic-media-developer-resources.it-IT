---
title: Riferimento comando
description: Questa sezione descrive i comandi del protocollo HTTP.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 187de979d7d1f7ce92b7b4c8b7661a787ab6889f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 3%

---

# Riferimento comando{#command-reference}

Questa sezione descrive i comandi del protocollo HTTP.

>[!TIP]
>
>Provate e scoprite i vantaggi dei modificatori di immagini Dynamic Media e dell&#39;imaging avanzato con Dynamic Media [_Snapshot_](https://snapshot.scene7.com/).
>
> Snapshot è uno strumento di dimostrazione visiva, progettato per illustrare la potenza di Dynamic Media per la distribuzione di immagini ottimizzate e dinamiche. Sperimenta immagini di test o URL Dynamic Media per osservare visivamente l’output di vari modificatori di immagini Dynamic Media e ottimizzazioni Smart Imaging per i seguenti elementi:
>* Dimensione del file (con consegna WebP e AVIF)
>* Larghezza di banda di rete
>* DPR (Device Pixel Ratio, rapporto pixel dispositivo)
>
>Per scoprire quanto è facile utilizzare Snapshot, riprodurre il [Video di formazione sulle istantanee](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=en) (3 minuti e 17 secondi)


**Solo per Dynamic Media in Adobe Experience Manager** - oltre alle impostazioni di base delle immagini disponibili nell&#39;interfaccia utente, [!DNL Dynamic Media] nell&#39;AEM ( [!DNL Adobe Experience Manager]) supporta numerose modifiche avanzate delle immagini che è possibile specificare nella **Modificatori immagine** campo. Questi parametri sono definiti di seguito. Tuttavia, le seguenti funzionalità non sono supportate in Dynamic Media nell’AEM.

* Comandi di correzione colore: `icc=` e `iccEmbed=`.
* Comandi di base per la creazione di modelli e il rendering del testo: `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` e `textPs=`.
* Comandi di localizzazione: `locale=` e `req=xlate`.
* `req=set` non è disponibile per l’utilizzo generale.
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* Servizi Dynamic Media non core: SVG, Image Rendering e Web-to-Print.

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

Consulta anche Dynamic Media [Opzioni predefinito immagine](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) nella documentazione AEM 6.5.

* [allinea](r-align.md)
* [ancoraggio](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [cache](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [colore](r-color-commandref.md)
* [ritagliare](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [effetto](r-effect.md)
* [effectMask](r-effectmask.md)
* [estendere](r-extend.md)
* [adatta](r-fit.md)
* [capovolgere](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [nascondi](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [setImmagini](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [layer](r-layer.md)
* [locale](r-locale.md)
* [mappa](r-map.md)
* [maschera](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_grow](r-op-grow.md)
* [op_growMask](r-op-growmask.md)
* [op_growMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_noise](r-op-noise.md)
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
* [retto](r-rect.md)
* [req](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [rotate](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
* [dimensione](r-size-reference.md)
* [src](r-src.md)
* [modello](r-template.md)
* [text](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [tipo](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
