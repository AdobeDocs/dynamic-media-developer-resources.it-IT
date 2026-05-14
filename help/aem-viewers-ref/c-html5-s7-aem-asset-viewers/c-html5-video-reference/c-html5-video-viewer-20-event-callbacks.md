---
title: Callback di eventi
description: Callback di eventi
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 2493208b-9030-49fa-b1fd-2f2bd524bce6
TQID: 'https://experienceleague.adobe.com/-P5-isdXSmYHGdRQ6Ao1hUvsqfuHRG0xgkoe2Qr9mG8'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 147
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

Vedere anche [VideoViewer](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-videoviewer.md#reference-bfad5aa071c74a66a23c39a9b48dedb0) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-javascriptapiref/r-html5-video-viewer-20-javascriptapiref-sethandlers.md#reference-22b373b37e8943a7be5c4d4cc21ed926).
