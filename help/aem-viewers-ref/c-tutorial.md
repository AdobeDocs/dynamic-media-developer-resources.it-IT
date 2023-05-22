---
title: Tutorial sull’SDK per visualizzatori
description: L’SDK del visualizzatore fornisce un set di componenti basati su JavaScript per lo sviluppo di visualizzatori personalizzati. I visualizzatori sono applicazioni basate sul web che consentono di incorporare nelle pagine web i contenuti rich media gestiti da Adobe Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 3a798595-6c65-4a12-983d-3cdc53830d28
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '970'
ht-degree: 0%

---

# Tutorial sull’SDK per visualizzatori{#viewer-sdk-tutorial}

L’SDK del visualizzatore fornisce un set di componenti basati su JavaScript per lo sviluppo di visualizzatori personalizzati. I visualizzatori sono applicazioni basate sul web che consentono di incorporare nelle pagine web i contenuti rich media gestiti da Adobe Dynamic Media.

Ad esempio, l&#39;SDK fornisce zoom e panning interattivi. Inoltre, fornisce una visualizzazione a 360° e la riproduzione video delle risorse caricate in Adobe Dynamic Media tramite l’applicazione back-end denominata Dynamic Media Classic.

Anche se i componenti si basano sulla funzionalità HTML5, sono progettati per funzionare su dispositivi e desktop iOS Android™ e Apple, tra cui Internet Explorer e versioni successive. Questo tipo di esperienza ti consente di fornire un unico flusso di lavoro per tutte le piattaforme supportate.

L’SDK è costituito da componenti dell’interfaccia utente che compongono il contenuto del visualizzatore. Puoi assegnare a questi componenti uno stile CSS o componenti non dell’interfaccia utente che dispongono di un certo tipo di ruolo di supporto, ad esempio recupero, analisi e tracciamento delle definizioni dei set. Tutti i comportamenti dei componenti sono personalizzabili tramite modificatori che possono essere specificati in vari modi, ad esempio come `name=value` nell&#39;URL.

Questo tutorial include il seguente ordine di attività per aiutarti a creare un visualizzatore di zoom di base:

* [Scarica l’SDK del visualizzatore più recente da Adobe Developer Connection](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Caricare l’SDK del visualizzatore](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Aggiunta di stile al visualizzatore](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [Inclusione di Container e ZoomView](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Aggiunta di componenti MediaSet e Campioni al visualizzatore](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Aggiunta di pulsanti al visualizzatore](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [Configurazione dei campioni in verticale](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Scarica l’SDK del visualizzatore più recente da Adobe Developer Connection {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Scarica l’SDK del visualizzatore più recente da Adobe Developer Connection <!-- SDK NO LONGER AVAILABLE TO DOWNLOAD;DOUBLE CHECK WITH AMIT. THIS ENTIRE TOPIC IS LIKELY OBSOLETE. [here](https://marketing.adobe.com/developer/devcenter/scene7/show) -->.

   >[!NOTE]
   >
   >Puoi completare questa esercitazione senza scaricare il pacchetto SDK del visualizzatore, perché l’SDK viene caricato in remoto. Tuttavia, il pacchetto Visualizzatore include ulteriori esempi e una guida di riferimento API che possono essere utili per creare visualizzatori personalizzati.

## Caricare l’SDK del visualizzatore {#section-98596c276faf4cf79ccf558a9f4432c6}

1. Per iniziare, imposta una nuova pagina per sviluppare il visualizzatore zoom di base che stai per creare.

   Considera questa nuova pagina come il codice Bootstrap (o caricatore) utilizzato per impostare un’applicazione SDK vuota. Apri l’editor di testo preferito e incolla il seguente markup HTML:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
       <head> 
           <meta http-equiv="Content-Type" content="text/html; charset=utf-8" /> 
           <meta name="viewport" content="user-scalable=no, height=device-height, width=device-width, initial-scale=1.0, maximum-scale=1.0"/> 
   
           <!-- Hiding the Safari on iPhone OS UI components --> 
           <meta name="apple-mobile-web-app-capable" content="yes"/> 
           <meta name="apple-mobile-web-app-status-bar-style" content="black"/> 
           <meta name="apple-touch-fullscreen" content="no"/> 
   
           <title>Custom Viewer</title> 
   
           <!-- 
               Include Utils.js before you use any of the SDK components. This file  
               contains SDK utilities and global functions that are used to initialize the viewer and load viewer  
               components. The path to the Utils.js determines which version of the SDK that the viewer uses. You  
               can use a relative path if the viewer is deployed on one of the Adobe Dynamic Media servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Dynamic Media servers that have the SDK  
               installed.  
           --> 
           <script language="javascript" type="text/javascript"      
                   src="http://s7d1.scene7.com/s7sdk/2.8/js/s7sdk/utils/Utils.js"></script> 
   
       </head> 
       <body> 
           <script language="javascript" type="text/javascript"> 
           </script>  
       </body> 
   </html>
   ```

   Aggiungi il seguente codice JavaScript all&#39;interno del `script` in modo da inizializzare `ParameterManager`. In questo modo puoi prepararti a creare e creare istanze di componenti SDK all’interno del `initViewer` funzione:

   ```javascript {.line-numbers}
   /* We create a self-running anonymous function to encapsulate variable scope. Placing code inside such 
      a function is optional, but this prevents variables from polluting the global object.  */ 
   (function () { 
   
       // Initialize the SDK   
       s7sdk.Util.init(); 
   
       /* Create an instance of the ParameterManager component to collect components' configuration 
          that can come from a viewer preset, URL, or the HTML page itself. The ParameterManager  
          component also sends a notification s7sdk.Event.SDK_READY when all needed files are loaded 
          and the configuration parameters are processed. The other components should never be initialized 
          outside this handler. After defining the handler for the s7sdk.Event.SDK_READY event, it 
          is safe to initiate configuration initialization by calling ParameterManager.init(). */ 
       var params = new s7sdk.ParameterManager(); 
   
       /* Event handler for s7sdk.Event.SDK_READY dispatched by ParameterManager to initialize various components of  
          this viewer. */ 
       function initViewer() { 
   
       }  
   
       /* Add event handler for the s7sdk.Event.SDK_READY event dispatched by the ParameterManager when all modifiers 
          are processed and it is safe to initialize the viewer. */ 
       params.addEventListener(s7sdk.Event.SDK_READY, initViewer, false); 
   
       /* Initiate configuration initialization of ParameterManager. */ 
       params.init(); 
   
   }());
   ```

1. Salva il file come modello vuoto. È possibile utilizzare qualsiasi nome di file desiderato.

   Utilizzerai questo file modello vuoto come riferimento quando creerai visualizzatori in futuro. Questo modello funziona localmente e quando viene distribuito da un server web.

Ora aggiungi stile al visualizzatore.

## Aggiunta di stile al visualizzatore {#section-3783125360a1425eae5a5a334867cc32}

1. Per questo visualizzatore a pagina intera che stai creando, puoi aggiungere alcuni stili di base.

   Aggiungi quanto segue `style` blocco nella parte inferiore del `head`:

   ```html {.line-numbers}
   <style> 
       html, body { 
           width: 100%; 
           height: 100%; 
       } 
       body { 
           /* Remove any padding and margin around the edges of the browser window */ 
           padding: 0; 
           margin: 0; 
   
           /* We set overflow to hidden so that scroll bars do not flicker when resizing the window */ 
           overflow: hidden; 
       } 
   </style>
   ```

Ora includi i componenti `Container` e `ZoomView`.

## Inclusione di Container e ZoomView {#section-1a01730663154a508b88cc40c6f35539}

1. Creare un visualizzatore effettivo includendo i componenti `Container` e `ZoomView`.

   Inserisci quanto segue `include` istruzioni in fondo al `<head>` element - dopo il [!DNL Utils.js] script caricato:

   ```javascript {.line-numbers}
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. Ora crea delle variabili per fare riferimento ai vari componenti dell’SDK.

   Aggiungi le seguenti variabili nella parte superiore della funzione principale anonima, appena sopra `s7sdk.Util.init()`:

   ```javascript {.line-numbers}
   var container, zoomView;
   ```

1. Inserisci quanto segue all&#39;interno di `initViewer` in modo da poter definire alcuni modificatori e creare istanze dei rispettivi componenti:

   ```javascript {.line-numbers}
   /* Modifiers can be added directly to ParameterManager instance */ 
   params.push("serverurl", "http://s7d1.scene7.com/is/image"); 
   params.push("asset", "Scene7SharedAssets/ImageSet-Views-Sample"); 
   
   /* Create a viewer container as a parent component for other user interface components that  
      are part of the viewer application and associate event handlers for resize and  
      full screen notification. The advantage of using Container as the parent is the  
      component's ability to resize and bring itself and its children to full screen. */ 
   container = new s7sdk.common.Container(null, params, "s7container"); 
   container.addEventListener(s7sdk.event.ResizeEvent.COMPONENT_RESIZE, containerResize, false); 
   
   /* Create ZoomView component */ 
   zoomView = new s7sdk.image.ZoomView("s7container", params, "myZoomView");  
   
   /* We call this to ensure all SDK components are scaled to initial conditions when viewer loads */ 
   resizeViewer(container.getWidth(), container.getHeight());
   ```

1. Per il corretto funzionamento del codice precedente, aggiungi un `containerResize` un gestore eventi e una funzione helper:

   ```javascript {.line-numbers}
   /* Event handler for s7sdk.event.ResizeEvent.COMPONENT_RESIZE events dispatched by Container to resize 
      various view components included in this viewer. */ 
   function containerResize(event) { 
       resizeViewer(event.s7event.w, event.s7event.h); 
   } 
   
   /* Resize viewer components */ 
   function resizeViewer(width, height) { 
       zoomView.resize(width, height); 
   }
   ```

1. Visualizzare l&#39;anteprima della pagina in modo da poter vedere ciò che è stato creato. La pagina avrà un aspetto simile al seguente:

   ![Esempio di un&#39;immagine per il visualizzatore](assets/viewer-1.jpg)

Ora aggiungi i componenti `MediaSet` e `Swatches` al tuo visualizzatore.

## Aggiunta di componenti MediaSet e Campioni al visualizzatore {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Per consentire agli utenti di selezionare immagini da un set, puoi aggiungere i componenti `MediaSet` e `Swatches`.

   Aggiungi i seguenti SDK includono:

   ```javascript {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Aggiorna l’elenco delle variabili con quanto segue:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches;
   ```

1. Crea istanza `MediaSet` e `Swatches` componenti all&#39;interno del `initViewer` funzione.

   Assicurati di creare un’istanza di `Swatches` istanza dopo `ZoomView` e `Container` componenti, altrimenti l&#39;ordine di sovrapposizione nasconde `Swatches`:

   ```javascript {.line-numbers}
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Ora aggiungi le seguenti funzioni del gestore eventi:

   ```javascript {.line-numbers}
   /* Event handler for the s7sdk.event.AssetEvent.NOTF_SET_PARSED event dispatched by MediaSet to 
      assign the asset to the Swatches when parsing is complete. */ 
   function onSetParsed(e) { 
   
       // set media set for Swatches to display  
       var mediasetDesc = e.s7event.asset;  
       swatches.setMediaSet(mediasetDesc); 
   
       // select the first swatch by default  
       swatches.selectSwatch(0, true);      
   } 
   
   /* Event handler for s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT events dispatched by Swatches to switch 
      the image in the ZoomView when a different swatch is selected. */ 
   function swatchSelected(event) {     
       zoomView.setItem(event.s7event.asset);  
   }
   ```

1. Posiziona i campioni nella parte inferiore del visualizzatore aggiungendo i seguenti CSS alla `style` elemento:

   ```CSS {.line-numbers}
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Visualizzare l&#39;anteprima del visualizzatore.

   I campioni si trovano in basso a sinistra nel visualizzatore. Affinché i campioni occupino l’intera larghezza del visualizzatore, aggiungi una chiamata per ridimensionarli manualmente ogni volta che l’utente ridimensiona il browser. Aggiungi quanto segue a `resizeViewer` funzione:

   ```javascript {.line-numbers}
   swatches.resize(width, swatches.getHeight());
   ```

   L&#39;aspetto del visualizzatore è ora simile a quello dell&#39;immagine seguente. Prova a ridimensionare la finestra del browser del visualizzatore e osserva il comportamento risultante.

   ![Esempio di immagine due per il visualizzatore](assets/viewer-2.jpg)

Ora aggiungi al visualizzatore i pulsanti zoom in, zoom out e zoom reset (zoom in, zoom out, zoom reset).

## Aggiunta di pulsanti al visualizzatore {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Attualmente, l’utente può eseguire lo zoom solo con gesti di clic o tocco. Pertanto, aggiungere alcuni pulsanti di base per il controllo dello zoom al visualizzatore.

   Aggiungi i seguenti componenti pulsante:

   ```CSS {.line-numbers}
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Aggiorna l’elenco delle variabili con quanto segue:

   ```javascript {.line-numbers}
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Crea istanza pulsanti nella parte inferiore di `initViewer` funzione.

   Ricorda che l’ordine è importante, a meno che non specifichi `z-index` in CSS:

   ```CSS {.line-numbers}
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. Ora definisci alcuni stili di base per i pulsanti aggiungendo quanto segue alla `style` blocca nella parte superiore del file:

   ```CSS {.line-numbers}
   /* define styles common to all button components and their sub-classes */ 
   .s7button { 
       position:absolute; 
       width: 28px; 
       height: 28px; 
       z-index:100; 
   } 
   
   /* position individual buttons*/ 
   .s7zoominbutton  { 
       top: 50px; 
       left: 50px; 
    } 
   .s7zoomoutbutton  { 
       top: 50px; 
       left: 80px; 
    } 
   .s7zoomresetbutton  { 
       top: 50px; 
       left: 110px; 
    }
   ```

1. Visualizzare l&#39;anteprima del visualizzatore. Dovrebbe essere simile al seguente:

   ![Esempio di immagine tre per il visualizzatore](assets/viewer-3.jpg)

   Ora configura i campioni in modo che siano allineati verticalmente a destra.

## Configurazione dei campioni in verticale {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. Puoi configurare i modificatori direttamente sul `ParameterManager` dell&#39;istanza.

   Aggiungi quanto segue nella parte superiore della sezione `initViewer` in modo da poter configurare `Swatches` layout miniature come riga singola:

   ```javascript {.line-numbers}
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Aggiorna la seguente chiamata di ridimensionamento all&#39;interno di `resizeViewer`:

   ```javascript {.line-numbers}
   swatches.resize(swatches.getWidth(), height);
   ```

1. Modifica quanto segue `s7swatches` regola in `ZoomViewer.css`:

   ```CSS {.line-numbers}
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. Visualizzare l&#39;anteprima del visualizzatore. Si presenta come segue:

   ![Esempio di visualizzatore: quattro immagini](assets/viewer-4.jpg)

   Il visualizzatore zoom di base è stato completato.

   Questo tutorial illustra le nozioni di base di Dynamic Media Viewer SDK. Mentre lavori con l’SDK, puoi utilizzare i vari componenti standard per creare e personalizzare facilmente le esperienze di visualizzazione per il pubblico di destinazione.
