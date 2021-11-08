---
description: Zoom Viewer è un visualizzatore di immagini che visualizza un’immagine zoomabile. Questo visualizzatore funziona con i set di immagini e la navigazione viene eseguita utilizzando i campioni. È dotato di strumenti di zoom, supporto a schermo intero, campioni e un pulsante di chiusura opzionale. È progettato per funzionare su desktop e dispositivi mobili.
keywords: reattivo
solution: Experience Manager
title: Zoom
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: fd3a1fe47da5ba26b53ea9414bfec1e4c11d7392
workflow-type: tm+mt
source-wordcount: '2397'
ht-degree: 0%

---

# Zoom{#zoom}

Zoom Viewer è un visualizzatore di immagini che visualizza un’immagine zoomabile. Questo visualizzatore funziona con i set di immagini e la navigazione viene eseguita utilizzando i campioni. È dotato di strumenti di zoom, supporto a schermo intero, campioni e un pulsante di chiusura opzionale. È progettato per funzionare su desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Tipo di visualizzatore 502.

Vedi [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilizzo del visualizzatore zoom {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore zoom rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse, CSS) scaricati dal visualizzatore in fase di esecuzione.

È possibile utilizzare il visualizzatore zoom in modalità pop-up utilizzando una pagina HTML pronta per la produzione fornita con IS-Viewers o in modalità incorporata, in cui è integrata nella pagina Web di destinazione utilizzando un’API documentata.

La configurazione e lo skin sono simili a quelli degli altri visualizzatori. Tutta la skin viene ottenuta tramite CSS personalizzati.

Vedi [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore zoom {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il visualizzatore zoom supporta i seguenti gesti touch comuni ad altre applicazioni mobili. Quando il visualizzatore non è in grado di elaborare il gesto di scorrimento rapido dell’utente, inoltra l’evento al browser web per eseguire lo scorrimento nativo della pagina. Questo tipo di funzionalità consente all’utente di navigare nella pagina anche se il visualizzatore occupa la maggior parte dell’area dello schermo del dispositivo.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Singolo tocco </p> </td> 
   <td colname="col2"> <p> Seleziona la nuova miniatura nei campioni. Nella vista principale, nasconde o rivela gli elementi dell’interfaccia utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doppio tocco </p> </td> 
   <td colname="col2"> <p> Esegue lo zoom di un livello fino a raggiungere l'ingrandimento massimo. Il doppio tocco successivo ripristina lo stato di visualizzazione iniziale del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pizzico </p> </td> 
   <td colname="col2"> <p>Ingrandisce o riduce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento orizzontale o rapido </p> </td> 
   <td colname="col2"> <p> Scorre l’elenco dei campioni nella barra dei campioni. </p> <p> Se l'immagine è in uno stato di reset e il <span class="codeph"> frametransita </span> è impostato su slide, la risorsa viene modificata con l'animazione diapositiva. Per altri <span class="codeph"> frametransita </span> il movimento esegue lo scorrimento nativo delle pagine. </p> <p> Se l'immagine viene ingrandita, l'immagine viene spostata in orizzontale. Se l’immagine viene spostata sul bordo della visualizzazione e lo scorrimento viene eseguito nella stessa direzione, il movimento esegue lo scorrimento nativo delle pagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento verticale </p> </td> 
   <td colname="col2"> <p> Se lo stato dell’immagine è reimpostato, il movimento esegue lo scorrimento nativo delle pagine. </p> <p> Quando l'immagine viene ingrandita, l'immagine viene spostata in verticale. Se l’immagine viene spostata sul bordo della visualizzazione e lo scorrimento viene eseguito nella stessa direzione, il movimento esegue lo scorrimento nativo della pagina. </p> <p> Se il movimento viene eseguito all’interno dell’area dei campioni, viene eseguito uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta sia l’input touch che l’input del mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Vedi [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporamento di un visualizzatore zoom {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, se selezionato, apre il visualizzatore in una finestra separata del browser. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere layout statico o utilizzare un design reattivo che viene visualizzato in modo diverso su diversi dispositivi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: incorporazione a dimensione fissa e design reattivo.

**Informazioni sulla modalità a comparsa**

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda separata del browser Web. Prende l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l&#39;orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` Chiamata JavaScript configurata correttamente `A` Elemento HTML o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML predefinita per la modalità operativa a comparsa. La pagina HTML predefinita è denominata `ZoomViewer.html` e si trova sotto la `html5/` sottocartella della distribuzione standard IS-Viewers come illustrato di seguito:

`<s7viewers_root>/html5/ZoomViewer.html`

Applica CSS personalizzati per ottenere un aspetto personalizzato per la pagina.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore nella nuova finestra:

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento della progettazione reattiva**

Nella modalità incorporata il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe avere già alcuni contenuti del cliente non correlati al visualizzatore. Normalmente lo spettatore occupa solo una parte del patrimonio immobiliare della pagina web.

I casi d’uso principali sono le pagine web orientate ai desktop o ai dispositivi tablet, nonché le pagine responsive progettate che regolano automaticamente il layout, a seconda del tipo di dispositivo.

L’incorporazione a dimensione fissa viene utilizzata quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questa opzione è la scelta migliore per le pagine web con layout statico.

La modalità di incorporamento della progettazione reattiva presuppone che il ridimensionamento del visualizzatore sia necessario durante il runtime a causa della modifica delle dimensioni del contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web con layout flessibile.

Nella modalità di incorporamento della progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa logica assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura laterale. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout reattivo come Bootstrap, Foundation e così via.

Se la pagina web imposta sia la larghezza che l’altezza del contenitore del visualizzatore `DIV`, il visualizzatore riempie quell’area e ha le stesse dimensioni fornite dalla pagina web. Ad esempio, incorporando il visualizzatore in una sovrapposizione modale, la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

## Incorporazione a dimensione fissa {#section-44f365e6c0dd40709467a459afa82a7f}

Per aggiungere il visualizzatore a una pagina web, effettua le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore DIV.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione di HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL ZoomViewer.js]. La [!DNL ZoomViewer.js] si trova sotto [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene servito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>Dovresti fare riferimento solo al visualizzatore principale JavaScript `include` nella pagina. Non devi fare riferimento a file JavaScript aggiuntivi nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente all’SDK di HTML5 `Utils.js` libreria caricata dal visualizzatore da `/s7viewers` percorso contestuale (cosiddetto SDK consolidato) `include`). Il motivo è che la posizione di `Utils.js` Per librerie di visualizzatori runtime simili, sono gestite completamente dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, è possibile inserire un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe le funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore DIV.

   Aggiungi un elemento DIV vuoto alla pagina in cui desideri che appaia il visualizzatore. L’ID dell’elemento DIV deve essere definito perché viene passato successivamente all’API del visualizzatore.

   Il segnaposto DIV è un elemento posizionato, il che significa che il `position` La proprietà CSS è impostata su `relative` o `absolute`.

   Di seguito è riportato un esempio di elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore.

   Questo visualizzatore visualizza le miniature quando si lavora con set di più elementi, quando le miniature dei sistemi desktop vengono posizionate sotto la visualizzazione principale. Allo stesso tempo, il visualizzatore consente lo scambio della risorsa principale in fase di esecuzione utilizzando `setAsset()` API. In qualità di sviluppatore, puoi controllare come il visualizzatore gestisce l’area delle miniature in basso, quando la nuova risorsa ha un solo elemento. È possibile mantenere intatta la dimensione del visualizzatore esterno e lasciare che la vista principale aumenti la sua altezza e occupare l&#39;area delle miniature. In alternativa, è possibile mantenere statiche le dimensioni della visualizzazione principale e comprimere l’area del visualizzatore esterno, lasciando che il contenuto della pagina web si muova verso l’alto e utilizzare il relè immobiliare a schermo libero dalle miniature.

   Per mantenere intatti i limiti del visualizzatore esterno, definisci le dimensioni del `.s7zoomviewer` classe CSS di primo livello in unità assolute. Le dimensioni in CSS possono essere posizionate direttamente sulla pagina HTML o in un file CSS per visualizzatori personalizzati, che viene successivamente assegnato a un record predefinito visualizzatore in Dynamic Media Classic o passato esplicitamente utilizzando un comando stile.

   Vedi [Personalizzazione del visualizzatore zoom](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione di una dimensione statica del visualizzatore esterno nella pagina HTML:

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Il comportamento di un visualizzatore esterno fisso è visibile nell’esempio seguente. Quando si passa da un set all’altro, le dimensioni del visualizzatore esterno non cambiano:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html)

   Per rendere statiche le dimensioni della visualizzazione principale, definisci le dimensioni del visualizzatore in unità assolute per l&#39;interno `Container` Componente SDK che utilizza `.s7zoomviewer` `.s7container` Selettore CSS, o utilizzando `stagesize` modificatore.

   Di seguito è riportato un esempio di definizione della dimensione del visualizzatore per l’interno `Container` Componente SDK in modo che l’area di visualizzazione principale non cambi le sue dimensioni quando si cambia risorsa:

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La seguente pagina demo mostra il comportamento del visualizzatore con una dimensione di visualizzazione principale fissa. Quando si passa da un set all’altro, la visualizzazione principale rimane statica e il contenuto della pagina web si sposta in verticale.

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html)

   È possibile impostare `stagesize` modificatore nel record predefinito visualizzatore in Dynamic Media Classic, oppure puoi trasmetterlo esplicitamente con il codice di inizializzazione del visualizzatore con il `params` raccolta o come chiamata API come descritto nella sezione Riferimento comando di questa Guida, come segue:

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza di `s7viewers.ZoomViewer` , passare tutte le informazioni di configurazione al relativo costruttore e chiamare `init()` su un’istanza di visualizzatore.

   Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Almeno questo oggetto deve avere `containerId` campo che contiene il nome dell’ID contenitore visualizzatore e nidificato `params` Oggetto JSON con parametri di configurazione supportati dal visualizzatore. In questo caso, il `params` L&#39;oggetto deve avere almeno l&#39;URL Image Server passato come `serverUrl` e la risorsa iniziale come `asset` parametro . L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il `init()` metodo immediatamente prima della chiusura `BODY` o sul corpo `onload()` evento.

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web per ora. Ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del `init()` metodo . Questo esempio presuppone `zoomViewer` è l’istanza del visualizzatore, `s7viewer` è il nome del segnaposto DIV, `http://s7d1.scene7.com/is/image/` è l’URL di Image Server e `Scene7SharedAssets/ImageSet-Views-Sample` è la risorsa.

   ```
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Il codice seguente è un esempio completo di una pagina web banale che incorpora il visualizzatore video con dimensioni fisse:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Incorporazione di design reattivo con altezza illimitata {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

Con l’incorporazione di design reattivo, la pagina web dispone normalmente di un layout flessibile che determina le dimensioni di runtime del contenitore del visualizzatore `DIV`. Nell’esempio seguente, si supponga che la pagina web consenta il contenitore del visualizzatore `DIV` per prendere il 40% delle dimensioni della finestra del browser web, lasciando la sua altezza senza restrizioni. Il codice HTML della pagina web sarà simile al seguente:

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html> 
```

L’aggiunta del visualizzatore a una pagina di questo tipo è simile alla procedura per l’incorporazione a dimensione fissa. L’unica differenza è che non è necessario definire esplicitamente la dimensione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell&#39;incorporazione con dimensione fissa. Aggiungi il DIV del contenitore all’esistente `"holder"` DIV Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La pagina degli esempi seguenti illustra gli utilizzi più reali dell’incorporazione di design reattivo a altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Incorporamento a dimensioni flessibili con larghezza e altezza definite {#section-3674e6c032594441a6576b7fb1de6e64}

In caso di incorporamento di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina web è diverso. Fornisce entrambe le dimensioni al `"holder"` DIV e centralo nella finestra del browser. Inoltre, la pagina web imposta le dimensioni del `HTML` e `BODY` al 100%.

```
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"></div> 
</body> 
</html> 
```

Gli altri passaggi di incorporamento sono identici ai passaggi utilizzati per incorporare design reattivo con altezza illimitata. L’esempio risultante è il seguente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
html, body { 
 width: 100%; 
 height: 100%; 
} 
.holder { 
 position: absolute; 
 left: 20%; 
 top: 20%; 
 width: 60%; 
height: 60%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative"></div> 
</div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

## Incorporazione tramite API basata su setter {#section-44e014925f24418b900696003855c0a9}

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L’utilizzo di questo costruttore API non richiede alcun parametro e i parametri di configurazione specificati utilizzano `setContainerId()`, `setParam()`e `setAsset()` Metodi API con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con l’API basata su setter:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```
