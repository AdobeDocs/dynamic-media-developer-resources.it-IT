---
title: Callback di eventi
description: Callback di eventi
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 26f1dd99-fee9-4a71-9ec1-cfd1e29cb886
source-git-commit: 6f838470a7bdea8e8c0219e59746ec82ecd802a8
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

Vedi anche [SpinViewer](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-spinviewer.md#reference-59b70dd7b58c43059bd85e3295441195) e [setHandlers](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-javascriptapiref/r-html5-spin-viewer-javascriptapiref-sethandlers.md#reference-d2223794fb45440094e9fdb5e9b73bef).
