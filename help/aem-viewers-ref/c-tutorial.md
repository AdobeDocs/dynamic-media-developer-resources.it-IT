---
description: L’SDK per visualizzatori offre un set di componenti basati su JavaScript per lo sviluppo personalizzato del visualizzatore. I visualizzatori sono applicazioni basate sul Web che consentono di incorporare nelle pagine Web contenuti multimediali avanzati gestiti da Adobe Scene7.
seo-description: L’SDK per visualizzatori offre un set di componenti basati su JavaScript per lo sviluppo personalizzato del visualizzatore. I visualizzatori sono applicazioni basate sul Web che consentono di incorporare nelle pagine Web contenuti multimediali avanzati gestiti da Adobe Scene7.
seo-title: Esercitazione SDK per visualizzatori
solution: Experience Manager
title: Esercitazione SDK per visualizzatori
topic: Dynamic media
uuid: ea331f05-0c58-4e6b-b5a1-d9b8372d8e94
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Esercitazione SDK per visualizzatori{#viewer-sdk-tutorial}

L’SDK per visualizzatori offre un set di componenti basati su JavaScript per lo sviluppo personalizzato del visualizzatore. I visualizzatori sono applicazioni basate sul Web che consentono di incorporare nelle pagine Web contenuti multimediali avanzati gestiti da Adobe Scene7.

Ad esempio, l’SDK fornisce funzioni interattive di zoom e panning. Fornisce inoltre la visualizzazione a 360° e la riproduzione video delle risorse caricate in Adobe Scene7 tramite l’applicazione di back-end SPS (Scene7 Publishing System).

Anche se i componenti si basano sulla funzionalità HTML5, sono progettati per funzionare su dispositivi Android e Apple iOS e computer desktop, inclusi Internet Explorer e versioni successive. Questo tipo di esperienza consente di fornire un singolo flusso di lavoro per tutte le piattaforme supportate.

L’SDK è costituito da componenti dell’interfaccia utente che compongono il contenuto del visualizzatore. Potete formattare questi componenti tramite CSS e componenti non dell&#39;interfaccia utente che hanno un ruolo di supporto, come il recupero delle definizioni dei set, l&#39;analisi o il tracciamento. Tutti i comportamenti dei componenti possono essere personalizzati tramite modificatori che è possibile specificare in diversi modi, ad esempio, come `name=value` coppie nell’URL.

Questa esercitazione include il seguente ordine di attività per creare un visualizzatore zoom di base:

* [Scarica l’SDK visualizzatore più recente da Adobe Developer Connection](c-tutorial.md#section-84dc74c9d8e24a2380b6cf8fc28d7127)
* [Caricamento dell’SDK per visualizzatori](c-tutorial.md#section-98596c276faf4cf79ccf558a9f4432c6)
* [Aggiunta di stile al visualizzatore](c-tutorial.md#section-3783125360a1425eae5a5a334867cc32)
* [Inclusi Contenitore e Visualizzazione zoom](c-tutorial.md#section-1a01730663154a508b88cc40c6f35539)
* [Aggiunta di componenti MediaSet e Campioni al visualizzatore](c-tutorial.md#section-02b8c21dd842400e83eae2a48ec265b7)
* [Aggiunta di pulsanti al visualizzatore](c-tutorial.md#section-1fc334fa0d2b47eb9cdad461725c07be)
* [Configurazione dei campioni in verticale](c-tutorial.md#section-91a8829d5b5a4d45a35b7faeb097fcc9)

## Scarica l’SDK visualizzatore più recente da Adobe Developer Connection {#section-84dc74c9d8e24a2380b6cf8fc28d7127}

1. Scarica l’SDK per visualizzatori più recente da Adobe Developer Connection [qui](https://marketing.adobe.com/developer/devcenter/scene7/show).

   >[!NOTE]
   >
   >Puoi completare questa esercitazione senza dover scaricare il pacchetto SDK per visualizzatori, in quanto l’SDK viene caricato in remoto. Tuttavia, il pacchetto Visualizzatore include esempi aggiuntivi e una guida di riferimento API che sarà utile per creare visualizzatori personalizzati.

## Caricamento dell’SDK per visualizzatori {#section-98596c276faf4cf79ccf558a9f4432c6}

1. Per iniziare, impostate una nuova pagina per sviluppare il visualizzatore zoom di base che intendete creare.

   Considerate questo esempio come codice di avvio (o caricatore) per impostare un’applicazione SDK vuota. Aprite l’editor di testo preferito e incollate la seguente marcatura HTML:

   ```
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
               can use a relative path if the viewer is deployed on one of the Adobe Scene7 servers and it is served  
               from the same domain. Otherwise, specify a full path to one of Adobe Scene7 servers that have the SDK  
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

   Aggiungete il seguente codice JavaScript all&#39;interno del `script` tag per inizializzare il `ParameterManager`. Questo consente di prepararsi a creare e creare un&#39;istanza di componenti SDK all&#39;interno della `initViewer` funzione:

   ```
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

1. Salvate il file come modello vuoto. Potete usare il nome file desiderato.

   Questo file di modello vuoto verrà utilizzato come riferimento per la creazione di nuovi visualizzatori in futuro. Questo modello funziona localmente e quando viene servito da un server Web.

Ora potete aggiungere dello stile al visualizzatore.

## Aggiunta di stile al visualizzatore {#section-3783125360a1425eae5a5a334867cc32}

1. Per questo visualizzatore a pagina intera che state creando, potete aggiungere alcuni stili di base.

   Aggiungere il seguente `style` blocco nella parte inferiore della `head`:

   ```
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

Ora verranno inclusi i componenti `Container` e `ZoomView`.

## Inclusi Contenitore e Visualizzazione zoom {#section-1a01730663154a508b88cc40c6f35539}

1. Create un visualizzatore effettivo includendo i componenti `Container` e `ZoomView`.

   Inserite le seguenti `include` istruzioni nella parte inferiore dell&#39; `<head>` elemento, dopo che lo [!DNL Utils.js] script è stato caricato:

   ```
   <!-- 
       Add an "include" statement with a related module for each component that is needed for that particular  
       viewer. Check API documentation to see a complete list of components and their modules. 
   --> 
   <script language="javascript" type="text/javascript"> 
       s7sdk.Util.lib.include('s7sdk.common.Container');  
       s7sdk.Util.lib.include('s7sdk.image.ZoomView');  
   </script>
   ```

1. Ora create le variabili per fare riferimento ai vari componenti SDK.

   Aggiungi le seguenti variabili all&#39;inizio della funzione anonima principale, appena sopra `s7sdk.Util.init()`:

   ```
   var container, zoomView;
   ```

1. Inserite quanto segue all&#39;interno della `initViewer` funzione per definire alcuni modificatori e creare un&#39;istanza dei rispettivi componenti:

   ```
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

1. Affinché il codice riportato sopra venga eseguito correttamente, aggiungete un gestore di `containerResize` eventi e una funzione helper:

   ```
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

1. Visualizzate l’anteprima della pagina per vedere cosa avete creato. La pagina avrà l’aspetto seguente:

   ![](assets/viewer-1.jpg)

Ora potete aggiungere i componenti `MediaSet` e `Swatches` il visualizzatore.

## Aggiunta di componenti MediaSet e Campioni al visualizzatore {#section-02b8c21dd842400e83eae2a48ec265b7}

1. Per consentire agli utenti di selezionare le immagini da un set, potete aggiungere i componenti `MediaSet` e `Swatches`.

   Aggiungi il seguente SDK:

   ```
   s7sdk.Util.lib.include('s7sdk.set.MediaSet'); 
   s7sdk.Util.lib.include('s7sdk.set.Swatches');
   ```

1. Aggiorna l’elenco delle variabili con i seguenti elementi:

   ```
   var mediaSet, container, zoomView, swatches;
   ```

1. Creare un&#39;istanza `MediaSet` e `Swatches` componenti all&#39;interno della `initViewer` funzione.

   Assicuratevi di creare un&#39;istanza dopo i `Swatches` componenti `ZoomView` e `Container` , in caso contrario l&#39;ordine di sovrapposizione nasconde `Swatches`:

   ```
   // Create MediaSet to manage assets and add event listener to the NOTF_SET_PARSED event 
   mediaSet = new s7sdk.set.MediaSet(null, params, "mediaSet"); 
   
   // Add MediaSet event listener 
   mediaSet.addEventListener(s7sdk.event.AssetEvent.NOTF_SET_PARSED, onSetParsed, false); 
   
   /* create Swatches component and associate event handler for swatch selection notification */ 
   swatches = new s7sdk.set.Swatches("s7container", params, "mySwatches");   
   swatches.addEventListener(s7sdk.event.AssetEvent.SWATCH_SELECTED_EVENT, swatchSelected, false);
   ```

1. Aggiungete ora le seguenti funzioni del gestore di eventi:

   ```
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

1. Posizionate i campioni nella parte inferiore del visualizzatore aggiungendo il seguente CSS all’ `style` elemento:

   ```
   /* Align swatches to bottom of viewer */ 
   .s7swatches { 
       bottom: 0; 
       left: 0; 
       right: 0; 
       height: 150px; 
   }
   ```

1. Visualizzate l’anteprima del visualizzatore.

   I campioni si trovano nella parte inferiore sinistra del visualizzatore. Affinché i campioni possano avere l’intera larghezza del visualizzatore, aggiungete una chiamata per ridimensionare manualmente i campioni ogni volta che l’utente ridimensiona il browser. Aggiungere quanto segue alla `resizeViewer` funzione:

   ```
   swatches.resize(width, swatches.getHeight());
   ```

   Il visualizzatore ora si presenta come la seguente immagine. Provate a ridimensionare la finestra del browser del visualizzatore e notate il comportamento che ne risulta.

   ![](assets/viewer-2.jpg)

Ora potete aggiungere al visualizzatore pulsanti di zoom in, zoom out e reimpostazione zoom.

## Aggiunta di pulsanti al visualizzatore {#section-1fc334fa0d2b47eb9cdad461725c07be}

1. Al momento, l&#39;utente può effettuare lo zoom solo tramite clic o gesti touch. Aggiungete quindi al visualizzatore alcuni pulsanti di controllo dello zoom di base.

   Aggiungete i seguenti componenti pulsante:

   ```
   s7sdk.Util.lib.include('s7sdk.common.Button');
   ```

1. Aggiorna l’elenco delle variabili con i seguenti elementi:

   ```
   var mediaSet, container, zoomView, swatches, zoomInButton, zoomOutButton, zoomResetButton;
   ```

1. Creare un&#39;istanza dei pulsanti nella parte inferiore della `initViewer` funzione.

   Tenete presente che l’ordine è importante, a meno che non specifichiate il valore `z-index` in CSS:

   ```
   /* Create Zoom In, Zoom Out and Zoom Reset buttons */ 
   zoomInButton  = new s7sdk.common.ZoomInButton("s7container", params, "zoomInBtn"); 
   zoomOutButton = new s7sdk.common.ZoomOutButton("s7container", params, "zoomOutBtn"); 
   zoomResetButton = new s7sdk.common.ZoomResetButton("s7container", params, "zoomResetBtn"); 
   
   /* Add handlers for zoom in, zoom out and zoom reset buttons inline. */ 
   zoomInButton.addEventListener("click", function() { zoomView.zoomIn(); }); 
   zoomOutButton.addEventListener("click", function() { zoomView.zoomOut(); }); 
   zoomResetButton.addEventListener("click", function() { zoomView.zoomReset(); });
   ```

1. Definire ora alcuni stili di base per i pulsanti aggiungendo quanto segue al `style` blocco nella parte superiore del file:

   ```
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

1. Visualizzate l’anteprima del visualizzatore. Si presenterà come segue:

   ![](assets/viewer-3.jpg)

   Ora potete configurare i campioni in modo che siano allineati verticalmente a destra.

## Configurazione dei campioni in verticale {#section-91a8829d5b5a4d45a35b7faeb097fcc9}

1. Potete configurare i modificatori direttamente sull’ `ParameterManager` istanza.

   Aggiungete quanto segue nella parte superiore della `initViewer` funzione per configurare il layout delle `Swatches` miniature come una singola riga:

   ```
   params.push("Swatches.tmblayout", "1,0");
   ```

1. Aggiorna la seguente chiamata di ridimensionamento all&#39;interno `resizeViewer`:

   ```
   swatches.resize(swatches.getWidth(), height);
   ```

1. Modificate la seguente `s7swatches` regola in `ZoomViewer.css`:

   ```
   .s7swatches { 
       top:0 ; 
       bottom: 0; 
       right: 0; 
       width: 150px; 
   }
   ```

1. Visualizzate l’anteprima del visualizzatore. Si presenterà come segue:

   ![](assets/viewer-4.jpg)

   Il visualizzatore zoom di base è ora completo.

   Questa esercitazione sul visualizzatore illustra i principi di base di Scene7 Viewer SDK. Mentre lavori con l’SDK, puoi usare i vari componenti standard per creare e personalizzare facilmente esperienze di visualizzazione avanzate per il pubblico di destinazione.

