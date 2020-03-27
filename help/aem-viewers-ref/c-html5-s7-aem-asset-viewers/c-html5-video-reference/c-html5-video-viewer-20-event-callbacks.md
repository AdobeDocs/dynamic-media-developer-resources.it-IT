---
description: 'null'
seo-description: 'null'
seo-title: Callback evento
solution: Experience Manager
title: Callback evento
topic: Dynamic media
uuid: 08756e93-2c6c-4c63-9dd0-c64531561d6f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Callback evento{#event-callbacks}

Il visualizzatore supporta le callback di eventi JavaScript utilizzate dalla pagina Web per monitorare il processo di inizializzazione del visualizzatore o il comportamento di runtime.

I gestori di callback vengono assegnati trasmettendo i nomi degli eventi e le corrispondenti funzioni del gestore con la `handlers` proprietà all&#39;oggetto `config` JSON nel costruttore del visualizzatore. In alternativa, è possibile utilizzare il metodo `setHandlers()` API.

Gli eventi dei visualizzatori supportati includono quanto segue:

* `initComplete` - viene attivato quando l&#39;inizializzazione del visualizzatore è completa e vengono creati tutti i componenti interni, in modo che sia possibile utilizzare l&#39; `getComponent()` API. Il gestore di callback non accetta argomenti.

* `trackEvent` - viene attivato ogni volta che si verifica un evento all&#39;interno del visualizzatore che può essere gestito da un sistema di tracciamento degli eventi, come Adobe Analytics. Il gestore di callback accetta gli argomenti seguenti:

   * `objID {String}` attualmente non utilizzato.
   * `compClass {String}` attualmente non utilizzato.
   * `instName {String}` un nome di istanza del componente SDK per visualizzatori che ha attivato l’evento.
   * `timeStamp {Number}` data e ora dell’evento.
   * `eventInfo {String}` payload di eventi.

Consultate anche [VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
