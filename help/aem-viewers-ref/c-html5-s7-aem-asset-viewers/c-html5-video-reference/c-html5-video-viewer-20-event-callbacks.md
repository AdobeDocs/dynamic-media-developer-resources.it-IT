---
description: Callback degli eventi
solution: Experience Manager
title: Callback degli eventi
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 0%

---


# Callback evento{#event-callbacks}

Il visualizzatore supporta i callback di eventi JavaScript utilizzati dalla pagina web per tenere traccia del processo di inizializzazione del visualizzatore o del comportamento di runtime.

I gestori di callback vengono assegnati passando i nomi degli eventi e le corrispondenti funzioni del gestore con la proprietà `handlers` all&#39;oggetto JSON `config` nel costruttore del visualizzatore. In alternativa, è possibile utilizzare il metodo API `setHandlers()`.

Gli eventi del visualizzatore supportati includono:

* `initComplete` - viene attivato quando l’inizializzazione del visualizzatore è completa e vengono creati tutti i componenti interni, in modo da poter utilizzare l’ `getComponent()` API. Il gestore di callback non accetta argomenti.

* `trackEvent` - viene attivato ogni volta che si verifica un evento all’interno del visualizzatore che può essere gestito da un sistema di tracciamento degli eventi, ad esempio Adobe Analytics. L&#39;handler di callback accetta i seguenti argomenti:

   * `objID {String}` attualmente non utilizzato.
   * `compClass {String}` attualmente non utilizzato.
   * `instName {String}` un nome di istanza del componente SDK per visualizzatori che ha attivato l’evento.
   * `timeStamp {Number}` marca temporale dell&#39;evento.
   * `eventInfo {String}` payload dell’evento.

Vedere anche [VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
