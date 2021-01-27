---
description: Il visualizzatore zoom è un visualizzatore di immagini che visualizza un’immagine con zoom. Questo visualizzatore funziona con i set di immagini e la navigazione viene effettuata utilizzando i campioni. Sono disponibili strumenti di zoom, supporto per schermo intero, campioni e un pulsante di chiusura opzionale. È progettato per funzionare su computer desktop e dispositivi mobili.
keywords: responsive
seo-description: Il visualizzatore zoom è un visualizzatore di immagini che visualizza un’immagine con zoom. Questo visualizzatore funziona con i set di immagini e la navigazione viene effettuata utilizzando i campioni. Sono disponibili strumenti di zoom, supporto per schermo intero, campioni e un pulsante di chiusura opzionale. È progettato per funzionare su computer desktop e dispositivi mobili.
seo-title: Zoom
solution: Experience Manager
title: Zoom
topic: Dynamic Media
uuid: ec2a91e2-ce2c-48b1-a2b2-8671524288c7
translation-type: tm+mt
source-git-commit: dacd641302826196f4bf4c8d2dfc02d032d63487
workflow-type: tm+mt
source-wordcount: '2460'
ht-degree: 0%

---


# Zoom{#zoom}

Il visualizzatore zoom è un visualizzatore di immagini che visualizza un’immagine con zoom. Questo visualizzatore funziona con i set di immagini e la navigazione viene effettuata utilizzando i campioni. Sono disponibili strumenti di zoom, supporto per schermo intero, campioni e un pulsante di chiusura opzionale. È progettato per funzionare su computer desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Tipo di visualizzatore 502.

Vedere [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilizzo del visualizzatore zoom {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore zoom rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Potete utilizzare il visualizzatore zoom in modalità pop-up utilizzando una pagina HTML pronta per la produzione fornita con i visualizzatori IS o in modalità incorporata, dove viene integrata nella pagina Web di destinazione tramite l’API documentata.

La configurazione e l’interfaccia sono simili a quelle degli altri visualizzatori. L’associazione di interfacce viene realizzata tramite CSS personalizzato.

Consultate [Riferimento comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore zoom {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il visualizzatore zoom supporta i seguenti gesti touch, comuni ad altre applicazioni mobili. Quando il visualizzatore non è in grado di elaborare il gesto di scorrimento dell&#39;utente, inoltra l&#39;evento al browser Web per eseguire lo scorrimento nativo della pagina. Questo tipo di funzionalità consente all&#39;utente di navigare nella pagina anche se il visualizzatore occupa la maggior parte dell&#39;area dello schermo del dispositivo.

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
   <td colname="col2"> <p> Seleziona una nuova miniatura nei campioni. Nella vista principale, nasconde o rivela gli elementi dell’interfaccia utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doppio tocco </p> </td> 
   <td colname="col2"> <p> Esegue lo zoom di un livello fino al raggiungimento dell'ingrandimento massimo. Il doppio tocco successivo ripristina lo stato di visualizzazione iniziale del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pizzico </p> </td> 
   <td colname="col2"> <p>Effettua lo zoom in o zoom out. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento o scorrimento orizzontale </p> </td> 
   <td colname="col2"> <p> Consente di scorrere l’elenco dei campioni nella barra dei campioni. </p> <p> Se l'immagine è in stato di ripristino e il parametro <span class="codeph"> di frametransition </span> è impostato su slide, la risorsa viene modificata con l'animazione della diapositiva. Per altre modalità di <span class="codeph"> frametransition </span> il gesto esegue lo scorrimento nativo delle pagine. </p> <p> Se l’immagine viene ingrandita, l’immagine viene spostata in orizzontale. Se l’immagine viene spostata sul bordo della visualizzazione e un passaggio del dito viene eseguito nella stessa direzione, il gesto esegue lo scorrimento nativo della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento verticale </p> </td> 
   <td colname="col2"> <p> Se lo stato dell'immagine è reset, il gesto esegue lo scorrimento nativo delle pagine. </p> <p> Quando l'immagine viene ingrandita, essa si sposta in verticale. Se l’immagine viene spostata sul bordo della visualizzazione e un passaggio del dito viene eseguito nella stessa direzione, il gesto esegue lo scorrimento nativo della pagina. </p> <p> Se il gesto viene eseguito all’interno dell’area dei campioni, viene eseguito uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta sia l&#39;input touch che l&#39;input del mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser Web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile tramite tastiera.

Vedere [Accessibilità e navigazione da tastiera](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore zoom {#section-6bb5d3c502544ad18a58eafe12a13435}

Diverse pagine Web hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina Web fornisce un collegamento che, quando viene fatto clic su di essa, apre il visualizzatore in una finestra browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest&#39;ultimo caso, la pagina Web potrebbe avere un layout statico o utilizzare un design reattivo che viene visualizzato in modo diverso su dispositivi diversi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: incorporazione a comparsa, dimensione fissa e incorporazione reattiva del design.

**Informazioni sulla modalità a comparsa**

In modalità pop-up, il visualizzatore viene aperto in una finestra o in una scheda separata del browser Web. Richiede l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l&#39;orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando la chiamata `window.open()` JavaScript, l&#39;elemento HTML configurato correttamente `A` o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML out-of-the-box per la modalità di operazione a comparsa. La pagina HTML out-of-the-box è denominata `ZoomViewer.html` e si trova nella sottocartella `html5/` della distribuzione standard dei visualizzatori IS come segue:

`<s7viewers_root>/html5/ZoomViewer.html`

Applicate CSS personalizzato per ottenere un aspetto personalizzato per la pagina.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore nella nuova finestra:

```
 <a 
href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina Web esistente, che potrebbe già presentare contenuti per clienti non correlati al visualizzatore. In genere, il visualizzatore occupa solo una parte del patrimonio immobiliare della pagina Web.

I casi d’uso principali sono le pagine Web orientate per desktop o dispositivi tablet, nonché le pagine reattive progettate che regolano automaticamente il layout, a seconda del tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica la dimensione dopo il caricamento iniziale. Questa opzione è la scelta migliore per le pagine Web con layout statico.

La modalità di incorporazione reattiva presuppone che il ridimensionamento del visualizzatore sia necessario durante l&#39;esecuzione a causa della modifica delle dimensioni del contenitore `DIV`. L’esempio più comune è l’aggiunta di un visualizzatore a una pagina Web con layout flessibile.

In modalità di incorporazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina Web ridimensiona il contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente l’altezza in base alle proporzioni della risorsa utilizzata. Questa logica garantisce che la risorsa si adatti perfettamente alla vista senza riempimenti laterali. Questo caso di utilizzo è il più comune per le pagine Web che utilizzano framework di layout reattivi come Bootstrap, Foundation e così via.

Se la pagina Web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore riempie tale area e ha le stesse dimensioni della pagina Web. Ad esempio, incorporando il visualizzatore in una sovrapposizione modale, la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser Web.

## Incorporazione a dimensione fissa {#section-44f365e6c0dd40709467a459afa82a7f}

Per aggiungere il visualizzatore a una pagina Web, effettuate le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore DIV.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell&#39;intestazione HTML. Prima di poter utilizzare l&#39;API del visualizzatore, accertatevi di includere [!DNL ZoomViewer.js]. Il file [!DNL ZoomViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Potete utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Dynamic Media Classic  Adobe e viene distribuito dallo stesso dominio. In caso contrario, specificate un percorso completo per uno dei server Dynamic Media Classic  Adobe in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>È consigliabile fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non dovete fare riferimento ad altri file JavaScript nel codice della pagina Web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fate riferimento direttamente alla libreria HTML5 SDK `Utils.js` caricata dal visualizzatore dal percorso contestuale `/s7viewers` (il cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o librerie di visualizzatori runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore.  Adobe non conserva sul server versioni precedenti del visualizzatore secondario `includes`.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi codice JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina, si interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione di prodotto.

1. Definizione del contenitore DIV.

   Aggiungete un elemento DIV vuoto alla pagina in cui desiderate visualizzare il visualizzatore. L&#39;ID dell&#39;elemento DIV deve essere definito perché l&#39;ID viene passato successivamente all&#39;API del visualizzatore.

   Il segnaposto DIV è un elemento posizionato, il che significa che la proprietà `position` CSS è impostata su `relative` o `absolute`.

   Esempio di un elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore.

   Questo visualizzatore visualizza le miniature quando si lavora con set di più elementi, mentre sui sistemi desktop le miniature vengono posizionate sotto la visualizzazione principale. Allo stesso tempo, il visualizzatore consente di scambiare la risorsa principale in fase di esecuzione utilizzando l&#39;API `setAsset()`. In qualità di sviluppatore, potete controllare come il visualizzatore gestisce l’area delle miniature in basso quando la nuova risorsa dispone di un solo elemento. È possibile mantenere intatte le dimensioni del visualizzatore esterno e consentire alla vista principale di aumentare l’altezza e occupare l’area delle miniature. In alternativa, potete mantenere statiche le dimensioni di visualizzazione principale e comprimere l’area del visualizzatore esterno, consentendo al contenuto della pagina Web di spostarsi verso l’alto e utilizzare lo stato reale dello schermo gratuito lasciato sopra le miniature.

   Per mantenere intatti i limiti del visualizzatore esterno, definite le dimensioni della classe CSS di livello principale `.s7zoomviewer` in unità assolute. Il ridimensionamento in CSS può essere inserito direttamente nella pagina HTML o in un file CSS del visualizzatore personalizzato, che verrà successivamente assegnato a un record di predefinito per visualizzatori in Dynamic Media Classic o trasmesso esplicitamente utilizzando un comando di stile.

   Consultate [Personalizzazione del visualizzatore zoom](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) per ulteriori informazioni sullo stile del visualizzatore con i CSS.

   Di seguito è riportato un esempio di definizione di una dimensione statica per visualizzatore esterno nella pagina HTML:

   ```
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Potete vedere il comportamento con un visualizzatore esterno fisso nell&#39;esempio seguente. Tenete presente che quando passate da un set all’altro, le dimensioni del visualizzatore esterno non cambiano:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-outer-area.html)

   Per rendere statiche le dimensioni di visualizzazione principali, definite le dimensioni del visualizzatore in unità assolute per il componente SDK interno `Container` utilizzando il selettore `.s7zoomviewer` `.s7container` CSS oppure utilizzando il modificatore `stagesize`.

   Di seguito è riportato un esempio di definizione delle dimensioni del visualizzatore per il componente SDK interno `Container` in modo che l&#39;area di visualizzazione principale non cambi le dimensioni quando si passa da una risorsa all&#39;altra:

   ```
   #s7viewer.s7zoomviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La seguente pagina demo mostra il comportamento del visualizzatore con una dimensione di visualizzazione principale fissa. Notate che quando passate da un set all’altro, la vista principale rimane statica e il contenuto della pagina Web si sposta in verticale.

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/ZoomViewer-fixed-main-view.html)

   Potete impostare il modificatore `stagesize` nel record del predefinito per visualizzatori in Dynamic Media Classic, oppure trasmetterlo esplicitamente con il codice di inizializzazione del visualizzatore con la raccolta `params` o come chiamata API come descritto nella sezione Riferimento comandi di questa Guida, come segue:

   ```
    zoomViewer.setParam("stagesize", 
   "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi descritti qui sopra, potete creare un&#39;istanza della classe `s7viewers.ZoomViewer`, trasmettere tutte le informazioni di configurazione al relativo costruttore e chiamare il metodo `init()` su un&#39;istanza di visualizzatore.

   Le informazioni di configurazione vengono trasmesse al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere un campo `containerId` contenente il nome dell&#39;ID contenitore del visualizzatore e un oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore. In questo caso, l&#39;oggetto `params` deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. L&#39;API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore del visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser ritardano la creazione del DOM fino alla fine della pagina Web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()`.

   Allo stesso tempo, l&#39;elemento contenitore non deve necessariamente far parte del layout della pagina Web. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del metodo `init()`. Questo esempio presuppone che `zoomViewer` sia l’istanza del visualizzatore, che `s7viewer` sia il nome del segnaposto DIV, che `http://s7d1.scene7.com/is/image/` sia l’URL del server immagini e che `Scene7SharedAssets/ImageSet-Views-Sample` sia la risorsa.

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

   Il codice seguente è un esempio completo di una pagina Web banale che incorpora il visualizzatore video con una dimensione fissa:

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

## Incorporazione responsive con altezza illimitata {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

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

L’aggiunta del visualizzatore a tale pagina è simile alla procedura per l’incorporamento a dimensione fissa. L’unica differenza è che non è necessario definire in modo esplicito le dimensioni del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi indicati sopra sono uguali a quelli con l&#39;incorporamento a dimensione fissa. Aggiungete il DIV contenitore al DIV `"holder"` esistente. Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

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

La pagina degli esempi seguente illustra gli usi più reali dell’incorporamento reattivo di design con altezza illimitata:

[Live Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Incorporamento di dimensioni flessibili con larghezza e altezza definite {#section-3674e6c032594441a6576b7fb1de6e64}

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

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L&#39;utilizzo di questo costruttore di API non accetta parametri e i parametri di configurazione vengono specificati utilizzando i metodi `setContainerId()`, `setParam()` e `setAsset()` API con chiamate JavaScript separate.

L&#39;esempio seguente illustra l&#39;utilizzo dell&#39;incorporamento a dimensione fissa con l&#39;API basata su setter:

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

