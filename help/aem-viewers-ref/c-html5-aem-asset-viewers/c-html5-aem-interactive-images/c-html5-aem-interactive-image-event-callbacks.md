---
description: Callback degli eventi
solution: Experience Manager
title: Callback degli eventi
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Immagini interattive
role: Developer,User
exl-id: 59b8a88e-0139-4981-bfb9-f2dc1ac2337d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 1%

---

# Callback degli eventi{#event-callbacks}

Il visualizzatore supporta i callback di eventi JavaScript utilizzati dalla pagina web per tenere traccia del processo di inizializzazione del visualizzatore o del comportamento di runtime.

I gestori di callback vengono assegnati passando i nomi degli eventi e le corrispondenti funzioni del gestore con la proprietà `handlers` all&#39;oggetto JSON `config` nel costruttore del visualizzatore. In alternativa, è possibile utilizzare il metodo API `setHandlers()`.

Gli eventi del visualizzatore supportati includono:

<table id="table_D4A2035B65B140F882F550B711BD3160"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Evento visualizzatore </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> initComplete  </span> </p> </td> 
   <td colname="col2"> <p>Attiva quando l'inizializzazione del visualizzatore è completa e vengono creati tutti i componenti interni, in modo da poter utilizzare l'API <span class="codeph"> getComponent() </span>. Il gestore di callback non accetta argomenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> trackEvent </span> </p> </td> 
   <td colname="col2"> <p> Attiva ogni volta che un evento si verifica all’interno del visualizzatore e può essere gestito da un sistema di tracciamento degli eventi, ad esempio Adobe Analytics. L'handler di callback accetta i seguenti argomenti: </p> <p> 
     <ul id="ul_8A5F409E32E94063AE8D3AB158A0E13D"> 
      <li id="li_1311D5DDD4454FBC9116BA8E2CB003B1"> <p> <span class="codeph"> objID {String}  </span> - attualmente non utilizzato. </p> </li> 
      <li id="li_C2ABD13097FA40A7B9801C0B7592FB59"> <p> <span class="codeph"> compClass {String}  </span> - attualmente non utilizzato. </p> </li> 
      <li id="li_3BE8001365714C3FAC32C9B2CFFD5DCE"> <p> <span class="codeph"> instName {String}  </span> - un nome di istanza del componente SDK del visualizzatore che ha attivato l'evento. </p> </li> 
      <li id="li_755DDE84B1CC4B4D8A3FA0C774CBA666"> <p> <span class="codeph"> timeStamp {Number}  </span> - timestamp evento. </p> </li> 
      <li id="li_05A1C45826AC4D1192CB72FE07EE4C29"> <p> <span class="codeph"> eventInfo {String}  </span> - payload evento. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> quickViewActivate  </span> </p> </td> 
   <td colname="col2"> <p> Attiva quando l'utente attiva un punto attivo a cui sono associati i dati di Visualizzazione rapida. L'handler di callback accetta il seguente argomento: </p> <p> 
     <ul id="ul_171110934BD54839B371FAD8D2AD467B"> 
      <li id="li_7B14C3BA432B43E392AC103926807E88"> <p> <span class="codeph"> dati {Object}  </span> - un oggetto JSON contenente dati dalla definizione del punto attivo. Il campo <span class="codeph"> SKU </span> è obbligatorio, mentre altri campi sono facoltativi e dipendono dalla definizione del punto attivo di origine. </p> </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

Vedere anche [InteractiveImage](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-interactiveimage.md#reference-bd16cadc0c054fafb0db4994741d47cd) e [setHandlers](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-javascriptapiref/r-html5-aem-int-image-viewer-javascriptapiref-sethandlers.md#reference-d76f126ac4354dc282e56afd49a0c643).
