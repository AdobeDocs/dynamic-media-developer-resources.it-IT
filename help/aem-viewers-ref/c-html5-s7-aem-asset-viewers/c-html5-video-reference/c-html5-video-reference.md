---
description: Il visualizzatore video è un lettore video che riproduce lo streaming e il video progressivo codificati in formato H.264. Viene distribuito da Scene7 Publishing System o AEM Dynamic Media.
keywords: responsive
seo-description: Il visualizzatore video è un lettore video che riproduce lo streaming e il video progressivo codificati in formato H.264. Viene distribuito da Scene7 Publishing System o AEM Dynamic Media.
seo-title: Video
solution: Experience Manager
title: Video
topic: Dynamic media
uuid: 961a9b99-5892-4ee3-a2df-13e299f5d086
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Video{#video}

Il visualizzatore video è un lettore video che riproduce lo streaming e il video progressivo codificati in formato H.264. Viene distribuito da Scene7 Publishing System o AEM Dynamic Media.

Consultate Requisiti di [sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Sono supportati sia i singoli video che i set video adattivi. Inoltre, il visualizzatore supporta l&#39;utilizzo di video progressivi e flussi HLS ospitati su posizioni esterne. È progettata per funzionare sia sui browser Web desktop che sui browser mobili che supportano video HTML5. Questo visualizzatore supporta anche i sottotitoli codificati facoltativi visualizzati sopra il contenuto video, la navigazione dei capitoli video e gli strumenti di condivisione social media.

Il visualizzatore video utilizza la riproduzione di video in streaming HTML5 in formato HLS nella configurazione predefinita ogni volta che il sistema sottostante lo supporta. Sui sistemi che non supportano lo streaming HTML5, il visualizzatore torna alla distribuzione video progressiva HTML5.

Tipo di visualizzatore 506.

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Utilizzo del visualizzatore video {#section-f21ac23d3f6449ad9765588d69584772}

Il visualizzatore video rappresenta un file JavaScript principale e un set di file di supporto, una singola inclusione JavaScript con tutti i componenti SDK per visualizzatori utilizzati da questo particolare visualizzatore, risorse e CSS scaricati dal visualizzatore in fase di esecuzione.

Potete usare il visualizzatore video in modalità a comparsa utilizzando la pagina HTML pronta per la produzione fornita con i visualizzatori IS. Oppure, potete utilizzare il visualizzatore in modalità incorporata, dove viene integrato in una pagina Web di destinazione tramite l&#39;API documentata.

La configurazione e l’associazione di interfacce al visualizzatore sono simili agli altri visualizzatori. L’associazione di interfacce viene realizzata tramite CSS personalizzato.

Consultate Riferimento [comando comune a tutti i visualizzatori - Attributi](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) di configurazione e Riferimento [comando comuni a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore video {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore video offre una serie di controlli standard dell’interfaccia utente per la riproduzione video, come un pulsante di riproduzione/pausa, una bolla temporale del video per lo scorrimento video, un indicatore del tempo di riproduzione/totale, un controllo del volume, un pulsante a schermo intero e un interruttore per la didascalia chiusa. Tutti questi controlli sono raggruppati in una barra di controllo nella parte inferiore dell’interfaccia utente del visualizzatore.

Sui dispositivi touch, il controllo del volume è nascosto dall&#39;interfaccia utente, perché è possibile controllare il volume solo utilizzando i pulsanti hardware.

Quando il visualizzatore funziona in modalità pop-up, il pulsante a schermo intero non è disponibile nell&#39;interfaccia utente.

È possibile navigare rapidamente nel contenuto di un video quando si attiva il filtro per video. I capitoli video sono visualizzati come marcatori nella traccia di scorrimento video e mostrano il titolo del capitolo e la descrizione associata su un passaggio del mouse o con un singolo tocco sui sistemi touch. Gli utenti possono cercare un particolare capitolo facendo clic su un marcatore di capitolo o toccando la bolla della descrizione del capitolo.

Il visualizzatore supporta sia l&#39;input touch che l&#39;input del mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser Web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile tramite tastiera.

Consultate Accesso [e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)da tastiera.

## Strumenti di condivisione per social media con il visualizzatore video {#section-907d316fe1da4b87abb9775f02464704}

Il visualizzatore video supporta gli strumenti di condivisione per social media Sono disponibili come un singolo pulsante nell’interfaccia utente che si espande in una barra degli strumenti di condivisione quando l’utente fa clic su di essa o vi tocca.

La barra degli strumenti di condivisione contiene un&#39;icona per ciascun tipo di canale di condivisione supportato, ad esempio Facebook, Twitter, condivisione e-mail, condivisione del codice da incorporare e condivisione dei collegamenti. Quando si attivano gli strumenti di condivisione e-mail, incorpora o collega, il visualizzatore visualizza una finestra di dialogo modale con un modulo di immissione dati corrispondente. Quando Facebook o Twitter vengono chiamati, il visualizzatore reindirizzerà l&#39;utente a una finestra di dialogo di condivisione standard da un servizio di social media. Anche quando uno strumento di condivisione è attivato, la riproduzione video viene messa in pausa automaticamente.

Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di protezione del browser Web.

## Incorporazione del visualizzatore video {#section-6bb5d3c502544ad18a58eafe12a13435}

Diverse pagine Web hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina Web fornisce un collegamento che, quando viene fatto clic, apre il visualizzatore in una finestra browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest&#39;ultimo caso, la pagina Web può avere un layout di pagina statico oppure utilizzare un design reattivo che viene visualizzato in modo diverso su diversi dispositivi o per diverse dimensioni di finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: finestre a comparsa, incorporamento a dimensione fissa e incorporazione reattiva della progettazione.

L&#39;incorporamento di più video sulla stessa pagina è supportato su tablet e dispositivi mobili. Nella maggior parte dei casi, è possibile riprodurre un solo video alla volta. Quando un utente avvia la riproduzione di un video e tenta di riprodurre un altro video, il primo video viene automaticamente messo in pausa. Il video che è stato messo in pausa automatica ricorda il tempo di riproduzione corrente, in modo che l’utente possa sempre tornare al video e riprendere la riproduzione. L&#39;unica eccezione questa regola è nel browser Chrome su dispositivi Android 4.x, che può riprodurre video in parallelo.

**Informazioni sulla modalità a comparsa**

In modalità pop-up, il visualizzatore viene aperto in una finestra o in una scheda separata del browser Web. Richiede l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l&#39;orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando la chiamata `window.open()` JavaScript, l’elemento `A` HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML out-of-box per la modalità operativa a comparsa. Viene chiamato [!DNL VideoViewer.html] e si trova nella [!DNL html5/] sottocartella della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Potete ottenere la personalizzazione visiva applicando CSS personalizzato.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina Web esistente, che potrebbe già presentare contenuti per clienti non correlati al visualizzatore. In genere, il visualizzatore occupa solo una parte del patrimonio immobiliare della pagina Web.

I casi d’uso principali sono le pagine Web orientate per desktop o dispositivi tablet, nonché le pagine di progettazione reattiva che adattano automaticamente il layout in base al tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica la dimensione dopo il caricamento iniziale. Questa è la scelta migliore per le pagine Web con layout di pagina statico.

L’incorporazione di una progettazione reattiva presuppone che il visualizzatore debba ridimensionare in fase di esecuzione in risposta alla modifica delle dimensioni del suo contenitore `DIV`. L’esempio più comune è l’aggiunta del visualizzatore a una pagina Web con layout di pagina flessibile.

In modalità di incorporazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina Web ridimensiona il proprio contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`e ne lascia invariata l’altezza, il visualizzatore sceglie automaticamente l’altezza in base alle proporzioni della risorsa utilizzata. Questo metodo garantisce che la risorsa si adatti perfettamente alla vista senza riempimenti laterali. Questo caso di utilizzo è il più comune per le pagine Web che utilizzano un framework di layout reattivo come Bootstrap, Foundation e così via.

In caso contrario, se la pagina Web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore compila solo tale area e segue le dimensioni fornite dal layout della pagina Web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser Web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuate le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell&#39;intestazione HTML. Prima di poter utilizzare l&#39;API del visualizzatore, accertatevi di includerla [!DNL FlyoutViewer.js]. Il [!DNL FlyoutViewer.js] file si trova nella [!DNL html5/js/] sottocartella della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Potete usare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene distribuito dallo stesso dominio. In caso contrario, specificate un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
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

   Assicurarsi che la funzione a schermo intero funzioni correttamente in Internet Explorer. Verificate che nel DOM non vi siano altri elementi con un ordine di sovrapposizione superiore a quello del DIV segnaposto.

   Esempio di un elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore

   Potete impostare le dimensioni statiche per il visualizzatore dichiarandolo per la classe CSS di livello `.s7videoviewer` principale in unità assolute oppure utilizzando il modificatore `stagesize`.

   Il ridimensionamento in CSS può essere inserito direttamente nella pagina HTML o in un file CSS del visualizzatore personalizzato, che verrà successivamente assegnato a un record di predefinito per visualizzatori in Scene7 Publishing System o trasmesso esplicitamente utilizzando un comando di stile.

   Consultate [Personalizzazione del visualizzatore](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) video per ulteriori informazioni sullo stile del visualizzatore mediante CSS.

   Di seguito è riportato un esempio di definizione di una dimensione visualizzatore statica in una pagina HTML:

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Potete impostare `stagesize` il modificatore nel record del predefinito per visualizzatori in Scene7 Publishing System oppure passarlo esplicitamente con il codice di inizializzazione del visualizzatore con `params` la raccolta oppure come chiamata API come descritto nella sezione Riferimento comando, come segue:

   ```
   videoViewer.setParam("stagesize", "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi descritti qui sopra, potete creare un&#39;istanza della `s7viewers.VideoViewer` classe, trasmettere tutte le informazioni di configurazione al relativo costruttore e chiamare `init()` il metodo su un&#39;istanza di visualizzatore. Le informazioni di configurazione vengono trasmesse al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere `containerId` `params` un campo che contiene il nome dell’ID del contenitore del visualizzatore e un oggetto JSON nidificato con i parametri di configurazione supportati dal visualizzatore. In questo caso, `params` l’oggetto deve avere almeno l’URL Image Server passato come `serverUrl` proprietà, l’URL del server video trasmesso come `videoserverurl` proprietà e la risorsa iniziale come `asset` parametro. L&#39;API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore del visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser ritardano la creazione del DOM fino alla fine della pagina Web. Per garantire la massima compatibilità, chiamate il `init()` metodo immediatamente prima del `BODY` tag di chiusura o dell’ `onload()` evento body.

   Allo stesso tempo, l&#39;elemento contenitore non deve necessariamente far parte del layout della pagina Web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` lo stile assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del `init()` metodo. Questo esempio presuppone `videoViewer` che l’istanza del visualizzatore `s7viewer` sia il nome del segnaposto `DIV`, [!DNL http://s7d1.scene7.com/is/image/] sia l’URL del server immagini, [!DNL http://s7d1.scene7.com/is/content/] sia l’URL del server video e [!DNL Scene7SharedAssets/Glacier_Climber_MP4] sia la risorsa.

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

   Il codice seguente è un esempio completo di una pagina Web banale che incorpora il visualizzatore video con una dimensione fissa:

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

**Incorporazione responsive con altezza illimitata**

Con l’incorporazione reattiva della progettazione, la pagina Web dispone in genere di un layout flessibile che specifica la dimensione in fase di esecuzione del contenitore del visualizzatore `DIV`. In questo esempio, si supponga che la pagina Web consenta al contenitore del visualizzatore `DIV` di occupare il 40% delle dimensioni della finestra del browser Web, lasciando invariata l’altezza. Il codice HTML della pagina Web sarà simile al seguente:

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

L&#39;aggiunta del visualizzatore a tale pagina è molto simile all&#39;incorporazione a dimensione fissa; l’unica differenza è che non è necessario definire in modo esplicito le dimensioni del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi indicati sopra sono uguali a quelli con l&#39;incorporamento a dimensione fissa. Aggiungere un contenitore `DIV` al &quot;titolare&quot; esistente `DIV`. Il codice seguente è un esempio completo. Potete vedere come cambiano le dimensioni del visualizzatore quando viene ridimensionato il browser e come le proporzioni del visualizzatore corrispondono alla risorsa.

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

La pagina degli esempi seguente illustra l’utilizzo più reale di incorporamento reattivo con un’altezza illimitata del design:

[https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html](https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html)

**Incorporazione reattiva con larghezza e altezza definite**

In caso di incorporamento reattivo con larghezza e altezza definite, lo stile della pagina Web è diverso; fornisce entrambe le dimensioni al &quot;titolare&quot; `DIV` e centrarlo nella finestra del browser. Inoltre, la pagina Web imposta su 100% la dimensione dell’ `HTML` `BODY` elemento e dell’elemento:

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

**Incorporazione tramite l&#39;API basata su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. Con tale API, il costruttore non accetta parametri e i parametri di configurazione sono specificati utilizzando `setContainerId()`, `setParam()`e metodi `setAsset()` API con chiamate JavaScript separate.

L&#39;esempio seguente illustra l&#39;incorporamento di dimensioni fisse con l&#39;API basata su setter:

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

