---
title: Zoom di base
description: Basic Zoom Viewer è un visualizzatore di immagini che visualizza una singola immagine zoomabile. Ha strumenti di zoom, supporto a schermo intero e un pulsante ravvicinato opzionale. Questo visualizzatore è il più leggero. È progettato per funzionare su desktop e dispositivi mobili.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: ee15ce21-20c4-428b-9512-050115e4c322
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1998'
ht-degree: 0%

---

# Zoom di base{#basic-zoom}

Visualizzatore zoom di base è un visualizzatore di immagini che visualizza una singola immagine ingrandita. Dispone di strumenti zoom, supporto per schermo intero e un pulsante di chiusura opzionale. Questo visualizzatore è il più leggero. È progettato per funzionare su desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (rendering Immagine) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Tipo di visualizzatore 501.

Vedere [requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B](https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B)

## Utilizzo del visualizzatore Zoom di base {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore Zoom di base rappresenta un file di JavaScript e un set di file di supporto che il visualizzatore scarica in fase di runtime. Essenzialmente, si tratta di un singolo JavaScript includere con tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS.

È possibile utilizzare Basic Zoom Viewer in modalità finestra a comparsa utilizzando una pagina HTML pronta per la produzione fornita con IS-Viewers o in modalità incorporata, dove è integrata in destinazione pagina Web utilizzando l&#39;API documentata.

La configurazione e lo skinning sono simili a quelli degli altri visualizzatori. Tutte le interfacce vengono eseguite tramite CSS personalizzati.

Vedere [Comando riferimento comune a tutti i visualizzatori - Attributi](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) di configurazione e [riferimento Comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore Zoom base {#section-642e66ca38cd4032992840ec6c0b0cd2}

Basic Zoom Viewer supporta i seguenti gesti touch comuni in altre applicazioni mobili.

Quando il visualizzatore non è in grado di elaborare il gesto di scorrimento di un utente, inoltra l&#39;evento al browser Web per eseguire uno scorrimento nativo pagina. Questo tipo di funzionalità consente al utente di spostarsi nella pagina lineare se il visualizzatore occupa la maggior parte dell&#39;area dello schermo del dispositivo.

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
   <td colname="col2"> <p>Nasconde o rivela utente elementi dell'interfaccia. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doppio tocco </p> </td> 
   <td colname="col2"> <p> Ingrandisce un livello fino a raggiungere il massimo ingrandimento. Il gesto successivo di doppio tocco riporta il visualizzatore allo stato di visualizzazione iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pizzicare </p> </td> 
   <td colname="col2"> <p>Ingrandisce o riduce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento </p> </td> 
   <td colname="col2"> <p> Se l'immagine è reimpostata, il movimento esegue uno scorrimento nativo della pagina. </p> <p> Quando l'immagine viene ingrandita, l'immagine viene spostata. Se l'immagine viene spostata sul bordo della vista e viene eseguito un passaggio di scorrimento in quella direzione, il movimento esegue uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta inoltre l&#39;input tocco e mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Consulta [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore zoom di base {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, se selezionato, apre il visualizzatore in una finestra del browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare una progettazione reattiva che viene visualizzata in modo diverso su dispositivi diversi o per dimensioni diverse della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità operative principali: finestra a comparsa, incorporazione a dimensione fissa e incorporazione dinamico progettazione.

**Informazioni sulla modalità finestra a comparsa**

In finestra a comparsa modalità, il visualizzatore viene aperto in una finestra o in una scheda separata del browser. Occupa l&#39;intera area della finestra browser e si regola nel caso in cui il browser venga ridimensionato o l&#39;orientamento del dispositivo venga modificato.

La modalità pop-up è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando la chiamata JavaScript, un `window.open()` elemento HTML configurato correttamente `A` o qualsiasi altro metodo adatto.

Si consiglia di utilizzare una pagina HTML pronta all&#39;uso per finestra a comparsa modalità operativa. In questo caso, si chiama [!DNL BasicZoomViewer.html] e si trova nella sottocartella [!DNL html5/] della distribuzione IS-Viewers standard:

[!DNL <s7viewers_root>/html5/BasicZoomViewer.html]

Puoi ottenere una personalizzazione visiva applicando CSS personalizzata.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset=Scene7SharedAssets/Backpack_B" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento di progettazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe già avere alcuni contenuti per i clienti non correlati al visualizzatore. Il visualizzatore occupa normalmente solo una parte del patrimonio immobiliare di una pagina web.

I casi d&#39;uso principali sono le pagine Web orientate per desktop o dispositivi tablet e anche dinamico pagine progettate che regolano automaticamente il layout a seconda del tipo di dispositivo.

L&#39;incorporazione a dimensione fissa viene utilizzata quando la dimensione del visualizzatore non viene modificata dopo il caricamento iniziale. Questo metodo è la scelta migliore per le pagine Web con un layout statico.

L&#39;incorporamento di progettazione reattiva presuppone che il visualizzatore debba ridimensionarsi in fase di esecuzione in risposta al cambiamento di dimensione del suo contenitore `DIV`. Il caso d&#39;uso più comune è l&#39;aggiunta di un visualizzatore a una pagina Web che utilizza un layout di pagina flessibile.

In dinamico modalità di incorporamento della progettazione, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina Web ridimensiona il suo contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando la sua altezza senza restrizioni, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni del risorsa che viene utilizzato. Questa funzionalità assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura sui lati. Questo caso d&#39;uso è il più comune per le pagine Web che utilizzano framework di layout design responsive like Bootstrap e Foundation.

In caso contrario, se la pagina Web imposta sia la larghezza che l&#39;altezza per il contenitore `DIV`del visualizzatore, il visualizzatore riempie solo quell&#39;area e segue le dimensioni fornite dal layout della pagina Web. Un buon esempio consiste nell&#39;incorporare il visualizzatore in un sovrapposizione modale, in cui il sovrapposizione viene ridimensionato in base alle dimensioni della finestra Web browser.

**Incorporazione a dimensione fissa**

È possibile aggiungere il visualizzatore a una pagina Web eseguendo le operazioni seguenti:

1. Aggiunta del file JavaScript visualizzatore alla pagina Web.
1. Definizione del DIV del contenitore.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l&#39;API visualizzatore, assicurati di includere [!DNL BasicZoomViewer.js]. Il file [!DNL BasicZoomViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/BasicZoomViewer.js]

È possibile utilizzare un percorso relativo se il visualizzatore è distribuito in uno dei server Adobe Systems Dynamic Media Classic e viene servito dallo stesso dominio. In caso contrario, si specifica il percorso completo di uno dei server Adobe Systems Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta like seguente:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/BasicZoomViewer.js"></script>
```

>[!NOTE]
>
>Fate riferimento solo al file JavaScript `include` del visualizzatore principale nella pagina. Non fare riferimento ad altri file JavaScript nel codice della pagina Web che potrebbero essere scaricati dalla logica del visualizzatore in fase di runtime. In particolare, non fare riferimento direttamente all&#39;SDK `Utils.js` HTML5 libreria caricato dal visualizzatore dal `/s7viewers` percorso di contesto (c.d. SDK `include`consolidato). La ragione è che la posizione di `Utils.js` un librerie di runtime o simile visualizzatore è completamente gestita dalla logica del visualizzatore e la posizione cambia tra visualizzatore versioni. Adobe Systems non mantiene sul server le versioni precedenti dei visualizzatore `includes` secondari.
>
>
>Di conseguenza, l&#39;inserimento di un riferimento diretto a qualsiasi JavaScript `include` secondario utilizzato dal visualizzatore nella pagina interrompe la funzionalità visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore DIV.

   Aggiungi un elemento DIV vuoto alla pagina in cui desideri visualizzare il visualizzatore. L&#39;ID definito per l&#39;elemento DIV deve essere definito perché questo ID viene passato successivamente all&#39;API visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il DIV segnaposto è un elemento posizionato, il che significa che la `position` proprietà CSS è impostata su `relative` o `absolute`.

   Di seguito è riportato un esempio di elemento DIV segnaposto definito:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni visualizzatore

   È possibile impostare la dimensione statica per il visualizzatore dichiarandola per `.s7basiczoomviewer` la classe CSS di primo livello in unità assolute o utilizzando `stagesize` il modificatore.

   Inserisci il ridimensionamento in CSS direttamente nella pagina HTML o in un file CSS visualizzatore personalizzato. Viene quindi successivamente assegnato a un record preimpostato visualizzatore in Dynamic Media Classic o passato esplicitamente utilizzando un comando di stile.

   Per ulteriori informazioni sullo stile dei visualizzatore con CSS, consultate [Personalizzazione del visualizzatore](../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-customizingviewer/c-html5-20-basic-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) Zoom di base.

   Di seguito è riportato un esempio di definizione di una dimensione visualizzatore statica in una pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7basiczoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Potete impostare `stagesize` il modificatore nel record del predefinito visualizzatore in Dynamic Media Classic. In alternativa, puoi passarlo in modo esplicito con il codice di inizializzazione del visualizzatore con `params` raccolta oppure, come chiamata API come descritto nella sezione Comando Reference, like quanto segue:

   ```html {.line-numbers}
   basicZoomViewer.setParam("stagesize", "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, creare un istanza di classe, passare tutte le informazioni di `s7viewers.BasicZoomViewer` configurazione al relativo costruttore e chiamare `init()` il metodo su un visualizzatore istanza. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto deve avere almeno un campo containerId che contiene il nome del visualizzatore `container ID` e un oggetto JSON `params` nidificato con i parametri di configurazione supportati dal visualizzatore. In questo caso, l&#39;oggetto `params` deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sul corpo dell&#39;evento `onload()`.

   Allo stesso tempo, l’elemento contenitore non deve ancora necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questo evento, il caricamento della visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un istanza di visualizzatore, passando le opzioni di configurazione minime necessarie al costruttore e chiamando il `init()` metodo. Nell&#39;esempio si `basicZoomViewer` presuppone che il visualizzatore istanza; `s7viewer` sia il nome del segnaposto `DIV`; `http://s7d1.scene7.com/is/image/` sia il Immagine che serve URL e `Scene7SharedAssets/Backpack_B` sia il risorsa:

   ```html {.line-numbers}
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

   Il codice seguente è un esempio completo di una pagina Web banale che incorpora il visualizzatore Zoom base con una dimensione fissa:

   ```html {.line-numbers}
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

**Incorporamento di design reattivo con altezza illimitata**

Con dinamico incorporamento del design, la pagina Web normalmente ha una sorta di layout flessibile che determina la dimensione di runtime del contenitore `DIV`del visualizzatore. Per l&#39;esempio seguente, si supponga che la pagina Web consenta al contenitore `DIV` del visualizzatore di occupare il 40% delle dimensioni della finestra del browser Web, lasciandone illimitata l&#39;altezza. Il codice HTML della pagina Web avrà un aspetto like seguente:

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

L&#39;aggiunta del visualizzatore a tale pagina è simile ai passaggi per l&#39;incorporamento a dimensione fissa. L&#39;unica differenza consiste nel fatto che non è necessario definire in modo esplicito le dimensioni visualizzatore.

1. Aggiunta del file JavaScript visualizzatore alla pagina Web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell’incorporamento di dimensioni fisse. Aggiungere il DIV contenitore al DIV `"holder"` esistente. Il codice seguente è un esempio completo. Osserva come cambiano le dimensioni del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```html {.line-numbers}
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

La pagina di esempi seguente illustra usi più reali dell’incorporamento di design responsive con altezza illimitata:

[Demo Live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Dimensione flessibile incorporata con larghezza e altezza definite**

Se è presente un incorporamento di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina Web è diverso. Fornisce entrambe le dimensioni al `"holder"` DIV e lo centra nella finestra browser. Inoltre, la pagina Web imposta la dimensione dell&#39;elemento `HTML` and `BODY` su 100%.

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

Gli altri passaggi di incorporamento sono identici ai passaggi utilizzati per dinamico incorporazione con altezza illimitata. L&#39;esempio risultante è il seguente:

```html {.line-numbers}
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

**Incorporamento mediante API basata su Setter**

Invece di utilizzare l’inizializzazione basata su JSON, puoi utilizzare l’API basata su setter e il costruttore no-args. L&#39;utilizzo di questo costruttore API non accetta parametri e i parametri di configurazione sono specificati utilizzando i metodi API `setContainerId()`, `setParam()` e `setAsset()` con chiamate JavaScript separate.

L&#39;esempio seguente illustra l&#39;utilizzo dell&#39;incorporamento a dimensione fissa con API basata su Setter:

```html {.line-numbers}
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
