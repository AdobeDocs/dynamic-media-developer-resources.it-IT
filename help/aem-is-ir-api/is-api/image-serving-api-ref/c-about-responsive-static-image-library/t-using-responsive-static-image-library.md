---
description: Per aggiungere una libreria di immagini reattive a una pagina Web e gestire le immagini esistenti con la libreria, effettua i seguenti passaggi.
seo-description: Per aggiungere una libreria di immagini reattive a una pagina Web e gestire le immagini esistenti con la libreria, effettua i seguenti passaggi.
seo-title: Utilizzo della libreria di immagini reattive
solution: Experience Manager
title: Utilizzo della libreria di immagini reattive
topic: Scene7 Image Serving - Image Rendering API
uuid: 325cdc8d-2bfa-4f9b-bf88-51d1dcc6c495
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '580'
ht-degree: 0%

---


# Utilizzo della libreria di immagini reattive{#using-responsive-image-library}

Per aggiungere una libreria di immagini reattive a una pagina Web e gestire le immagini esistenti con la libreria, effettua i seguenti passaggi.

**Per utilizzare la libreria di immagini reattive**

1. In SPS, [create un predefinito per immagini](http://help.adobe.com/en_US/scene7/using/WS2F6A1049-B41F-447d-A520-91227F9CDABF.html) se intendete utilizzare la libreria di immagini reattive con dei predefiniti.

   Quando definite i predefiniti per immagini utilizzati con la libreria di immagini reattive, non usate impostazioni che influiscano sulle dimensioni dell’immagine, ad esempio `wid=`, `hei=` o `scl=`. Non specificate alcun campo dimensione nel predefinito per immagini. Lasciateli invece come valori vuoti.
1. Aggiungete il file JavaScript della libreria alla pagina Web.

   Prima di poter utilizzare l&#39;API della libreria, accertatevi di includere `responsive_image.js`. Questo file JavaScript si trova nella sottocartella `libs/` della distribuzione standard dei visualizzatori IS:

   `<s7viewers_root>/libs/responsive_image.js`
1. Configurate le immagini esistenti.

   La libreria legge alcuni attributi di configurazione da un’istanza di immagine con cui sta lavorando. Definire gli attributi prima che la funzione `s7responsiveImage` API sia chiamata per tale immagine.

   È inoltre consigliabile inserire l&#39;URL immagine esistente nell&#39;attributo `data-src`. Quindi, imposta l&#39;attributo `src` esistente in modo che un&#39;immagine GIF 1x1 venga codificata come URI dati. In questo modo, si riduce il numero di richieste HTTP inviate dalla pagina Web al momento del caricamento. Tuttavia, se è necessaria l&#39;ottimizzazione SEO (motore di ricerca), è meglio impostare un attributo `title` sull&#39;istanza dell&#39;immagine.

   Di seguito è riportato un esempio di definizione dell&#39;attributo `data-breakpoints` per l&#39;immagine e utilizzo di un GIF 1x1 codificato come URI dati:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Chiama la funzione API `s7responsiveImage` per ogni istanza di immagine gestita dalla libreria.

   Chiama la funzione API `s7responsiveImage` per ogni istanza di immagine gestita dalla libreria. Dopo tale chiamata, la libreria sostituisce l&#39;immagine originale con l&#39;immagine scaricata da Image Server in base alle dimensioni runtime dell&#39;elemento `IMG` nel layout della pagina Web e alla densità dello schermo del dispositivo.

   Il codice seguente è un esempio di chiamata della funzione API `s7responsiveImage` su un&#39;immagine, partendo dal presupposto che `responsiveImage` sia un ID dell&#39;immagine:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Esempio {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

La libreria supporta l&#39;utilizzo simultaneo di più istanze di immagini sulla pagina Web. Di conseguenza, ripetete i passaggi 1 e 2 precedenti per ogni immagine che desiderate gestire dalla libreria.

È responsabilità della pagina Web formattare l’elemento immagine per renderlo flessibile in termini di dimensioni. La libreria di immagini reattive non fa distinzione tra immagini a dimensione fissa e immagini fluide. Se applicata a un’immagine a dimensione fissa, la nuova immagine viene caricata una sola volta.

Il codice seguente è un esempio completo di una pagina Web banale con una singola immagine fluida gestita dalla libreria Immagini reattive. L’esempio contiene uno stile CSS aggiuntivo per rendere l’immagine &quot;reattiva&quot; alle dimensioni della finestra del browser Web:

```
<!DOCTYPE html> 
<html> 
 <head> 
  <style type="text/css"> 
  .container { 
   width: 50%; 
  } 
  .fluidimage { 
   max-width: 100%; 
  } 
  </style> 
 </head> 
 <body> 
  <div class="container"> 
   <img id="responsiveImage" src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="200,400,600,800" class="fluidimage"> 
  </div> 
  <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/libs/responsive_image.js"></script> 
  <script type="text/javascript"> 
   s7responsiveImage(document.getElementById("responsiveImage")); 
  </script> 
 </body> 
</html>
```

**Utilizzo del ritaglio avanzato**

Sono disponibili due modalità di ritaglio avanzato nei visualizzatori AEM 6.4 e Scene7 5.9:

* **I punti di interruzione definiti dall’utente e i comandi corrispondenti del servizio immagini sono definiti all’interno di un attributo nell’elemento immagine.** 
* **Smart Crop** : le rappresentazioni di ritaglio avanzato calcolate vengono recuperate automaticamente dal server di consegna. La rappresentazione migliore viene selezionata utilizzando le dimensioni di runtime dell&#39;elemento immagine.

Per utilizzare la modalità Smart Crop, impostate l&#39;attributo `data-mode` su `smart crop`. Ad esempio:

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

L&#39;elemento immagine associato invia un evento `s7responsiveViewer` durante il runtime quando il punto di interruzione cambia.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
