---
description: Basic Zoom Viewer è un visualizzatore di immagini che visualizza una singola immagine con zoom. È dotato di strumenti di zoom, supporto a schermo intero e un pulsante di chiusura opzionale. Questo visualizzatore è il più leggero. È progettato per funzionare su computer desktop e dispositivi mobili.
keywords: responsive
seo-description: Basic Zoom Viewer è un visualizzatore di immagini che visualizza una singola immagine con zoom. È dotato di strumenti di zoom, supporto a schermo intero e un pulsante di chiusura opzionale. Questo visualizzatore è il più leggero. È progettato per funzionare su computer desktop e dispositivi mobili.
seo-title: Zoom di base
solution: Experience Manager
title: Zoom di base
topic: Dynamic media
uuid: 5466d647-af70-4503-9898-bb712ba6a007
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Zoom di base{#basic-zoom}

Basic Zoom Viewer è un visualizzatore di immagini che visualizza una singola immagine con zoom. È dotato di strumenti di zoom, supporto a schermo intero e un pulsante di chiusura opzionale. Questo visualizzatore è il più leggero. È progettato per funzionare su computer desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User Generated Content) non sono supportate da questo visualizzatore.

Tipo di visualizzatore 501.

Consultate Requisiti di [sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B](https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B)

## Utilizzo del visualizzatore zoom di base {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore zoom di base rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) che gli utenti scaricano in fase di esecuzione.

Potete utilizzare il visualizzatore zoom di base in modalità pop-up utilizzando una pagina HTML pronta per la produzione fornita con i visualizzatori IS o in modalità incorporata, in cui è integrata nella pagina Web di destinazione tramite l’API documentata.

La configurazione e l’interfaccia sono simili a quelle degli altri visualizzatori. L’associazione di interfacce viene realizzata tramite CSS personalizzato.

Consultate Riferimento [comando comune a tutti i visualizzatori - Attributi](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) di configurazione e Riferimento [comando comuni a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore zoom di base {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il visualizzatore zoom di base supporta i seguenti gesti touch, comuni ad altre applicazioni mobili.

Quando il visualizzatore non è in grado di elaborare il gesto di scorrimento di un utente, inoltra l&#39;evento al browser Web per eseguire uno scorrimento nativo della pagina. Questo tipo di funzionalità consente all&#39;utente di navigare nella pagina anche se il visualizzatore occupa la maggior parte dell&#39;area dello schermo del dispositivo.

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
   <td colname="col2"> <p>Nasconde o rivela gli elementi dell’interfaccia utente. </p> </td> 
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
   <td colname="col1"> <p>Scorrimento </p> </td> 
   <td colname="col2"> <p> Se lo stato dell'immagine è reset, il gesto esegue uno scorrimento nativo della pagina. </p> <p> Quando l'immagine viene ingrandita, essa sposta l'immagine. Se l’immagine viene spostata sul bordo della visualizzazione e viene eseguito un passaggio del dito in quella direzione, il gesto esegue uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta inoltre l&#39;input touch e l&#39;input del mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser Web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile tramite tastiera.

Consultate Accesso [e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)da tastiera.

## Incorporazione del visualizzatore zoom di base {#section-6bb5d3c502544ad18a58eafe12a13435}

Diverse pagine Web hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina Web fornisce un collegamento che, quando viene fatto clic su di essa, apre il visualizzatore in una finestra browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest&#39;ultimo caso, la pagina Web potrebbe avere un layout di pagina statico oppure utilizzare un design reattivo che viene visualizzato in modo diverso su dispositivi diversi o per diverse dimensioni di finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: incorporazione a comparsa, dimensione fissa e incorporazione reattiva del design.

**Informazioni sulla modalità a comparsa**

In modalità pop-up, il visualizzatore viene aperto in una finestra o in una scheda separata del browser Web. Richiede l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l&#39;orientamento del dispositivo venga modificato.

La modalità a comparsa è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando la chiamata `window.open()` JavaScript, l’elemento `A` HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML out-of-the-box per la modalità operativa a comparsa. In questo caso, viene chiamato [!DNL BasicZoomViewer.html] e si trova nella [!DNL html5/] sottocartella della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/BasicZoomViewer.html]

Potete ottenere la personalizzazione visiva applicando CSS personalizzato.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina Web esistente, che potrebbe già presentare contenuti per clienti non correlati al visualizzatore. In genere, il visualizzatore occupa solo una parte del patrimonio immobiliare di una pagina Web.

I casi d’uso principali sono le pagine Web orientate per desktop o dispositivi tablet, nonché le pagine reattive progettate che adattano automaticamente il layout in base al tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica la dimensione dopo il caricamento iniziale. Questa è la scelta migliore per le pagine Web con layout statico.

L&#39;incorporazione di una progettazione reattiva presuppone che il visualizzatore debba ridimensionare in fase di esecuzione in seguito alla modifica delle dimensioni del suo contenitore `DIV`. L’esempio più comune è l’aggiunta di un visualizzatore a una pagina Web con layout di pagina flessibile.

In modalità di incorporazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina Web ridimensiona il proprio contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`e ne lascia invariata l’altezza, il visualizzatore sceglie automaticamente l’altezza in base alle proporzioni della risorsa utilizzata. Questa funzione assicura che la risorsa si adatti perfettamente alla vista senza riempimenti laterali. Questo caso di utilizzo è il più comune per le pagine Web che utilizzano framework di layout reattivi per la progettazione Web come Bootstrap, Foundation e così via.

In caso contrario, se la pagina Web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore compila solo tale area e ha le stesse dimensioni del layout della pagina Web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser Web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuate le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore DIV.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell&#39;intestazione HTML. Prima di poter utilizzare l&#39;API del visualizzatore, accertatevi di includerla [!DNL BasicZoomViewer.js]. Il [!DNL BasicZoomViewer.js] file si trova nella [!DNL html5/js/] sottocartella della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/js/BasicZoomViewer.js]

Potete usare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene distribuito dallo stesso dominio. In caso contrario, specificate un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/BasicZoomViewer.js"></script>
```

>[!NOTE]
>
>È consigliabile fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non dovete fare riferimento ad altri file JavaScript nel codice della pagina Web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fate riferimento direttamente alla libreria SDK HTML5 caricata dal `Utils.js` visualizzatore dal percorso `/s7viewers` contestuale (il cosiddetto SDK consolidato `include`). Il motivo è che la posizione delle librerie di visualizzatori runtime `Utils.js` o simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva `includes` sul server le versioni precedenti del visualizzatore secondario.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi codice JavaScript secondario utilizzato `include` dal visualizzatore sulla pagina si interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione di prodotto.

1. Definizione del contenitore DIV.

   Aggiungete un elemento DIV vuoto alla pagina in cui desiderate visualizzare il visualizzatore. L&#39;ID dell&#39;elemento DIV deve essere definito perché l&#39;ID viene passato successivamente all&#39;API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il segnaposto DIV è un elemento posizionato, il che significa che la proprietà `position` CSS è impostata su `relative` o `absolute`.

   Esempio di un elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   Potete impostare le dimensioni statiche per il visualizzatore dichiarandolo per la classe CSS di livello `.s7basiczoomviewer` principale in unità assolute oppure utilizzando il `stagesize` modificatore.

   Potete inserire le dimensioni in CSS direttamente nella pagina HTML, oppure in un file CSS del visualizzatore personalizzato, che verrà successivamente assegnato a un record di predefinito per visualizzatori in SPS, oppure trasmesso esplicitamente utilizzando un comando di stile.

   Consultate [Personalizzazione del visualizzatore](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) zoom di base per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione di una dimensione visualizzatore statica in una pagina HTML:

   ```
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Potete impostare il `stagesize` modificatore nel record del predefinito per visualizzatori in SPS, oppure passarlo esplicitamente con il codice di inizializzazione del visualizzatore con `params` la raccolta, oppure come chiamata API come descritto nella sezione Riferimento comando, come segue:

   ```
   basicZoomViewer.setParam("stagesize", "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi descritti qui sopra, potete creare un&#39;istanza della `s7viewers.BasicZoomViewer` classe, trasmettere tutte le informazioni di configurazione al relativo costruttore e chiamare `init()` il metodo su un&#39;istanza di visualizzatore. Le informazioni di configurazione vengono trasmesse al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere un campo containerId che contiene il nome del visualizzatore `container ID` `params` e un oggetto JSON nidificato con i parametri di configurazione supportati dal visualizzatore. In questo caso, l’ `params` oggetto deve avere almeno l’URL Image Server passato come `serverUrl` proprietà e la risorsa iniziale come `asset` parametro. L&#39;API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore del visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser ritardano la creazione del DOM fino alla fine della pagina Web. Per garantire la massima compatibilità, chiamate il `init()` metodo immediatamente prima del `BODY` tag di chiusura o dell’ `onload()` evento body.

   Allo stesso tempo, l&#39;elemento contenitore non deve necessariamente far parte del layout della pagina Web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` lo stile assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del `init()` metodo. L’esempio presuppone che `basicZoomViewer` sia l’istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; è `http://s7d1.scene7.com/is/image/` l’URL del server immagini ed `Scene7SharedAssets/Backpack_B` è la risorsa:

   ```
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Backpack_B", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Il codice seguente è un esempio completo di una pagina Web semplice che incorpora il visualizzatore zoom di base con una dimensione fissa:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
    "containerId":"s7viewer", 
    "params":{ 
     "asset":"Scene7SharedAssets/Backpack_B", 
     "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporazione responsive con altezza illimitata**

Con l’incorporazione reattiva della progettazione, la pagina Web dispone in genere di un layout flessibile che specifica le dimensioni runtime del contenitore del visualizzatore `DIV`. Ad esempio, si supponga che la pagina Web consenta al contenitore del visualizzatore `DIV` di occupare il 40% delle dimensioni della finestra del browser Web, lasciando invariata l’altezza. Il codice HTML della pagina Web sarà simile al seguente:

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

Tutti i passaggi indicati sopra sono uguali a quelli con l&#39;incorporamento a dimensione fissa. Aggiungere il contenitore DIV al `"holder"` DIV esistente. Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La pagina degli esempi seguente illustra gli usi più reali dell’incorporamento reattivo di design con altezza illimitata:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**Dimensioni flessibili Incorporamento con larghezza e altezza definite**

In caso di incorporamento di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina Web è diverso. Fornisce entrambe le dimensioni al `"holder"` DIV e lo centrerà nella finestra del browser. Inoltre, la pagina Web imposta la dimensione dell’elemento `HTML` e `BODY` dell’elemento su 100%.

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

Gli altri passaggi di incorporamento sono identici ai passaggi utilizzati per l&#39;incorporamento reattivo con altezza illimitata. L’esempio risultante è il seguente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
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
var basicZoomViewer = new s7viewers.BasicZoomViewer({ 
 "containerId":"s7viewer", 
 "params":{ 
  "asset":"Scene7SharedAssets/Backpack_B", 
  "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporazione tramite l&#39;API basata su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L&#39;utilizzo di questo costruttore di API non accetta parametri e i parametri di configurazione vengono specificati utilizzando `setContainerId()`, `setParam()`e metodi `setAsset()` API con chiamate JavaScript separate.

L&#39;esempio seguente illustra l&#39;utilizzo dell&#39;incorporamento a dimensione fissa con l&#39;API basata su setter:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/BasicZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7basiczoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var basicZoomViewer = new s7viewers.BasicZoomViewer(); 
basicZoomViewer.setContainerId("s7viewer"); 
basicZoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
basicZoomViewer.setAsset("Scene7SharedAssets/Backpack_B"); 
basicZoomViewer.init(); 
</script> 
</body> 
</html>
```

