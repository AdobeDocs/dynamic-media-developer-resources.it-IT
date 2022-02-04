---
title: Callback degli eventi
description: Callback degli eventi
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 1a7b51c1-baa7-4ae3-b6b7-17478055a605
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Callback degli eventi{#event-callbacks}

Il visualizzatore supporta i callback di eventi JavaScript utilizzati dalla pagina web per tenere traccia del processo di inizializzazione del visualizzatore o del comportamento di runtime.

I gestori di callback vengono assegnati trasmettendo i nomi degli eventi e le corrispondenti funzioni del gestore con `handlers` proprietà di `config` Oggetto JSON nel costruttore del visualizzatore. In alternativa, è possibile utilizzare `setHandlers()` Metodo API.

Gli eventi del visualizzatore supportati includono:

* `initComplete` - si attiva quando l&#39;inizializzazione del visualizzatore è completa e vengono creati tutti i componenti interni, in modo che sia possibile utilizzare `getComponent()` API. Il gestore di callback non accetta argomenti.

* `trackEvent` - viene attivato ogni volta che si verifica un evento all’interno del visualizzatore che può essere gestito da un sistema di tracciamento degli eventi, ad esempio Adobe Analytics. L&#39;handler di callback accetta i seguenti argomenti:

   * `objID {String}` attualmente non utilizzato.
   * `compClass {String}` attualmente non utilizzato.
   * `instName {String}` un nome di istanza del componente SDK per visualizzatori che ha attivato l’evento.
   * `timeStamp {Number}` marca temporale dell&#39;evento.
   * `eventInfo {String}` payload dell’evento.

Vedi anche [MixedMediaViewer](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-mixedmediaviewer.md#reference-59b70dd7b58c43059bd85e3295441195) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-javascriptapiref/r-html5-mixedmedia-javascriptapiref-sethandlers.md#reference-09523cf4f448400b83f7906688368bf3).
