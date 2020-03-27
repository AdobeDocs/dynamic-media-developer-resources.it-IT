---
description: 'null'
seo-description: 'null'
seo-title: Callback evento
solution: Experience Manager
title: Callback evento
topic: Dynamic media
uuid: 0c4c4111-5ad7-458c-afa2-d551b5987322
translation-type: tm+mt
source-git-commit: b4331c6f033903ec64f168da0b739927c6066710

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

Consultate anche [eCatalogViewer](/help/aem-viewers-ref/c-html5-s7-aem-asset-viewers/c-html5-ecatsearch-viewer-about/c-html5-ecatsearch-viewer-javascriptapiref/r-html5-ecatsearch-javascriptapiref-ecatalogsearchviewer.md) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-javascriptapiref/r-html5-ecatalog-viewer-20-javascriptapiref-sethandlers.md#reference-7858574ff5c34ce993ef4fdff741a856).
