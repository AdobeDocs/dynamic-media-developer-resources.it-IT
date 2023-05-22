---
title: Callback di eventi
description: Callback di eventi
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 24ea35c0-a0b1-4768-9336-94eb5e2d4fb2
source-git-commit: 14b9f6d3a01d47ca60710b19abfe11df1e927978
workflow-type: tm+mt
source-wordcount: '149'
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
   * `instName {String}` un nome di istanza del componente SDK del visualizzatore HTML5 che ha attivato l’evento.
   * `timeStamp {Number}` timestamp dell’evento.
   * `eventInfo {String}` payload dell’evento.

Vedi anche [Visualizzatore video360i](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-video360viewer.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-javascriptapiref/r-html5-aem-video360-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
