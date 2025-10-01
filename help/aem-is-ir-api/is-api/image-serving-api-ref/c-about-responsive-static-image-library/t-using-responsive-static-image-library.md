---
title: Utilizzo della libreria Immagine reattiva
description: La procedura seguente illustra come aggiungere una libreria di immagini reattive a una pagina web e gestire le immagini esistenti con la libreria.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Utilizzo della libreria Immagine reattiva{#using-responsive-image-library}

La procedura seguente illustra come aggiungere una libreria di immagini reattive a una pagina web e gestire le immagini esistenti con la libreria.

**Per utilizzare la libreria Immagine reattiva**

1. In Dynamic Media Classic, [crea un predefinito immagine](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html?lang=it#image-sizing) se intendi utilizzare la libreria Immagine reattiva con i predefiniti.

   Quando definisci i predefiniti immagine da utilizzare con la Libreria immagini reattiva, non utilizzare impostazioni che influiscono sulla dimensione dell&#39;immagine, ad esempio `wid=`, `hei=` o `scl=`. Non specificare alcun campo di dimensione nel predefinito immagine. Lasciali invece vuoti.
1. Aggiungi il file JavaScript della libreria alla pagina web.

   Prima di poter utilizzare l&#39;API della libreria, accertarsi di includere `responsive_image.js`. Questo file JavaScript si trova nella sottocartella `libs/` della distribuzione standard IS-Viewers:

   `<s7viewers_root>/libs/responsive_image.js`
1. Configura le immagini esistenti.

   La libreria legge alcuni attributi di configurazione da un’istanza di immagine con cui sta lavorando. Definire gli attributi prima che venga chiamata la funzione API `s7responsiveImage` per tale immagine.

   Si consiglia inoltre di inserire l&#39;URL dell&#39;immagine esistente nell&#39;attributo `data-src`. Quindi, impostare l&#39;attributo `src` esistente in modo che un&#39;immagine GIF 1x1 sia codificata come URI dati. In questo modo, riduce il numero di richieste HTTP inviate dalla pagina web al momento del caricamento. Tuttavia, se è necessario l&#39;ottimizzazione SEO (Search Engine Optimization), è meglio impostare un attributo `title` sull&#39;istanza dell&#39;immagine.

<!--
   The following is an example of defining `data-breakpoints` attribute for the image and using a 1x1 GIF encoded as Data URI:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```
-->

1. Chiamare la funzione API `s7responsiveImage` per ogni istanza di immagine gestita dalla libreria.

   Chiamare la funzione API `s7responsiveImage` per ogni istanza di immagine gestita dalla libreria. Dopo tale chiamata, la libreria sostituisce l&#39;immagine originale con l&#39;immagine scaricata da Image Server in base alle dimensioni di runtime dell&#39;elemento `IMG` nel layout della pagina Web e alla densità dello schermo del dispositivo.

   Il codice seguente è un esempio di chiamata della funzione API `s7responsiveImage` su un&#39;immagine, supponendo che `responsiveImage` sia un ID dell&#39;immagine:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Esempio {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

La libreria supporta l’utilizzo simultaneo di più istanze di immagini sulla pagina web. Ripeti quindi i passaggi 1 e 2 precedenti per ogni immagine che desideri gestire con la libreria.

È responsabilità della pagina web applicare uno stile all’elemento immagine per renderlo di dimensioni flessibili. La libreria Immagine reattiva di per sé non distingue tra immagini di dimensioni fisse e immagini &quot;fluide&quot;. Se applicata a un’immagine a dimensione fissa, la nuova immagine viene caricata una sola volta.

<!--
The following code is a complete example of a trivial web page that has a single fluid image managed by the Responsive Image library. The example contains extra CSS styling to make the image "responsive" to the web browser window size:

```html {.line-numbers}
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
-->

**Utilizzo di ritaglio avanzato**

In AEM 6.4 e Dynamic Media Viewers 5.9 sono disponibili due modalità di ritaglio avanzato:

* **Manuale**: i punti di interruzione definiti dall&#39;utente e i comandi del servizio immagini corrispondenti sono definiti all&#39;interno di un attributo nell&#39;elemento immagine.
* **Ritaglio avanzato** - le rappresentazioni di ritaglio avanzato calcolate vengono recuperate automaticamente dal server di consegna. La rappresentazione migliore viene selezionata utilizzando le dimensioni di runtime dell’elemento immagine.

Per utilizzare la modalità Ritaglio avanzato, impostare l&#39;attributo `data-mode` su `smart crop`. Ad esempio:

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

L&#39;elemento immagine associato invia un evento `s7responsiveViewer` durante il runtime quando cambia il punto di interruzione.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
