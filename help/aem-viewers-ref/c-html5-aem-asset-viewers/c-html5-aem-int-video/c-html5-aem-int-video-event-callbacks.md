---
title: Callback di eventi
description: Callback di eventi
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: af051437-28e5-416f-a61a-0abafb1814b2
TQID: 'https://experienceleague.adobe.com/pAXI43BvGyX7rM3--kuoLsAsexeM993-WKoLPCU9Zzg'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 210
ht-degree: 0%

---

# Callback di eventi{#event-callbacks}

Il visualizzatore supporta i callback di eventi di JavaScript utilizzati dalla pagina web per tenere traccia del processo di inizializzazione del visualizzatore o del suo comportamento in fase di esecuzione.

I gestori di callback vengono assegnati passando i nomi degli eventi e le funzioni corrispondenti del gestore con la proprietà `handlers` all&#39;oggetto JSON `config` nel costruttore del visualizzatore. In alternativa, è possibile utilizzare il metodo API `setHandlers()`.

Gli eventi visualizzatore supportati includono:

* `initComplete` - viene attivato al termine dell&#39;inizializzazione del visualizzatore e vengono creati tutti i componenti interni, in modo da poter utilizzare l&#39;API `getComponent()`. Il gestore di callback non accetta argomenti.
* `trackEvent` - viene attivato ogni volta che si verifica un evento all&#39;interno del visualizzatore che può essere gestito da un sistema di tracciamento degli eventi, ad esempio Adobe Analytics. Il gestore di callback utilizza gli argomenti seguenti:

   * `objID {String}` non attualmente in uso.
   * `compClass {String}` non attualmente in uso.
   * `instName {String}` un nome di istanza del componente SDK del visualizzatore che ha attivato l&#39;evento.
   * Timestamp evento `timeStamp {Number}`.
   * Payload evento `eventInfo {String}`.

* `quickViewActivate` - viene attivato quando un utente fa clic o tocca un campione interattivo all&#39;interno del componente campioni interattivi o nella schermata &quot;call to action&quot; mostrata alla fine della riproduzione video. Il gestore di callback accetta l’unico argomento che è un oggetto JSON con i campi seguenti:

   * `sku` { `String`} valore SKU associato al campione interattivo.
   * `<additionalVariable>` { `String`} zero o più variabili aggiuntive associate al campione interattivo.

Vedere anche [InteractiveVideoViewer](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-interactivevideo.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-javascriptapiref/r-html5-aem-int-video-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
