---
description: Il visualizzatore zoom in linea è un visualizzatore di immagini. Viene visualizzata un’immagine statica con la versione ingrandita mostrata sopra l’immagine statica quando un utente passa il mouse o tocca la vista principale. Questo visualizzatore funziona con i set di immagini e la navigazione viene effettuata utilizzando i campioni. È progettato per funzionare su computer desktop e dispositivi mobili.
keywords: responsive
seo-description: Il visualizzatore zoom in linea è un visualizzatore di immagini. Viene visualizzata un’immagine statica con la versione ingrandita mostrata sopra l’immagine statica quando un utente passa il mouse o tocca la vista principale. Questo visualizzatore funziona con i set di immagini e la navigazione viene effettuata utilizzando i campioni. È progettato per funzionare su computer desktop e dispositivi mobili.
seo-title: Zoom in linea
solution: Experience Manager
title: Zoom in linea
topic: Dynamic media
uuid: 2287aef0-79ba-4d63-911a-969fa1c63385
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2457'
ht-degree: 0%

---


# Zoom in linea{#inline-zoom}

Il visualizzatore zoom in linea è un visualizzatore di immagini. Viene visualizzata un’immagine statica con la versione ingrandita mostrata sopra l’immagine statica quando un utente passa il mouse o tocca la vista principale. Questo visualizzatore funziona con i set di immagini e la navigazione viene effettuata utilizzando i campioni. È progettato per funzionare su computer desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Il tipo di visualizzatore è 504.

Vedere [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400](http://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&amp;config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline&amp;stagesize=500,400)

## Utilizzo del visualizzatore zoom in linea {#section-f21ac23d3f6449ad9765588d69584772}

Il visualizzatore zoom in linea rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Il visualizzatore zoom in linea può essere utilizzato sia in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con i visualizzatori Image Server, sia in modalità incorporata, in cui è integrato in una pagina Web di destinazione mediante l’API documentata.

La configurazione e l’interfaccia sono simili a quelle degli altri visualizzatori. Potete utilizzare un CSS personalizzato per applicare l&#39;interfaccia.

Consultate [Riferimento comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore zoom in linea {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore zoom in linea supporta i gesti touch singola e multi-touch comuni in altre applicazioni mobili.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tocco singolo </p> </td> 
   <td colname="col2"> <p> Attiva la visualizzazione a comparsa o modifica il livello di zoom principale e secondario nei campioni, seleziona la nuova miniatura. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento o scorrimento orizzontale </p> </td> 
   <td colname="col2"> <p> Consente di scorrere l’elenco dei campioni nella barra dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento verticale </p> </td> 
   <td colname="col2"> <p>Se il gesto viene eseguito all’interno dell’area dei campioni, viene eseguito uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta inoltre l&#39;input touch e l&#39;input del mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser Web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile tramite tastiera.

Vedere [Accessibilità e navigazione da tastiera](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore zoom in linea {#section-6bb5d3c502544ad18a58eafe12a13435}

Diverse pagine Web hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina Web fornisce un collegamento selezionabile che apre il visualizzatore in una finestra browser separata. In altri casi, potrebbe essere necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest&#39;ultimo caso, la pagina Web potrebbe avere un layout di pagina statico, oppure utilizzare un design reattivo che viene visualizzato in modo diverso su dispositivi diversi, o per dimensioni diverse della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: incorporazione a comparsa, dimensione fissa e incorporazione reattiva.

**Pop-up**

Nella modalità a comparsa, il visualizzatore viene aperto in una finestra o in una scheda separata del browser Web. Richiede l&#39;intera area della finestra del browser e si regola quando la finestra del browser viene ridimensionata o viene modificato l&#39;orientamento del dispositivo.

Questa modalità è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando la chiamata `window.open()` JavaScript, l&#39;elemento HTML configurato correttamente `A` o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare la pagina HTML out-of-the-box per la modalità a comparsa denominata `FlyoutViewer.html`. Si trova nella sottocartella [!DNL html5/] della distribuzione standard di Image Serving Viewers:

`<s7viewers_root>/html5/FlyoutViewer.html`

È inoltre necessario che il componente FlyoutZoomView sia configurato per funzionare in modalità zoom in linea. Si consiglia di utilizzare il predefinito `Scene7SharedAssets/Universal_HTML5_Zoom_Inline` predefinito per visualizzatori zoom in linea o un predefinito personalizzato da esso derivato. La personalizzazione visiva può essere ottenuta applicando CSS personalizzato.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
 <a href="http://s7d1.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample&config=Scene7SharedAssets/Universal_HTML5_Zoom_Inline"target="_blank">Open popup viewer</a>
```

**Incorporazione a dimensione fissa e incorporazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina Web esistente, che potrebbe già presentare contenuti per clienti non correlati al visualizzatore. In genere, il visualizzatore occupa solo una parte dello stato reale della pagina Web.

I casi d’uso principali sono le pagine Web orientate per computer desktop o dispositivi tablet e le pagine Web reattive che adattano automaticamente il layout in base al tipo di dispositivo.

La modalità di incorporazione a dimensione fissa viene utilizzata quando il visualizzatore non ne modifica la dimensione dopo il caricamento iniziale. Questa opzione è ideale per le pagine Web con layout di pagina statico.

La modalità di incorporazione reattiva presuppone che il visualizzatore debba ridimensionare durante il runtime in seguito alla modifica delle dimensioni del contenitore `DIV`. L’esempio più comune è l’aggiunta di un visualizzatore a una pagina Web con layout di pagina flessibile.

Quando utilizzate la modalità di incorporamento reattiva del design con il visualizzatore zoom in linea, accertatevi di specificare punti di interruzione espliciti per l&#39;immagine della vista principale utilizzando il parametro `imagereload`. Idealmente, potete far corrispondere i punti di interruzione con i punti di interruzione della larghezza del visualizzatore come indicato dalla pagina Web CSS.

In modalità di incorporazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui una pagina Web ridimensiona il proprio contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente l’altezza in base alle proporzioni della risorsa utilizzata. Ciò significa che la risorsa si adatta perfettamente alla vista senza riempimenti laterali. Questo caso di utilizzo è il più comune per le pagine Web che utilizzano framework di layout reattivi come Bootstrap, Foundation e così via.

In caso contrario, se la pagina Web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore compila solo tale area e segue le dimensioni fornite dal layout della pagina Web. Un buon esempio di utilizzo consiste nell’incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser Web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuate le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell&#39;intestazione HTML. Prima di poter utilizzare l&#39;API del visualizzatore, accertatevi di includere `FlyoutViewer.js`. `FlyoutViewer.js` si trova nella seguente  [!DNL html5/js/] sottocartella della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Potete utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Scene7  e viene distribuito dallo stesso dominio. In caso contrario, specificate un percorso completo per uno  server Adobe Scene7 in cui sono installati i visualizzatori IS.

Un percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>È consigliabile fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non dovete fare riferimento ad altri file JavaScript nel codice della pagina Web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fate riferimento direttamente alla libreria HTML5 SDK `Utils.js` caricata dal visualizzatore dal percorso contestuale `/s7viewers` (il cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o librerie di visualizzatori runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore.  Adobe non conserva sul server versioni precedenti del visualizzatore secondario `includes`.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi codice JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina, si interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione di prodotto.

1. Definizione del contenitore DIV.

   Aggiungete un elemento DIV vuoto alla pagina in cui desiderate visualizzare il visualizzatore. L&#39;ID dell&#39;elemento DIV deve essere definito perché in seguito l&#39;ID viene passato all&#39;API del visualizzatore.

   Il segnaposto DIV è un elemento posizionato, il che significa che la proprietà `position` CSS è impostata su `relative` o `absolute`.

   È responsabilità della pagina Web specificare l&#39;elemento DIV segnaposto corretto `z-index`. In questo modo la porzione a comparsa del visualizzatore viene visualizzata sopra agli altri elementi della pagina Web.

   Esempio di un elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore.

   Questo visualizzatore visualizza le miniature quando si utilizzano i set di più elementi. Sui sistemi desktop, le miniature vengono posizionate sotto la vista principale. Allo stesso tempo, il visualizzatore consente di scambiare la risorsa principale durante l&#39;esecuzione utilizzando l&#39;API `setAsset()`. In qualità di sviluppatore, potete controllare in che modo il visualizzatore gestisce l’area delle miniature nell’area inferiore quando la nuova risorsa dispone di un solo elemento. È possibile mantenere intatte le dimensioni del visualizzatore esterno e lasciare che la vista principale ne aumenti l’altezza e occupi l’area delle miniature. In alternativa, potete mantenere statiche le dimensioni di visualizzazione principale e comprimere l’area del visualizzatore esterno, consentendo al contenuto della pagina Web di spostarsi verso l’alto, quindi utilizzare l’area reale della pagina gratuita a sinistra dalle miniature.

   Per mantenere intatti i limiti del visualizzatore esterno, definite le dimensioni della classe CSS di livello principale `.s7flyoutviewer` in unità assolute. Il ridimensionamento in CSS può essere inserito direttamente nella pagina HTML o in un file CSS del visualizzatore personalizzato, che verrà successivamente assegnato a un record di predefinito per visualizzatori in Scene7 Publishing System, oppure trasmesso in modo esplicito tramite il comando stile.

   Consultate [Personalizzazione del visualizzatore zoom in linea](../../c-html5-s7-aem-asset-viewers/c-html5-inlinezoom-viewer-about/c-html5-inlinezoom-viewer-customizingviewer/c-html5-inlinezoom-viewer-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) per ulteriori informazioni sullo stile del visualizzatore con i CSS.

   Di seguito è riportato un esempio di definizione delle dimensioni statiche del visualizzatore esterno in una pagina HTML:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Potete visualizzare il comportamento con un’area fissa del visualizzatore esterno sulla pagina di esempio seguente. Tenete presente che quando passate da un set all’altro, le dimensioni del visualizzatore esterno non cambiano:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-outer-area.html)

   Per rendere statiche le dimensioni di visualizzazione principali, definite le dimensioni del visualizzatore in unità assolute per il componente SDK interno `Container` utilizzando il selettore CSS `.s7flyoutviewer .s7container`. Inoltre, è necessario ignorare le dimensioni fisse definite per la classe CSS di livello principale `.s7flyoutviewer` nel CSS del visualizzatore predefinito, impostando tale valore su `auto`.

   Di seguito è riportato un esempio di definizione delle dimensioni del visualizzatore per il componente SDK interno `Container` in modo che l&#39;area di visualizzazione principale non cambi le dimensioni quando si passa da una risorsa all&#39;altra:

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La pagina di esempio seguente mostra il comportamento del visualizzatore con una dimensione di visualizzazione principale fissa. Quando passate da un set all’altro, la vista principale rimane statica e il contenuto della pagina Web si sposta in verticale:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/InlineZoom-fixed-main-view.html)

   Inoltre, il CSS predefinito per visualizzatori offre una dimensione fissa per l&#39;area esterna out-of-the-box.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi descritti qui sopra, potete creare un&#39;istanza della classe `s7viewers.FlyoutViewer`, trasmettere tutte le informazioni di configurazione al relativo costruttore e chiamare il metodo `init()` su un&#39;istanza di visualizzatore. Le informazioni di configurazione vengono trasmesse al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere il campo `containerId` che contiene il nome dell&#39;ID contenitore del visualizzatore e l&#39;oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore. In questo caso, l&#39;oggetto `params` deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl`, la risorsa iniziale come parametro `asset`, il percorso di base per il caricamento di CSS come parametro `contentUrl` e il nome predefinito come parametro `config`. L&#39;API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore del visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser ritardano la creazione del DOM fino alla fine della pagina Web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()`.

   Allo stesso tempo, l&#39;elemento contenitore non deve necessariamente far parte del layout della pagina Web. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del metodo `init()`. L&#39;esempio presuppone che `inlineZoomViewer` sia l&#39;istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; `http://s7d1.scene7.com/is/image/` è l&#39;URL del server immagini; e `Scene7SharedAssets/ImageSet-Views-Sample` è la risorsa:

   ```
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

   Il codice seguente è un esempio completo di una pagina Web banale che incorpora il visualizzatore zoom in linea con una dimensione fissa:

   ```
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

## Incorporazione responsive con altezza illimitata {#section-056cb574713c4d07be6d07cf3c598839}

Con l&#39;incorporazione reattiva della progettazione, la pagina Web dispone in genere di un layout flessibile che specifica le dimensioni runtime del contenitore del visualizzatore `DIV`. Nell&#39;esempio seguente, si supponga che la pagina Web consenta al contenitore del visualizzatore `DIV` di assumere il 40% delle dimensioni della finestra del browser Web, lasciando invariata l&#39;altezza. Il codice HTML della pagina Web sarà simile al seguente:

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

L’aggiunta del visualizzatore a tale pagina è simile alla procedura per l’incorporamento a dimensione fissa. L’unica differenza è che dovete ignorare il ridimensionamento fisso dal CSS del visualizzatore predefinito con la dimensione impostata in unità relative.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi indicati sopra sono identici a quelli con l&#39;incorporazione a dimensione fissa con le tre eccezioni seguenti:

* aggiungere il contenitore `DIV` al &quot;supporto&quot; `DIV` esistente;
* è stato aggiunto il parametro `imagereload` con punti di interruzione espliciti;
* invece di impostare una dimensione fissa per il visualizzatore utilizzando unità assolute, utilizzate i CSS che impostano il visualizzatore `width` e `height` su 100%, come segue:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

```
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

La pagina degli esempi seguente illustra gli usi più reali dell’incorporamento reattivo di design con altezza illimitata:

[Live Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Incorporazione di dimensioni flessibili con larghezza e altezza definita {#section-0a329016f9414d199039776645c693de}

In caso di incorporamento di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina Web è diverso. Fornisce entrambe le dimensioni al DIV `"holder"` e lo centra nella finestra del browser. Inoltre, la pagina Web imposta la dimensione dell&#39;elemento `HTML` e `BODY` su 100%.

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

Gli altri passaggi di incorporamento sono identici ai passaggi utilizzati per incorporare design reattivi con altezza illimitata. L’esempio risultante è il seguente:

```
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

## Incorporazione tramite l&#39;API basata su Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L&#39;utilizzo di questo costruttore API non accetta parametri e i parametri di configurazione vengono specificati utilizzando i metodi API `setContainerId()`, `setParam()` e `setAsset()`, con chiamate JavaScript separate.

L&#39;esempio seguente illustra l&#39;utilizzo dell&#39;incorporamento a dimensione fissa con l&#39;API basata su setter:

```
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

