---
title: Callback di eventi
description: Callback di eventi
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 14b317ab-82fb-4f55-babe-72c24e6afc2c
source-git-commit: d5f1f05c36c1cb8a57b5a4bb8a9d066c20e32e75
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---

# Callback di eventi{#event-callbacks}

Il visualizzatore supporta i callback di eventi JavaScript utilizzati dalla pagina web per tenere traccia del processo di inizializzazione del visualizzatore o del suo comportamento in fase di esecuzione.

I gestori di callback vengono assegnati trasmettendo i nomi degli eventi e le funzioni di gestore corrispondenti con `handlers` proprietà a `config` Oggetto JSON nel costruttore del visualizzatore. In alternativa, è possibile utilizzare `setHandlers()` metodo API.

Gli eventi visualizzatore supportati includono:

* `initComplete` : si attiva quando l’inizializzazione del visualizzatore è completa e tutti i componenti interni vengono creati, in modo che sia possibile utilizzare `getComponent()` API. Il gestore di callback non accetta argomenti.

* `trackEvent` : viene attivato ogni volta che si verifica un evento all’interno del visualizzatore che può essere gestito da un sistema di tracciamento degli eventi, come Adobe Analytics. Il gestore di callback utilizza gli argomenti seguenti:

   * `objID {String}` non attualmente in uso.
   * `compClass {String}` non attualmente in uso.
   * `instName {String}` un nome di istanza del componente SDK del visualizzatore che ha attivato l’evento.
   * `timeStamp {Number}` timestamp dell’evento.
   * `eventInfo {String}` payload dell’evento.

Vedi anche [BasicZoomViewer](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-basiczoomviewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-sethandlers.md#reference-b748b29eaafa463a9d1723cb7b86f0d9).
