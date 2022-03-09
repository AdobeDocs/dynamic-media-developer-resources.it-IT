---
description: Gli attributi di configurazione sono definiti come attributi direttamente su un elemento IMG gestito dalla libreria di immagini reattive. Ogni immagine può avere un proprio set di attributi.
solution: Experience Manager
title: Riferimento comando - Attributi di configurazione
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8cc645f8-03fe-4ac7-b23f-36536b60fdf6
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Riferimento comando - Attributi di configurazione{#command-reference-configuration-attributes}

Gli attributi di configurazione sono definiti come attributi direttamente su un elemento IMG gestito dalla libreria di immagini reattive. Ogni immagine può avere un proprio set di attributi.

## data-src {#section-f52ff0f139604447a870abe6e1c03444}

Facoltativo.

URL dell&#39;immagine fornita da Image Server. Se l&#39;URL non è presente, la libreria utilizza il valore impostato in `src` come valore precedente. Questo attributo serve l’immagine iniziale e l’immagine dinamica gestite dalla libreria di immagini reattive da diverse posizioni.

**Esempio**

```
<img data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## src {#section-5dbc1f9a3c274705adb9702e4c7af0b1}

Se `data-src` è impostato, `src` è facoltativo e può contenere qualsiasi URL da aggiungere. Ad esempio, può contenere un URL della stessa immagine basata su Image Server utilizzata dalla libreria. Oppure può contenere un segnaposto GIF o persino un URI dati per evitare un ulteriore viaggio di andata e ritorno del server all&#39;avvio.

Se `data-src` non è impostato, `src` è obbligatorio e deve contenere un URL dell’immagine fornita da Image Server.

**Esempio**

Utilizzo dell’URI dati per il `src` e l&#39;URL di Image Server per `data-src` attributo:

```
<img src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" data-src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720,940">
```

## punti di interruzione dei dati {#section-3bf62a89ff3e40569848c1fe3ac7886c}

Elenco di punti di interruzione separati da virgole seguito facoltativamente da due punti ( `:`) e i comandi Image Server o Image Preset. Ogni punto di interruzione è un valore di larghezza dell’immagine definito in pixel CSS logici. La libreria carica l’immagine con il valore più vicino dall’elenco e la ridimensiona sul client in modo che corrisponda alla larghezza dell’immagine CSS di runtime. (Se si lavora su uno schermo ad alta densità, le rappresentazioni di immagini caricate dal server rappresentano valori di punto di interruzione moltiplicati per il rapporto pixel del dispositivo).

Per qualsiasi punto di interruzione dall’elenco, è possibile definire uno o più comandi Image Serving o nomi di predefiniti immagine. Tali parametri aggiuntivi vengono applicati solo all’immagine nel caso in cui questo particolare punto di interruzione sia attualmente attivo.

È possibile utilizzare qualsiasi comando Image Serving supportato, ad eccezione dei comandi di visualizzazione che influiscono sulle dimensioni dell&#39;immagine di risposta, come `wid=`, `hei=`oppure `scl=`. La stessa restrizione si applica ai predefiniti immagine: un predefinito per immagini utilizzato con la libreria di immagini reattive non deve contenere tali comandi.

I nomi di più comandi Image Server o di predefiniti immagine sono separati con &quot; `&`&quot; carattere. Se un comando Image Server ha una virgola nel suo valore, tale virgola viene sostituita con `%2C`. I nomi dei predefiniti per immagini sono racchiusi in simboli di dollaro ( `$`).

**Esempi**

**Uso solo dei punti di interruzione**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360,720">`

**Utilizzo dei comandi Image Server**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:op_sharpen=1,720:resMode=sharp2&op_usm=0.9%2C1.0%2C8%2C0">`

**Utilizzo dei predefiniti per immagini**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:$ResponsiveImage_Low$,940:$ResponsiveImage_High$">`

**Utilizzo dei predefiniti per immagini e dei comandi Image Serving**

`<img src="https://s7d9.scene7.com/is/image/Scene7SharedAssets/Backpack_B" data-breakpoints="360:qlt=50,940:$ResponsiveImage_High$">`

## modalità dati {#section-97caf43cf5ab4ca8b1b866d8f394a9a4}

Sono disponibili le due seguenti modalità di ritaglio avanzato in AEM 6.4 e versioni successive e in Dynamic Media Viewers 5.9 e versioni successive:

* **Manuale** - i punti di interruzione definiti dall’utente e i comandi corrispondenti del servizio immagine sono definiti all’interno di un attributo nell’elemento immagine.
* **Ritaglio avanzato** - le rappresentazioni di ritaglio avanzato calcolate vengono recuperate automaticamente dal server di consegna. Il rendering migliore viene selezionato utilizzando le dimensioni di runtime dell’elemento immagine.

Per utilizzare la modalità Ritaglio avanzato è necessario impostare `data-mode` attributo a `smart crop`.

**Esempio**

```html {.line-numbers}
<img 
src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7" 
data-src="https://imageserver.com/is/image/ExampleCo/SmartCropAsset" 
data-mode="smartcrop">
```

L’elemento immagine associato invia un `s7responsiveViewer` in fase di runtime quando il punto di interruzione cambia.

```html {.line-numbers}
         responsiveImage.addEventListener("s7responsiveViewer", function (event) { 
           var s7event = event.s7responsiveViewerEvent; 
           if(s7event.type == "breakpointchanged") { 
              console.log("New width: " + s7event.width); 
              console.log("Old width: " + s7event.oldWidth); 
           } 
        });
```
