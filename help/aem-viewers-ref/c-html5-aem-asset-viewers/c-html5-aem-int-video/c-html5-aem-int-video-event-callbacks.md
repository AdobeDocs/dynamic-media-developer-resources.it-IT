---
description: Callback degli eventi
solution: Experience Manager
title: Callback degli eventi
uuid: b9252d4b-cff1-42eb-9e56-553091f854b5
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '221'
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

* `quickViewActivate` - viene attivato quando un utente fa clic o tocca un campione interattivo all’interno del componente campioni interattivi o nella schermata &quot;Invito all’azione&quot; visualizzata al termine della riproduzione del video. L&#39;handler di callback prende l&#39;unico argomento che è un oggetto JSON con i seguenti campi:

   * `sku` { `String`} valore SKU associato al campione interattivo.
   * `<additionalVariable>` {  `String`} zero o più variabili aggiuntive associate al campione interattivo.

Vedere anche [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
