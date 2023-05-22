---
title: Utilizzo della libreria Immagine reattiva
description: La procedura seguente illustra come aggiungere una libreria di immagini reattive a una pagina web e gestire le immagini esistenti con la libreria.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 0%

---

# Utilizzo della libreria Immagine reattiva{#using-responsive-image-library}

La procedura seguente illustra come aggiungere una libreria di immagini reattive a una pagina web e gestire le immagini esistenti con la libreria.

**Per utilizzare la libreria Immagine reattiva**

1. In Dynamic Media Classic, [creare un predefinito immagine](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) se intendi utilizzare la libreria Immagine reattiva con i predefiniti.

   Quando definisci i predefiniti immagine da utilizzare con la Libreria immagini reattiva, non utilizzare impostazioni che influiscono sulle dimensioni dell’immagine, ad esempio `wid=`, `hei=`, o `scl=`. Non specificare alcun campo di dimensione nel predefinito immagine. Lasciali invece vuoti.
1. Aggiungi il file JavaScript della libreria alla pagina web.

   Prima di poter utilizzare l’API della libreria, assicurati di includere: `responsive_image.js`. Questo file JavaScript si trova in `libs/` sottocartella della distribuzione standard IS-Viewers:

   `<s7viewers_root>/libs/responsive_image.js`
1. Configura le immagini esistenti.

   La libreria legge alcuni attributi di configurazione da un’istanza di immagine con cui sta lavorando. Definisci gli attributi prima di `s7responsiveImage` La funzione API è chiamata per tale immagine.

   Si consiglia inoltre di inserire l’URL dell’immagine esistente nel `data-src` attributo. Quindi, imposta il `src` per avere un’immagine GIF 1x1 codificata come URI dati. In questo modo, riduce il numero di richieste HTTP inviate dalla pagina web al momento del caricamento. Tuttavia, se è necessario l’ottimizzazione SEO (Search Engine Optimization), è meglio impostare un’ `title` sull&#39;istanza dell&#39;immagine.

   Di seguito è riportato un esempio di definizione `data-breakpoints` per l’immagine e utilizzando un GIF 1x1 codificato come URI dati:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Chiama il `s7responsiveImage` Funzione API per ogni istanza di immagine gestita dalla libreria.

   Chiama il `s7responsiveImage` Funzione API per ogni istanza di immagine gestita dalla libreria. Dopo una chiamata di questo tipo, la libreria sostituisce l’immagine originale con l’immagine scaricata da Image Server in base alle dimensioni di esecuzione della `IMG` nel layout della pagina web e la densità dello schermo del dispositivo.

   Il codice che segue è un esempio di chiamata `s7responsiveImage` funzione API su un’immagine, supponendo che `responsiveImage` è un ID di quell’immagine:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Esempio {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

La libreria supporta l’utilizzo simultaneo di più istanze di immagini sulla pagina web. Ripeti quindi i passaggi 1 e 2 precedenti per ogni immagine che desideri gestire con la libreria.

È responsabilità della pagina web applicare uno stile all’elemento immagine per renderlo di dimensioni flessibili. La libreria Immagine reattiva di per sé non distingue tra immagini di dimensioni fisse e immagini &quot;fluide&quot;. Se applicata a un’immagine a dimensione fissa, la nuova immagine viene caricata una sola volta.

Il codice seguente è un esempio completo di una pagina web banale con una singola immagine fluida gestita dalla libreria Immagine reattiva. L’esempio contiene uno stile CSS aggiuntivo per rendere l’immagine &quot;reattiva&quot; alle dimensioni della finestra del browser web:

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

**Utilizzo di Ritaglio avanzato**

In AEM 6.4 e Dynamic Media Viewers 5.9 sono disponibili due modalità di ritaglio avanzato:

* **Manuale** : i punti di interruzione definiti dall&#39;utente e i comandi Image Service corrispondenti vengono definiti all&#39;interno di un attributo nell&#39;elemento immagine.
* **Ritaglio avanzato** : le rappresentazioni con ritaglio avanzato calcolate vengono recuperate automaticamente dal server di consegna. La rappresentazione migliore viene selezionata utilizzando le dimensioni di runtime dell’elemento immagine.

Per utilizzare la modalità Ritaglio avanzato, impostare `data-mode` attribuire a `smart crop`. Ad esempio:

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

L’elemento immagine associato invia un `s7responsiveViewer` evento durante il runtime quando cambia il punto di interruzione.

```javascript {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
