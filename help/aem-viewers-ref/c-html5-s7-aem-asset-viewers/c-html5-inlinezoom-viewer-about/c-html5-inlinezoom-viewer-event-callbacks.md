---
description: Callback evento
solution: Experience Manager
title: Callback evento
topic: Dynamic media
uuid: d98074f1-7dd9-4a7f-9ef8-ebd47b698869
translation-type: tm+mt
source-git-commit: bf5873e5a6bdb859e19b15584ba85e9c106f853b
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---


# Callback evento{#event-callbacks}

Il visualizzatore supporta le callback di eventi JavaScript utilizzate dalla pagina Web per monitorare il processo di inizializzazione del visualizzatore o il comportamento di runtime.

I gestori di callback vengono assegnati trasmettendo i nomi degli eventi e le corrispondenti funzioni del gestore con la proprietà `handlers` all&#39;oggetto JSON `config` nel costruttore del visualizzatore. In alternativa, è possibile utilizzare il metodo `setHandlers()` API.

Gli eventi dei visualizzatori supportati includono quanto segue:

* `initComplete` - viene attivato quando l&#39;inizializzazione del visualizzatore è completa e vengono creati tutti i componenti interni, in modo che sia possibile utilizzare l&#39; `getComponent()` API. Il gestore di callback non accetta argomenti.

* `trackEvent` - viene attivato ogni volta che si verifica un evento all&#39;interno del visualizzatore che può essere gestito da un sistema di tracciamento eventi, come  Adobe Analytics. Il gestore di callback accetta gli argomenti seguenti:

   * `objID {String}` attualmente non utilizzato.
   * `compClass {String}` attualmente non utilizzato.
   * `instName {String}` un nome di istanza del componente SDK per visualizzatori che ha attivato l’evento.
   * `timeStamp {Number}` data e ora dell’evento.
   * `eventInfo {String}` payload di eventi.

Vedere anche [FlyoutViewer](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-.flyoutviewer.md#reference-b99bb25606444f46b27529ff3e960b1e) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-javascriptapiref/r-html5-flyout-viewer-20-javascriptapiref-sethandlers.md#reference-74e9acb1cd0047d5bd60eea5fa5c8692).
