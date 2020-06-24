---
description: Il visualizzatore per set 360 gradi è un visualizzatore di immagini che offre una visualizzazione a 360 gradi dell’immagine o, se necessario, una visualizzazione multidimensionale. Sono disponibili strumenti di zoom e rotazione, supporto per schermo intero e un pulsante di chiusura opzionale. È progettato per funzionare su computer desktop e dispositivi mobili.
keywords: responsive
seo-description: Il visualizzatore per set 360 gradi è un visualizzatore di immagini che offre una visualizzazione a 360 gradi dell’immagine o, se necessario, una visualizzazione multidimensionale. Sono disponibili strumenti di zoom e rotazione, supporto per schermo intero e un pulsante di chiusura opzionale. È progettato per funzionare su computer desktop e dispositivi mobili.
seo-title: Spin
solution: Experience Manager
title: Spin
topic: Dynamic media
uuid: 5d5cdf83-cfe8-48cd-af74-b270f7400b14
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2166'
ht-degree: 0%

---


# Spin{#spin}

Il visualizzatore per set 360 gradi è un visualizzatore di immagini che offre una visualizzazione a 360 gradi dell’immagine o, se necessario, una visualizzazione multidimensionale. Sono disponibili strumenti di zoom e rotazione, supporto per schermo intero e un pulsante di chiusura opzionale. È progettato per funzionare su computer desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Tipo di visualizzatore 503.

Consultate Requisiti di [sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## Utilizzo del visualizzatore 360 gradi {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore 360 gradi rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Il visualizzatore 360 gradi può essere utilizzato sia in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con i visualizzatori IS, sia in modalità incorporata, dove viene integrato nella pagina Web di destinazione tramite l’API documentata.

La configurazione e l’interfaccia sono simili a quelle degli altri visualizzatori. È possibile ottenere tutte le interfacce tramite CSS personalizzato.

Consultate Riferimento [comando comune a tutti i visualizzatori - Attributi](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) di configurazione e Riferimento [comando comuni a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore 360 gradi {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il visualizzatore 360 gradi supporta i seguenti gesti touch, comuni ad altre applicazioni mobili. Quando il visualizzatore non è in grado di elaborare il gesto di scorrimento di un utente, inoltra l&#39;evento al browser Web per eseguire uno scorrimento nativo della pagina. Questo consente all&#39;utente di navigare nella pagina anche se il visualizzatore occupa la maggior parte dell&#39;area dello schermo del dispositivo.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Doppio tocco </p> </td> 
   <td colname="col2"> <p> Esegue lo zoom di un livello fino al raggiungimento dell'ingrandimento massimo. Il doppio tocco successivo ripristina lo stato di visualizzazione iniziale del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pizzico </p> </td> 
   <td colname="col2"> <p>Effettua lo zoom in o zoom out sull’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento o scorrimento orizzontale </p> </td> 
   <td colname="col2"> <p> Se l’immagine è in stato di reimpostazione, viene ruotata nel set in orizzontale. </p> <p> Se l’immagine viene ingrandita, l’immagine viene spostata in orizzontale. Se l’immagine viene spostata sul bordo della visualizzazione e lo scorrimento continua in quella direzione, il gesto esegue uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento o scorrimento verticale </p> </td> 
   <td colname="col2"> <p> Se l’immagine è in stato di ripristino, cambia l’angolo di visualizzazione verticale nel caso in cui venga utilizzato un set 360 gradi multidimensionale. In un set 360 gradi monodimensionale, o quando un set 360 gradi multidimensionale si trova sull’ultimo o sul primo asse, in modo che lo scorrimento verticale non comporti una modifica dell’angolo di visualizzazione verticale, il gesto esegue uno scorrimento nativo della pagina. </p> <p> Se l'immagine viene ingrandita, l'immagine viene spostata in verticale. Se l’immagine viene spostata sul bordo della visualizzazione e lo scorrimento continua in quella direzione, il gesto esegue uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il visualizzatore supporta inoltre l&#39;input touch e l&#39;input del mouse su dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser Web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile tramite tastiera.

Consultate Accesso [e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)da tastiera.

## Incorporazione del visualizzatore per set 360 gradi {#section-6bb5d3c502544ad18a58eafe12a13435}

Diverse pagine Web hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina Web fornisce un collegamento che, quando viene fatto clic su di essa, apre il visualizzatore in una finestra browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest&#39;ultimo caso, la pagina Web potrebbe avere un layout di pagina statico oppure utilizzare un design reattivo che viene visualizzato in modo diverso su dispositivi diversi o per diverse dimensioni di finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: incorporazione a comparsa, dimensione fissa e incorporazione reattiva del design.

**Informazioni sulla modalità a comparsa**

In modalità pop-up, il visualizzatore viene aperto in una finestra o in una scheda separata del browser Web. Richiede l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato, o se viene modificato l&#39;orientamento di un dispositivo mobile.

La modalità a comparsa è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando la chiamata `window.open()` JavaScript, l’elemento `A` HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML out-of-the-box per la modalità operativa a comparsa. In questo caso, viene chiamato [!DNL SpinViewer.html] e si trova nella [!DNL html5/] sottocartella della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/SpinViewer.html]

Potete ottenere la personalizzazione visiva applicando CSS personalizzato.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
<a 
href="http://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina Web esistente, che potrebbe già presentare contenuti per clienti non correlati al visualizzatore. In genere, il visualizzatore occupa solo una parte del patrimonio immobiliare di una pagina Web.

I casi d’uso principali sono le pagine Web orientate per computer desktop o dispositivi tablet e le pagine di progettazione reattiva che adattano automaticamente il layout in base al tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica la dimensione dopo il caricamento iniziale. Questa è la scelta migliore per le pagine Web con layout statico.

L&#39;incorporazione di una progettazione reattiva presuppone che il visualizzatore debba ridimensionare in fase di esecuzione in seguito alla modifica delle dimensioni del suo contenitore `DIV`. L’esempio più comune è l’aggiunta di un visualizzatore a una pagina Web con layout di pagina flessibile.

In modalità di incorporazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina Web ridimensiona il proprio contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`e ne lascia invariata l’altezza, il visualizzatore sceglie automaticamente l’altezza in base alle proporzioni della risorsa utilizzata. Questa funzione assicura che la risorsa si adatti perfettamente alla vista senza riempimenti laterali. Questo caso di utilizzo è il più comune per le pagine Web che utilizzano framework di layout reattivi come Bootstrap, Foundation e così via.

In caso contrario, se la pagina Web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore compila solo tale area e ha le stesse dimensioni del layout della pagina Web. Un buon esempio potrebbe consistere nell’incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser Web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore 360 gradi a una pagina Web, effettuate le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell&#39;intestazione HTML. Prima di poter utilizzare l&#39;API del visualizzatore, accertatevi di includerla `SpinViewer.js`. `SpinViewer.js` si trova nella [!DNL html5/js/] sottocartella della distribuzione standard dei visualizzatori IS:

   `<s7viewers_root>/html5/js/SpinViewer.js`

   Potete usare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Scene7 e distribuito dallo stesso dominio. In caso contrario, specificate un percorso completo per uno dei server Adobe Scene7 in cui sono installati i visualizzatori IS.

   Il percorso relativo si presenta come segue:

   ```
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >È consigliabile fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non dovete fare riferimento ad altri file JavaScript nel codice della pagina Web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fate riferimento direttamente alla libreria SDK HTML5 caricata dal `Utils.js` visualizzatore dal percorso `/s7viewers` contestuale (il cosiddetto SDK consolidato `include`). Il motivo è che la posizione delle librerie di visualizzatori runtime `Utils.js` o simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva `includes` sul server le versioni precedenti del visualizzatore secondario.
   >
   >
   >Di conseguenza, inserendo un riferimento diretto a qualsiasi codice JavaScript secondario utilizzato `include` dal visualizzatore sulla pagina si interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione di prodotto.

1. Definizione del contenitore DIV.

   Aggiungete un elemento DIV vuoto alla pagina in cui desiderate visualizzare il visualizzatore. L&#39;ID dell&#39;elemento DIV deve essere definito perché l&#39;ID viene passato successivamente all&#39;API del visualizzatore.

   Il segnaposto DIV è un elemento posizionato, il che significa che la proprietà `position` CSS è impostata su `relative` o `absolute`.

   Esempio di un elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   Potete impostare le dimensioni statiche per il visualizzatore dichiarandolo per la classe CSS di livello `.s7spinviewer` principale in unità assolute oppure utilizzando il `stagesize` modificatore.

   Potete inserire le dimensioni in CSS direttamente nella pagina HTML o in un file CSS del visualizzatore personalizzato, che verrà successivamente assegnato a un record del predefinito per visualizzatori in Scene7 Publishing System, oppure trasmesso esplicitamente tramite un comando di stile.

   Consultate [Personalizzazione del visualizzatore](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) 360 gradi per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione di una dimensione visualizzatore statica in una pagina HTML:

   ```
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Potete impostare il `stagesize` modificatore nel record del predefinito per visualizzatori in Scene7 Publishing System oppure passarlo esplicitamente con il codice di inizializzazione del visualizzatore con `params` la raccolta oppure come chiamata API come descritto nella sezione Riferimento comando, come segue:

   ```
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi descritti qui sopra, potete creare un&#39;istanza della `s7viewers.SpinViewer` classe, trasmettere tutte le informazioni di configurazione al relativo costruttore e chiamare `init()` il metodo su un&#39;istanza di visualizzatore. Le informazioni di configurazione vengono trasmesse al costruttore come oggetto JSON. Come minimo, questo oggetto ha `containerId` un campo che contiene il nome dell&#39;ID del contenitore del visualizzatore e dell&#39;oggetto `params` JSON nidificato con i parametri di configurazione supportati dal visualizzatore. In questo caso di `params` un oggetto, deve avere almeno l’URL Image Server passato come `serverUrl` proprietà e la risorsa iniziale come `asset` parametro. L&#39;API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore del visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser ritardano la creazione del DOM fino alla fine della pagina Web. Per garantire la massima compatibilità, chiamate il `init()` metodo immediatamente prima del `BODY` tag di chiusura o dell’ `onload()` evento body.

   Allo stesso tempo, l&#39;elemento contenitore non deve necessariamente essere ancora parte del layout della pagina Web. Ad esempio, potrebbe essere nascosto utilizzando lo stile a esso `display:none` assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del `init()` metodo. L’esempio presuppone `spinViewer` che l’istanza del visualizzatore `s7viewer` sia il nome del segnaposto `DIV`, [!DNL http://s7d1.scene7.com/is/image/] sia l’URL del server immagini e [!DNL Scene7SharedAssets/SpinSet_Sample] sia la risorsa.

   ```
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Il codice seguente è un esempio completo di una pagina Web di dimensioni ridotte che incorpora il visualizzatore 360 gradi con una dimensione fissa:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporazione responsive con altezza illimitata**

Con l’incorporazione reattiva della progettazione, la pagina Web dispone in genere di un layout flessibile che specifica le dimensioni runtime del contenitore del visualizzatore `DIV`. In questo esempio, si supponga che la pagina Web consenta al contenitore del visualizzatore `DIV` di occupare il 40% delle dimensioni della finestra del browser Web, lasciando invariata l’altezza. Il codice HTML della pagina Web risultante sarà simile al seguente:

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

L’aggiunta del visualizzatore a tale pagina è simile all’incorporamento a dimensione fissa, con l’unica differenza che non è necessario definire in modo esplicito le dimensioni del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi indicati sopra sono uguali a quelli con incorporamento a dimensione fissa. Aggiungete il contenitore `DIV` al &quot;titolare&quot; esistente `DIV`. Il codice seguente è un esempio completo. Potete vedere come cambiano le dimensioni del visualizzatore quando viene ridimensionato il browser e come le proporzioni del visualizzatore corrispondono alla risorsa.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

Nella pagina degli esempi seguente sono illustrati i casi di utilizzo più reali di incorporamento reattivo con altezza illimitata del progetto:

[Live Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Incorporazione di dimensioni flessibili con larghezza e altezza definite**

In caso di incorporamento di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina Web è diverso. In altre parole, fornisce entrambe le dimensioni al &quot;detentore&quot; `DIV` e le centra nella finestra del browser. Inoltre, la pagina Web imposta su 100% la dimensione dell’ `HTML` `BODY` elemento e dell’elemento:

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

I passaggi di incorporazione rimanenti sono identici a quelli per l’incorporamento reattivo di progetti con altezza illimitata. L’esempio risultante è il seguente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporazione tramite l&#39;API basata su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. Con questo costruttore di API non accetta parametri e i parametri di configurazione sono specificati utilizzando `setContainerId()`, `setParam()`, e metodi `setAsset()` API con chiamate JavaScript separate.

L&#39;esempio seguente mostra l&#39;incorporamento di dimensioni fisse con l&#39;API basata su setter:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```

