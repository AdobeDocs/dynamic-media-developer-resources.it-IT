---
title: Callback di eventi
description: Callback di eventi
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '210'
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

* `quickViewActivate` : si attiva quando un utente fa clic o tocca un campione interattivo all’interno del componente campioni interattivi o nella schermata &quot;invito all’azione&quot; visualizzata alla fine della riproduzione video. Il gestore di callback accetta l’unico argomento che è un oggetto JSON con i campi seguenti:

   * `sku` { `String`} Valore SKU associato al campione interattivo.
   * `<additionalVariable>` { `String`} zero o più variabili aggiuntive associate al campione interattivo.

Vedi anche [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
