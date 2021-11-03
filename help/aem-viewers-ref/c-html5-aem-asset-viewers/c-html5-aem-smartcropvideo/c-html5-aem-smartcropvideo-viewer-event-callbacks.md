---
description: Callback degli eventi
solution: Experience Manager
title: Callback degli eventi
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
source-git-commit: bdef251dcbb7c135d02813e9fd82e2e5e32300cc
workflow-type: tm+mt
source-wordcount: '165'
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

Vedi anche [SmartCropVideoViewer]
(../../c-html5-s7-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-smartcropvideo-viewer-javascriptapiref/r-html5-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-aem-smartcropvideo/c-html5-smartcropvideo-viewer-javascriptapiref/r-html5-smartcropvideo-viewer-javascriptapiref-smartcropvideoviewer.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
