---
description: Per aggiungere una libreria di immagini reattive a una pagina web e gestire le immagini esistenti con la libreria, completa i passaggi seguenti.
solution: Experience Manager
title: Utilizzo di una libreria di immagini reattive
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 2542b9f3-c398-4dbf-afa3-1671fc4fe72a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '558'
ht-degree: 0%

---

# Utilizzo di una libreria di immagini reattive{#using-responsive-image-library}

Per aggiungere una libreria di immagini reattive a una pagina web e gestire le immagini esistenti con la libreria, completa i passaggi seguenti.

**Per utilizzare la libreria di immagini reattive**

1. In Dynamic Media Classic, [create un predefinito immagine](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/image-sizing/setting-image-presets.html#image-sizing) nel caso in cui intendete utilizzare la libreria di immagini reattive con i predefiniti.

   Quando definisci i predefiniti per immagini utilizzati con Libreria immagini reattive, non utilizzare impostazioni che influiscano sulle dimensioni dell’immagine, ad esempio `wid=`, `hei=` o `scl=`. Non specificare campi dimensione nel predefinito immagine. Lasciali invece come valori vuoti.
1. Aggiungi il file JavaScript della libreria alla tua pagina web.

   Prima di poter utilizzare l&#39;API della libreria, assicurati di includere `responsive_image.js`. Questo file JavaScript si trova nella sottocartella `libs/` della distribuzione standard IS-Viewers:

   `<s7viewers_root>/libs/responsive_image.js`
1. Imposta le immagini esistenti.

   La libreria legge alcuni attributi di configurazione da un&#39;istanza di immagine con cui sta lavorando. Definisci gli attributi prima che la funzione API `s7responsiveImage` sia chiamata per tale immagine.

   Si consiglia inoltre di inserire l&#39;URL immagine esistente nell&#39;attributo `data-src` . Quindi, imposta l&#39;attributo esistente `src` in modo che un&#39;immagine GIF 1x1 sia codificata come URI dati. In questo modo, si riduce il numero di richieste HTTP inviate dalla pagina web al momento del caricamento. Nota, tuttavia, che se è necessario SEO (ottimizzazione per motori di ricerca), è meglio impostare un attributo `title` sull’istanza di immagine.

   Di seguito è riportato un esempio di definizione dell’attributo `data-breakpoints` per l’immagine e di utilizzo di un GIF 1x1 codificato come URI dati:

   ```
   <img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
   ```

1. Chiama la funzione API `s7responsiveImage` per ogni istanza di immagine gestita dalla libreria.

   Chiama la funzione API `s7responsiveImage` per ogni istanza di immagine gestita dalla libreria. Dopo tale chiamata, la libreria sostituisce l&#39;immagine originale con l&#39;immagine scaricata da Image Serving in base alle dimensioni di runtime dell&#39;elemento `IMG` nel layout della pagina web e alla densità dello schermo del dispositivo.

   Il codice seguente è un esempio di chiamata della funzione API `s7responsiveImage` su un&#39;immagine, supponendo che `responsiveImage` sia un ID di quell&#39;immagine:

   ```
   <script type="text/javascript"> 
    s7responsiveImage(document.getElementById("responsiveImage")); 
   </script>
   ```

## Esempio {#example-0509a0dd2a8e4fd58b5d39a0df47bd87}

La libreria supporta l’utilizzo simultaneo di più istanze di immagini sulla pagina web. Ripeti quindi i passaggi 1 e 2 di cui sopra per ogni immagine che desideri gestire dalla libreria.

È responsabilità della pagina web assegnare uno stile all’elemento immagine per renderlo flessibile nelle dimensioni. La libreria di immagini reattive non distingue tra immagini a dimensione fissa e &quot;fluide&quot;. Se applicata a un&#39;immagine a dimensione fissa, la nuova immagine viene caricata una sola volta.

Il codice seguente è un esempio completo di una pagina web banale con una singola immagine fluida gestita dalla libreria di immagini reattive. L’esempio contiene uno stile CSS aggiuntivo per rendere l’immagine &quot;reattiva&quot; alle dimensioni della finestra del browser Web:

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

Sono disponibili due modalità di ritaglio avanzato in AEM 6.4 e Dynamic Media Viewers 5.9:

* **Manuale** : i punti di interruzione definiti dall’utente e i comandi corrispondenti del Servizio immagini sono definiti all’interno di un attributo nell’elemento immagine.
* **Ritaglio avanzato** : le rappresentazioni di ritaglio avanzato calcolate vengono recuperate automaticamente dal server di consegna. Il rendering migliore viene selezionato utilizzando le dimensioni di runtime dell’elemento immagine.

Per utilizzare la modalità Ritaglio avanzato, impostate l’attributo `data-mode` su `smart crop`. Ad esempio:

```
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

L’elemento immagine associato invia un evento `s7responsiveViewer` durante il runtime quando cambia il punto di interruzione.

```
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
