---
description: Callback evento
solution: Experience Manager
title: Callback evento
topic: Dynamic Media
uuid: c347f178-254e-45da-b06d-394098064693
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '149'
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
   * `instName {String}` un nome di istanza del componente SDK per visualizzatori HTML5 che ha attivato l’evento.
   * `timeStamp {Number}` data e ora dell’evento.
   * `eventInfo {String}` payload di eventi.

Vedere anche [Video360Viewer](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-video360viewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
