---
description: Gli attributi di configurazione sono definiti come attributi direttamente su un elemento IMG gestito dalla libreria di immagini reattive. Ogni immagine può avere un proprio set di attributi.
seo-description: Gli attributi di configurazione sono definiti come attributi direttamente su un elemento IMG gestito dalla libreria di immagini reattive. Ogni immagine può avere un proprio set di attributi.
seo-title: Riferimento comando - Attributi di configurazione
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
topic: Scene7 Image Serving - Image Rendering API
uuid: a3d52680-2a28-40c8-9b5f-b1c252c88e4d
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---


# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Gli attributi di configurazione sono definiti come attributi direttamente su un elemento IMG gestito dalla libreria di immagini reattive. Ogni immagine può avere un proprio set di attributi.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Facoltativo.

URL dell’immagine trasmessa da Image Server. Se l&#39;URL non è presente, la libreria utilizza il valore impostato nell&#39;attributo `src` come fall back. Questo attributo serve l’immagine iniziale e l’immagine dinamica che la libreria di immagini reattive gestisce da diverse posizioni.

**Esempio**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Se `data-src` è impostato, `src` è facoltativo e può contenere qualsiasi URL da aggiungere. Ad esempio, può contenere un URL alla stessa immagine basata su Image Server utilizzata dalla libreria. Oppure può contenere un segnaposto GIF o anche un URI dati per evitare un ulteriore ciclo di lavoro del server all’avvio.

Se `data-src` non è impostato, `src` è obbligatorio e deve contenere un URL per l’immagine fornita da Image Server.

**Esempio**

Utilizzo dell&#39;URI dati per l&#39;attributo `src` e dell&#39;URL Image Server per l&#39;attributo `data-src`:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## punti di interruzione dei dati {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Un elenco di punti di interruzione separati da virgole seguito facoltativamente da due punti ( `:`) e da comandi Image Server o predefiniti per immagini. Ogni punto di interruzione è un valore di larghezza immagine definito in pixel CSS logici. La libreria carica l&#39;immagine con il valore più vicino dall&#39;elenco e la ridimensiona sul client in modo che corrisponda alla larghezza dell&#39;immagine CSS in fase di esecuzione. (Se lavorate su uno schermo ad alta densità, le rappresentazioni di immagini caricate dal server rappresentano i valori dei punti di interruzione moltiplicati per il rapporto pixel del dispositivo).

Per qualsiasi punto di interruzione dell’elenco, è possibile definire uno o più comandi Image Server o nomi di predefiniti per immagini. Tali parametri aggiuntivi vengono applicati solo all&#39;immagine nel caso in cui questo particolare punto di interruzione sia attivo.

È possibile utilizzare qualsiasi comando di Image Server supportato, ad eccezione dei comandi di visualizzazione che influiscono sulle dimensioni dell&#39;immagine della risposta, come `wid=`, `hei=` o `scl=`. La stessa limitazione si applica ai predefiniti per immagini: un predefinito per immagini usato con la libreria di immagini reattive non deve contenere tali comandi.

Più comandi Image Server o nomi di predefiniti per immagini sono separati dal carattere &quot; `&`&quot;. Se il valore di un comando Image Server contiene una virgola, tale virgola viene sostituita con `%2C`. I nomi dei predefiniti per immagini sono racchiusi tra simboli di dollaro ( `$`).

**Esempi**

**Uso dei soli punti di interruzione**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Utilizzo dei comandi Image Server**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Utilizzo dei predefiniti per immagini**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Utilizzo dei predefiniti per immagini e dei comandi Image Server**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## modalità dati {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Le due modalità SmartCrop seguenti sono disponibili in AEM 6.4 e versioni successive e nei visualizzatori Scene7 5.9 e versioni successive:

* **I punti di interruzione definiti dall’utente e i comandi corrispondenti del servizio immagini sono definiti all’interno di un attributo nell’elemento immagine.** 
* **Smart Crop** : le rappresentazioni di ritaglio avanzato calcolate vengono recuperate automaticamente dal server di consegna. La rappresentazione migliore viene selezionata utilizzando le dimensioni di runtime dell&#39;elemento immagine.

Per utilizzare la modalità Smart Crop, impostate l&#39;attributo `data-mode` su `smart crop`.

**Esempio**

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

