---
description: Il visualizzatore video è un lettore video che riproduce in streaming e video progressivo codificato in formato H.264. Viene fornito da Dynamic Media Classic o AEM Dynamic Media.
keywords: reattivo
solution: Experience Manager
title: Video
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2383'
ht-degree: 0%

---


# Video{#video}

Il visualizzatore video è un lettore video che riproduce in streaming e video progressivo codificato in formato H.264. Viene fornito da Dynamic Media Classic o AEM Dynamic Media.

Consulta [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Sono supportati sia i set video singoli che quelli adattivi. Inoltre, il visualizzatore supporta l’utilizzo di video progressivi e flussi HLS ospitati su posizioni esterne. È progettato per funzionare sia sui browser web desktop che mobili che supportano video HTML5. Questo visualizzatore supporta anche i sottotitoli codificati opzionali visualizzati sopra i contenuti video, la navigazione nei capitoli video e gli strumenti di condivisione dei social media.

Il visualizzatore video utilizza la riproduzione video in streaming HTML5 in formato HLS nella configurazione predefinita ogni volta che il sistema sottostante lo supporta. Nei sistemi che non supportano lo streaming HTML5, il visualizzatore torna alla distribuzione video progressiva HTML5.

Tipo di visualizzatore 506.

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Utilizzo del visualizzatore video {#section-f21ac23d3f6449ad9765588d69584772}

Il visualizzatore video rappresenta un file JavaScript principale e un set di file helper: un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS scaricati dal visualizzatore in fase di esecuzione.

È possibile utilizzare il Visualizzatore video in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con IS-Viewers. In alternativa, puoi utilizzare il visualizzatore in modalità incorporata, dove viene integrato in una pagina web di destinazione utilizzando l’API documentata.

L’attività di configurazione e skin del visualizzatore è simile a quella di altri visualizzatori. Tutta la skin viene ottenuta tramite CSS personalizzati.

Consulta [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento ai comandi comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore video {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore video fornisce una serie di controlli standard dell’interfaccia utente per la riproduzione video, come un pulsante di riproduzione/pausa, una bolla di tempo video per lo scorrimento video, un indicatore di tempo di riproduzione/totale, il controllo del volume, il pulsante a schermo intero e l’interruttore per la didascalia chiusa. Tutti questi controlli sono raggruppati in una barra di controllo nella parte inferiore dell’interfaccia utente del visualizzatore.

Sui dispositivi touch, il controllo del volume è nascosto dall&#39;interfaccia utente, perché è possibile controllare il volume solo utilizzando i pulsanti hardware.

Quando il visualizzatore funziona in modalità pop-up, il pulsante a schermo intero non è disponibile nell’interfaccia utente.

È possibile navigare rapidamente nel contenuto di un video quando si attiva il filtro video. I capitoli video vengono visualizzati come marcatori nella traccia di scorrimento video e mostrano il titolo del capitolo e la relativa descrizione su un rotolo del mouse o con un singolo tocco sui sistemi touch. Gli utenti possono cercare un capitolo specifico cliccando su un marcatore di capitolo o toccando la bolla di descrizione del capitolo.

Il visualizzatore supporta sia l’input touch che l’input del mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Consulta [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Strumenti per la condivisione di social media con il visualizzatore video {#section-907d316fe1da4b87abb9775f02464704}

Il visualizzatore video supporta gli strumenti di condivisione dei social media Sono disponibili come un singolo pulsante nell’interfaccia utente che si espande in una barra degli strumenti di condivisione quando l’utente fa clic o tocca su di essa.

La barra degli strumenti di condivisione contiene un&#39;icona per ogni tipo di canale di condivisione supportato come Facebook, Twitter, condivisione e-mail, condivisione del codice di incorporamento e condivisione dei collegamenti. Quando si attivano gli strumenti di condivisione e-mail, incorporamento o collegamento, il visualizzatore visualizza una finestra di dialogo modale con un modulo di immissione dati corrispondente. Quando si chiamano Facebook o Twitter, il visualizzatore reindirizzerà l&#39;utente a una finestra di dialogo di condivisione standard da un servizio di social media. Anche quando uno strumento di condivisione viene attivato, la riproduzione video viene messa in pausa automaticamente.

Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di sicurezza del browser Web.

## Incorporamento del visualizzatore video {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, quando fai clic su di essa, apre il visualizzatore in una finestra separata del browser. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare un design reattivo che viene visualizzato in modo diverso su diversi dispositivi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: a comparsa, incorporazione a dimensione fissa e incorporazione responsive della progettazione.

L’incorporazione di più video sulla stessa pagina è supportata sui tablet e sui dispositivi mobili. Nella maggior parte dei casi, è possibile riprodurre un solo video alla volta. Quando un utente inizia a riprodurre un video e poi prova a riprodurre un altro video, il primo video viene messo in pausa automaticamente. Il video messo in pausa automaticamente ricorda il tempo di riproduzione corrente, in modo che l&#39;utente possa sempre tornare ad esso e riprendere la riproduzione. L&#39;unica eccezione questa regola è nel browser Chrome su dispositivi Android 4.x, che può riprodurre video in parallelo.

**Informazioni sulla modalità a comparsa**

In modalità pop-up il visualizzatore viene aperto in una finestra o scheda separata del browser Web. Prende l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l&#39;orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` una chiamata JavaScript, un elemento `A` HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML predefinita per la modalità di funzionamento a comparsa. Si chiama [!DNL VideoViewer.html] e si trova nella sottocartella [!DNL html5/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Puoi ottenere la personalizzazione visiva applicando CSS personalizzati.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento reattiva**

Nella modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe avere già alcuni contenuti del cliente non correlati al visualizzatore. Normalmente lo spettatore occupa solo una parte del patrimonio immobiliare della pagina web.

Il caso d’uso principale sono le pagine web orientate ai desktop o ai dispositivi tablet, nonché le pagine di progettazione reattiva che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporazione a dimensione fissa viene utilizzata quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questa opzione è la migliore per le pagine web con layout di pagina statico.

L’incorporazione di design reattivo presuppone che il visualizzatore debba ridimensionare in fase di esecuzione in risposta alla modifica delle dimensioni del contenitore `DIV`. Il caso d’uso più comune è l’aggiunta del visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

In modalità di incorporamento della progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il proprio contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando senza limitazioni l’altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questo metodo assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura laterale. Questo caso d’uso è il più comune per le pagine web che utilizzano un framework di layout dinamico come Bootstrap, Foundation e così via.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza del contenitore del visualizzatore `DIV`, il visualizzatore compila solo quell’area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio è quello di incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina web, effettua le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL FlyoutViewer.js]. Il file [!DNL FlyoutViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Dynamic Media Classic di Adobe e viene servito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Dynamic Media Classic di Adobe in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>Dovresti fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non devi fare riferimento a file JavaScript aggiuntivi nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente alla libreria HTML5 SDK `Utils.js` caricata dal visualizzatore dal percorso contestuale `/s7viewers` (cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o librerie di visualizzatori runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, l’inserimento di un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore DIV.

   Aggiungi un elemento DIV vuoto alla pagina in cui desideri che appaia il visualizzatore. L’ID dell’elemento DIV deve essere definito perché viene passato successivamente all’API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il segnaposto DIV è un elemento posizionato, il che significa che la proprietà CSS `position` è impostata su `relative` o `absolute`.

   Assicurati che la funzione a schermo intero funzioni correttamente in Internet Explorer. Controlla che non ci siano altri elementi nel DOM con un ordine di impilamento più alto del tuo segnaposto DIV.

   Di seguito è riportato un esempio di elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica del visualizzatore dichiarandola per la classe CSS di livello principale `.s7videoviewer` in unità assolute o utilizzando il modificatore `stagesize`.

   Le dimensioni in CSS possono essere posizionate direttamente sulla pagina HTML o in un file CSS per visualizzatori personalizzati, che viene successivamente assegnato a un record predefinito per visualizzatori in Dynamic Media Classic o passato esplicitamente utilizzando un comando di stile.

   Per ulteriori informazioni sullo stile del visualizzatore tramite CSS, consulta [Personalizzazione del visualizzatore video](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) .

   Di seguito è riportato un esempio di definizione delle dimensioni di un visualizzatore statico in una pagina HTML:

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puoi impostare il modificatore `stagesize` nel record predefinito del visualizzatore in Dynamic Media Classic, oppure passarlo esplicitamente con il codice di inizializzazione del visualizzatore con la raccolta `params` oppure come chiamata API come descritto nella sezione Riferimento comando , come segue:

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza della classe `s7viewers.VideoViewer`, passa tutte le informazioni di configurazione al relativo costruttore e chiama il metodo `init()` su un’istanza di visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere un campo `containerId` che contiene il nome dell’ID del contenitore del visualizzatore e un oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore. In questo caso, l’oggetto `params` deve avere almeno l’URL Image Server passato come proprietà `serverUrl` , l’URL del server video passato come proprietà `videoserverurl` e la risorsa iniziale come parametro `asset` . L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()` .

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web per ora. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza di visualizzatore, passaggio al costruttore delle opzioni di configurazione minime necessarie e chiamata del metodo `init()` . Questo esempio presuppone che `videoViewer` sia l’istanza del visualizzatore, che `s7viewer` sia il nome del segnaposto `DIV`, che [!DNL http://s7d1.scene7.com/is/image/] sia l’URL del server immagini, che [!DNL http://s7d1.scene7.com/is/content/] sia l’URL del server video e che la risorsa sia [!DNL Scene7SharedAssets/Glacier_Climber_MP4].

   ```
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   Il codice seguente è un esempio completo di una pagina web banale che incorpora il visualizzatore video con dimensioni fisse:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var videoViewer = new s7viewers.VideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Incorporazione di design reattivo con altezza illimitata**

Con l’incorporazione del design reattivo, la pagina web dispone normalmente di un layout flessibile che determina la dimensione in fase di esecuzione del contenitore del visualizzatore `DIV`. Ai fini di questo esempio, si supponga che la pagina web consenta al contenitore del visualizzatore `DIV` di assumere il 40% delle dimensioni della finestra del browser Web, lasciando senza limitazioni l’altezza. Il codice HTML della pagina web sarà simile al seguente:

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

L’aggiunta del visualizzatore a una pagina di questo tipo è molto simile all’incorporazione con dimensioni fisse; l’unica differenza è che non è necessario definire esplicitamente la dimensione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell&#39;incorporazione con dimensione fissa. Aggiungi il contenitore `DIV` al &quot; holder&quot; esistente `DIV`. Il codice seguente è un esempio completo. Puoi vedere come cambia la dimensione del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La pagina degli esempi seguenti illustra l’utilizzo più reale di elementi di design reattivi con altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

**Incorporazione responsive con larghezza e altezza definite**

In caso di incorporamento dinamico del design con larghezza e altezza definite, lo stile della pagina web è diverso; fornisce entrambe le dimensioni al &quot; holder&quot; `DIV` e centralo nella finestra del browser. Inoltre, la pagina web imposta le dimensioni degli elementi `HTML` e `BODY` su 100%:

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

I passaggi rimanenti per l’incorporazione sono identici a quelli per l’incorporazione di progetti reattivi con altezza illimitata. L’esempio risultante è il seguente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
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
var videoViewer = new s7viewers.VideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Glacier_Climber_MP4", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Incorporazione tramite API basate su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. Con tale API, il costruttore non accetta alcun parametro e i parametri di configurazione vengono specificati utilizzando i metodi `setContainerId()`, `setParam()` e `setAsset()` API con chiamate JavaScript separate.

L’esempio seguente illustra l’incorporazione di dimensioni fisse con API basata su setter:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/VideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7videoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var videoViewer = new s7viewers.VideoViewer(); 
videoViewer.setContainerId("s7viewer"); 
videoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
videoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
videoViewer.setAsset("Scene7SharedAssets/Glacier_Climber_MP4"); 
videoViewer.init(); 
</script> 
</body> 
</html> 
```

