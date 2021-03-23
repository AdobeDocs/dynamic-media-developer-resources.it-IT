---
description: Imposta gli attributi su elemento radice FXG.
seo-description: Imposta gli attributi su elemento radice FXG.
seo-title: setAttr.rootElement
solution: Experience Manager
title: setAttr.rootElement
uuid: dda16612-57c7-4abe-8aa4-00e599a8ea69
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '60'
ht-degree: 1%

---


# setAttr.rootElement{#setattr-rootelement}

Imposta gli attributi su elemento radice FXG.

` setAttr.rootElement={ *[!DNL attributeName]*= *[!DNL attributeValue]*%26 *[!DNL attributeName]*= *[!DNL attributeValue]*}`

Questo comando può manipolare gli attributi dell&#39;elemento principale.

## Esempio {#section-2758a6e316c34b99b13b02147e5973bb}

Se disponiamo del seguente elemento principale:

`<Graphic version="1.0" viewHeight="692" viewWidth="792" s7:appVersion="1.0.0.11" ai:appVersion="14.0.0.367" d:id="1" xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008">`

Dopo aver applicato il comando seguente:

`setAttr.rootElement={viewHeight=300%26viewWidth=200}`

L’elemento principale viene ora modificato come segue:

`<Graphic xmlns="http://ns.adobe.com/fxg/2008" xmlns:ai="http://ns.adobe.com/ai/2008" xmlns:d="http://ns.adobe.com/fxg/2008/dt" xmlns:s7="http://ns.adobe.com/S7FXG/2008" ai:appVersion="14.0.0.367" d:id="1" s7:appVersion="1.0.0.11" version="1.0" viewHeight="300" viewWidth="200">`
