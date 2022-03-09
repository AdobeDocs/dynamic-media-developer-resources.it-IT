---
title: Zoom in linea
description: Il visualizzatore zoom in linea è un visualizzatore di immagini. Visualizza un'immagine statica con la versione ingrandita mostrata sopra quell'immagine statica quando un utente passa il mouse o tocca la vista principale. Questo visualizzatore funziona con i set di immagini e la navigazione viene eseguita utilizzando i campioni. È progettato per funzionare su desktop e dispositivi mobili.
keywords: reattivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Inline Zoom
role: Developer,User
exl-id: 33e661b0-be5e-4d37-af88-47f7bc433c01
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2385'
ht-degree: 0%

---

# Zoom in linea{#inline-zoom}

Il visualizzatore zoom in linea è un visualizzatore di immagini. Visualizza un&#39;immagine statica con la versione ingrandita mostrata sopra quell&#39;immagine statica quando un utente passa il mouse o tocca la vista principale. Questo visualizzatore funziona con i set di immagini e la navigazione viene eseguita utilizzando i campioni. È progettato per funzionare su desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Il tipo di visualizzatore è 504.

Vedi [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## Utilizzo del visualizzatore zoom in linea {#section-f21ac23d3f6449ad9765588d69584772}

Il visualizzatore zoom in linea rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Il visualizzatore zoom in linea può essere utilizzato sia in modalità pop-up utilizzando una pagina HTML pronta per la produzione fornita con i visualizzatori Image Serving sia in modalità incorporata, in cui è integrato in una pagina web di destinazione utilizzando un’API documentata.

La configurazione e lo skin sono simili a quelli degli altri visualizzatori. Puoi utilizzare CSS personalizzati per applicare la skin.

Vedi [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore zoom in linea {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore zoom in linea supporta gesti touch e touch singoli comuni ad altre applicazioni mobili.

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
   <td colname="col2"> <p> Attiva la visualizzazione a comparsa o le modifiche tra il livello di zoom primario e secondario nei campioni, seleziona la nuova miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento orizzontale o rapido </p> </td> 
   <td colname="col2"> <p> Scorre l’elenco dei campioni nella barra dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento verticale </p> </td> 
   <td colname="col2"> <p>Se il movimento viene eseguito all’interno dell’area dei campioni, viene eseguito uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta anche l’input touch e il mouse su dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Vedi [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione di un visualizzatore zoom in linea {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento cliccabile che apre il visualizzatore in una finestra separata del browser. In altri casi, potrebbe essere necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere layout di pagina statico o utilizzare un design reattivo che viene visualizzato in modo diverso su dispositivi diversi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: incorporazione a dimensione fissa e incorporamento dinamico.

**Pop-up**

Nella modalità a comparsa, il visualizzatore viene aperto in una finestra o scheda separata del browser Web. Prende l&#39;intera area della finestra del browser e si regola quando la finestra del browser viene ridimensionata o l&#39;orientamento del dispositivo viene modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` Chiamata JavaScript configurata correttamente `A` elemento HTML o qualsiasi altro modo appropriato.

Si consiglia di utilizzare la pagina HTML predefinita per la modalità a comparsa denominata `FlyoutViewer.html`. Si trova sotto la [!DNL html5/] sottocartella della distribuzione standard Image Server-Viewers:

`<s7viewers_root>/html5/FlyoutViewer.html`

È inoltre necessario che il componente FlyoutZoomView sia configurato per funzionare in modalità zoom in linea. Si consiglia di utilizzare il `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` predefinito per il visualizzatore zoom in linea o un predefinito personalizzato da esso derivato. È possibile personalizzare visivamente l’applicazione di CSS personalizzati.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Incorporazione a dimensione fissa e incorporamento reattivo**

Nella modalità incorporata il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe avere già alcuni contenuti del cliente non correlati al visualizzatore. Il visualizzatore normalmente occupa solo una parte del patrimonio immobiliare della pagina web.

I casi d’uso principali sono le pagine web orientate ai desktop o ai dispositivi tablet, nonché le pagine web reattive che regolano automaticamente il layout in base al tipo di dispositivo.

La modalità di incorporamento a dimensione fissa viene utilizzata quando il visualizzatore non modifica le dimensioni dopo il caricamento iniziale. Questa opzione è ideale per le pagine web con layout di pagina statico.

La modalità di incorporamento della progettazione reattiva presuppone che il visualizzatore debba ridimensionare durante il runtime in risposta alla modifica delle dimensioni del suo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

Quando si utilizza la modalità di incorporamento del design reattivo con il visualizzatore zoom in linea, assicurarsi di specificare punti di interruzione espliciti per l’immagine della vista principale utilizzando il `imagereload` parametro . Se lo desideri, abbina i tuoi punti di interruzione con i punti di interruzione della larghezza del visualizzatore come indicato dal CSS della pagina web.

Nella modalità di incorporamento della progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui è contenuto un contenitore di pagina web `DIV` è dimensionato. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Grazie a questa funzionalità, la risorsa si adatta perfettamente alla vista senza alcuna spaziatura laterale. Questo caso d’uso specifico è il più comune per le pagine web che utilizzano framework di layout di progettazione reattiva come Bootstrap o Foundation.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza del contenitore del visualizzatore `DIV`, il visualizzatore riempie solo quell’area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio di utilizzo è quello di incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina web, effettua le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione di HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere `FlyoutViewer.js`. `FlyoutViewer.js` si trova nei seguenti [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Dynamic Media di Adobe e viene servito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Dynamic Media di Adobe in cui sono installati i visualizzatori IS.

Un percorso relativo si presenta come segue:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Fai riferimento solo al visualizzatore principale JavaScript `include` nella pagina. Non fare riferimento a file JavaScript aggiuntivi nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente all’SDK di HTML5 `Utils.js` libreria caricata dal visualizzatore da `/s7viewers` percorso contestuale (cosiddetto SDK consolidato) `include`). Il motivo è che la posizione di `Utils.js` Per librerie di visualizzatori runtime simili, sono gestite completamente dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, è possibile inserire un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe le funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore DIV.

   Aggiungi un elemento DIV vuoto alla pagina in cui desideri che appaia il visualizzatore. L’ID dell’elemento DIV deve essere definito, perché viene successivamente passato all’API del visualizzatore.

   Il segnaposto DIV è un elemento posizionato, il che significa che il `position` La proprietà CSS è impostata su `relative` o `absolute`.

   È responsabilità della pagina web specificare il `z-index` per l’elemento DIV segnaposto. In questo modo la porzione a comparsa del visualizzatore viene visualizzata sopra gli altri elementi della pagina web.

   Di seguito è riportato un esempio di elemento DIV segnaposto definito:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore.

   Questo visualizzatore visualizza le miniature quando si lavora con set di più elementi. Nei sistemi desktop, le miniature vengono posizionate sotto la vista principale. Allo stesso tempo, il visualizzatore consente lo scambio della risorsa principale durante il runtime utilizzando `setAsset()` API. In qualità di sviluppatore, puoi controllare come il visualizzatore gestisce l’area delle miniature nell’area inferiore, quando la nuova risorsa ha un solo elemento. È possibile mantenere intatta la dimensione del visualizzatore esterno e lasciare che la vista principale aumenti la sua altezza e occupare l&#39;area delle miniature. In alternativa, è possibile mantenere statiche le dimensioni della visualizzazione principale e comprimere l’area del visualizzatore esterno, lasciando che il contenuto della pagina web si muova verso l’alto, e quindi utilizzare l’area immobiliare della pagina gratuita lasciata dalle miniature.

   Per mantenere intatti i limiti del visualizzatore esterno, definisci le dimensioni per `.s7flyoutviewer` classe CSS di primo livello in unità assolute. Le dimensioni in CSS possono essere posizionate direttamente sulla pagina HTML o in un file CSS per visualizzatori personalizzati e successivamente assegnate a un record predefinito per visualizzatori in Dynamic Media Classic oppure trasmesse in modo esplicito utilizzando il comando stile.

   Vedi [Personalizzazione del visualizzatore zoom in linea](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione delle dimensioni statiche del visualizzatore esterno in una pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puoi vedere il comportamento con un’area di visualizzazione esterna fissa nella pagina di esempio seguente. Quando si passa da un set all’altro, le dimensioni del visualizzatore esterno non cambiano:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-outer-area.html)

   Per rendere statiche le dimensioni della visualizzazione principale, definisci le dimensioni del visualizzatore in unità assolute per l&#39;interno `Container` Componente SDK che utilizza `.s7flyoutviewer .s7container` Selettore CSS. Inoltre, devi ignorare la dimensione fissa definita per il `.s7flyoutviewer` classe CSS di primo livello nel CSS del visualizzatore predefinito, impostandolo su `auto`.

   Di seguito è riportato un esempio di definizione della dimensione del visualizzatore per l’interno `Container` Componente SDK in modo che l’area di visualizzazione principale non cambi le sue dimensioni quando si cambia risorsa:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La pagina di esempio seguente mostra il comportamento del visualizzatore con una dimensione di visualizzazione principale fissa. Quando si passa da un set all’altro, la visualizzazione principale rimane statica e il contenuto della pagina web si sposta in verticale:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/inlinezoom/InlineZoom-fixed-main-view.html)

   Inoltre, il CSS del visualizzatore predefinito fornisce una dimensione fissa per l’area esterna preconfigurata.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza di `s7viewers.FlyoutViewer` , passare tutte le informazioni di configurazione al relativo costruttore e chiamare `init()` su un’istanza di visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere `containerId` campo che contiene il nome dell’ID contenitore visualizzatore e nidificato `params` Oggetto JSON con parametri di configurazione supportati dal visualizzatore. In questo caso, il `params` L&#39;oggetto deve avere almeno l&#39;URL Image Server passato come `serverUrl` proprietà; la risorsa iniziale come `asset` parametro , percorso di base per il caricamento di CSS come `contentUrl` e nome predefinito come `config` parametro . L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il `init()` metodo immediatamente prima della chiusura `BODY` o sul corpo `onload()` evento.

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata al `init()` metodo . L&#39;esempio presuppone `inlineZoomViewer` è l’istanza visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; `http://s7d1.scene7.com/is/image/` è l’URL di Image Server; e `Scene7SharedAssets/ImageSet-Views-Sample` è la risorsa:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
   "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Il codice seguente è un esempio completo di una pagina web semplice che incorpora il visualizzatore zoom in linea con dimensioni fisse:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head><body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
   "config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
   "contenturl" : "http://s7d1.scene7.com/is/content/", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Incorporazione di design reattivo con altezza illimitata {#section-056cb574713c4d07be6d07cf3c598839}

Con l’incorporazione di design reattivo, la pagina web dispone normalmente di un layout flessibile che determina le dimensioni di runtime del contenitore del visualizzatore `DIV`. Nell’esempio seguente, si supponga che la pagina web consenta il contenitore del visualizzatore `DIV` per prendere il 40% delle dimensioni della finestra del browser web, lasciando la sua altezza senza restrizioni. Il codice HTML della pagina web sarà simile al seguente:

```html {.line-numbers}
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

L’aggiunta del visualizzatore a una pagina di questo tipo è simile alla procedura per l’incorporazione a dimensione fissa. L’unica differenza è che devi sovrascrivere il ridimensionamento fisso dal CSS del visualizzatore predefinito con la dimensione impostata in unità relative.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell&#39;incorporazione della dimensione fissa con le seguenti tre eccezioni:

* aggiungi il contenitore `DIV` al &quot;titolare&quot; esistente `DIV`;
* aggiunto `imagereload` parametro con punti di interruzione espliciti;
* invece di impostare una dimensione fissa del visualizzatore utilizzando unità assolute, utilizza CSS che imposta il visualizzatore `width` e `height` al 100% come nei seguenti casi:

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La pagina degli esempi seguenti illustra gli utilizzi più reali dell’incorporazione di design reattivo a altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Posizione demo alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Incorporazione di dimensioni flessibili con larghezza e altezza definite {#section-0a329016f9414d199039776645c693de}

Se è definito un tipo di incorporamento a dimensioni flessibili con larghezza e altezza, lo stile della pagina web è diverso. Fornisce entrambe le dimensioni al `"holder"` DIV e lo centra nella finestra del browser. Inoltre, la pagina web imposta le dimensioni del `HTML` e `BODY` al 100%.

```html {.line-numbers}
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

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
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
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
"config" : "Scene7SharedAssets/Universal_HTML5_Zoom_Inline", 
"contenturl" : "http://s7d1.scene7.com/is/content/", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporazione tramite API basate su Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L’utilizzo di questo costruttore API non richiede alcun parametro e i parametri di configurazione specificati utilizzano `setContainerId()`, `setParam()`e `setAsset()` Metodi API, con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con l’API basata su setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var inlineZoomViewer = new s7viewers.FlyoutViewer(); 
inlineZoomViewer.setContainerId("s7viewer"); 
inlineZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
inlineZoomViewer.setParam("config", "Scene7SharedAssets/Universal_HTML5_Zoom_Inline"); 
inlineZoomViewer.setParam("contenturl", "http://s7d1.scene7.com/is/content/"); 
inlineZoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
inlineZoomViewer.init(); 
</script> 
</body> 
</html>
```
