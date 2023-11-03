---
title: Video
description: Il Visualizzatore video è un lettore video che riproduce video in streaming e video progressivo codificati nel formato H.264. Viene fornito da Dynamic Media Classic o Adobe Experience Manager con Dynamic Medie.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: fa9727dc-f9e2-4d91-b500-445693dfb6aa
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2368'
ht-degree: 0%

---

# Video{#video}

Il Visualizzatore video è un lettore video che riproduce video in streaming e video progressivo codificati nel formato H.264. Viene fornito da Dynamic Media Classic o Experience Manager con Dynamic Medie.

Consulta [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Sono supportati sia set per video singolo che set per video adattivi. Inoltre, il visualizzatore supporta l’utilizzo di video progressivi e flussi HLS in hosting su posizioni esterne. È progettato per funzionare sia su browser Web desktop che mobili che supportano video HTML5. Questo visualizzatore supporta anche sottotitoli codificati facoltativi visualizzati sopra al contenuto video, alla navigazione dei capitoli video e agli strumenti di condivisione dei social media.

Il Visualizzatore video utilizza la riproduzione video in streaming HTML5 in formato HLS nella sua configurazione predefinita ogni volta che il sistema sottostante lo supporta. Sui sistemi che non supportano lo streaming HTML5, il visualizzatore torna alla distribuzione di video progressivi HTML5.

Visualizzatore di tipo 506.

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4](https://s7d9.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4)

## Utilizzo del Visualizzatore video {#section-f21ac23d3f6449ad9765588d69584772}

Il Visualizzatore video rappresenta un file JavaScript principale e un set di file di supporto, un singolo file JavaScript da includere con tutti i componenti SDK del Visualizzatore utilizzati da questo particolare visualizzatore, le risorse e i file CSS scaricati dal visualizzatore in fase di esecuzione.

È possibile utilizzare il Visualizzatore video in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con i visualizzatori IS. In alternativa, puoi utilizzare il visualizzatore in modalità incorporata, dove viene integrato in una pagina web di destinazione utilizzando l’API documentata.

L’operazione di configurazione e interpolazione del visualizzatore è simile a quella di altri visualizzatori. Tutte le operazioni di skin vengono eseguite tramite CSS personalizzato.

Consulta [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore video {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Visualizzatore video offre una serie di controlli standard dell’interfaccia utente per la riproduzione video, come un pulsante di riproduzione/pausa, una bolla di tempo video con scorrimento video, un indicatore di tempo totale/tempo di riproduzione, un controllo del volume, un pulsante a schermo intero e un interruttore per sottotitoli. Tutti questi controlli sono raggruppati in una barra di controllo nella parte inferiore dell&#39;interfaccia utente del visualizzatore.

Sui dispositivi touch, il controllo del volume è nascosto dall&#39;interfaccia utente, perché è possibile controllare il volume solo utilizzando i pulsanti hardware.

Quando il visualizzatore funziona in modalità pop-up, il pulsante a schermo intero non è disponibile nell’interfaccia utente.

È possibile navigare rapidamente nel contenuto di un video quando il capitolo video è attivato. I capitoli video vengono visualizzati come marcatori nella traccia di scorrimento video e mostrano il titolo del capitolo e la descrizione associata al passaggio del mouse o con un solo tocco sui sistemi touch. Gli utenti possono cercare un capitolo particolare selezionando un marcatore di capitolo o selezionando la bolla di descrizione del capitolo.

Il visualizzatore supporta sia l&#39;input tocco che l&#39;input del mouse su dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Consulta [Accessibilità della tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Strumenti per la condivisione di social media con il visualizzatore video {#section-907d316fe1da4b87abb9775f02464704}

Il Visualizzatore video supporta gli strumenti di condivisione dei social media. Sono disponibili come pulsante singolo nell’interfaccia utente, che si espande in una barra degli strumenti di condivisione quando l’utente fa clic o tocca su di essa.

La barra degli strumenti Condivisione contiene un’icona per ogni tipo di canale di condivisione supportato, ad esempio Facebook, Twitter, condivisione e-mail, condivisione di codice da incorporare e condivisione di collegamento. Quando gli strumenti di condivisione e-mail, condivisione di incorporamento o condivisione di collegamenti sono attivati, il visualizzatore visualizza una finestra di dialogo modale con il modulo di immissione dati corrispondente. Quando si chiama Facebook o Twitter, il visualizzatore reindirizza l&#39;utente a una finestra di dialogo di condivisione standard da un servizio di social media. Inoltre, quando uno strumento di condivisione è attivato, la riproduzione video viene sospesa automaticamente.

Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di sicurezza del browser Web.

## Incorporazione del visualizzatore video {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, se selezionato, apre il visualizzatore in una finestra del browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare una progettazione reattiva che viene visualizzata in modo diverso su dispositivi diversi o per dimensioni diverse della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità operative principali: popup, incorporamento di dimensioni fisse e incorporamento di progetti reattivi.

È possibile incorporare più video sulla stessa pagina su tablet e dispositivi mobili. Di solito è possibile riprodurre un solo video alla volta. Quando un utente avvia la riproduzione di un video e tenta di riprodurne un altro, il primo video viene messo automaticamente in pausa. Il video messo in pausa automatica ricorda il tempo di riproduzione corrente, in modo che l’utente possa sempre recuperarlo e riprendere la riproduzione. L&#39;unica eccezione a questa regola è nel browser Chrome su dispositivi Android™ 4.x, che può riprodurre video in parallelo.

**Informazioni sulla modalità popup**

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda del browser Web separata. Occupa l’intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l’orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` Chiamata JavaScript configurata correttamente `A` HTML o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML preconfigurata per la modalità di funzionamento popup. Si chiama [!DNL VideoViewer.html] e si trova sotto il [!DNL html5/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/VideoViewer.html]

Puoi ottenere una personalizzazione visiva applicando CSS personalizzata.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/VideoViewer.html?asset=Scene7SharedAssets/Glacier_Climber_MP4" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento reattivo**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe già avere alcuni contenuti per i clienti non correlati al visualizzatore. Il visualizzatore occupa normalmente solo una parte del patrimonio immobiliare della pagina web.

I casi d’uso principali sono le pagine web orientate per desktop o dispositivi tablet e le pagine di progettazione reattive che regolano automaticamente il layout a seconda del tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando le dimensioni del visualizzatore non vengono modificate dopo il caricamento iniziale. Questa è la scelta migliore per le pagine web con un layout di pagina statico.

L’incorporamento reattivo della progettazione presuppone che il visualizzatore debba ridimensionarsi in fase di esecuzione in risposta alla modifica delle dimensioni del suo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta del visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

Nella modalità di incorporamento di un design reattivo, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il suo contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando libera la sua altezza, lo spettatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questo metodo assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura sui lati. Questo caso d’uso è il più comune per le pagine web che utilizzano un framework di layout di progettazione reattivo come Bootstrap o Foundation.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore riempie solo tale area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporamento a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuare le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL FlyoutViewer.js]. Il [!DNL FlyoutViewer.js] il file si trova sotto [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene fornito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/VideoViewer.js"></script>
```

>[!NOTE]
>
>Fai riferimento solo al visualizzatore principale JavaScript `include` sulla pagina. Non fare riferimento ad altri file JavaScript nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente all’SDK di HTML 5 `Utils.js` libreria caricata dal visualizzatore da `/s7viewers` percorso di contesto (il cosiddetto SDK consolidato) `include`). Il motivo è che l&#39;ubicazione di `Utils.js` o librerie di visualizzatori runtime simili sono completamente gestite dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. L’Adobe non mantiene le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del DIV del contenitore.

   Aggiungi un elemento DIV vuoto alla pagina in cui vuoi che venga visualizzato il visualizzatore. L’ID dell’elemento DIV deve essere definito perché questo ID viene passato successivamente all’API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il segnaposto DIV è un elemento posizionato, il che significa che `position` Proprietà CSS impostata su `relative` o `absolute`.

   Verificare che la funzione a schermo intero funzioni correttamente in Internet Explorer. Verifica che nel DOM non siano presenti altri elementi con un ordine di sovrapposizione più elevato rispetto al DIV segnaposto.

   Di seguito è riportato un esempio di un elemento DIV segnaposto definito:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica del visualizzatore dichiarandolo per `.s7videoviewer` classe CSS di primo livello in unità assolute oppure utilizzando il modificatore `stagesize`.

   È possibile inserire il formato CSS direttamente nella pagina HTML o in un file CSS visualizzatore personalizzato. Viene successivamente assegnato a un record di predefiniti visualizzatore in Dynamic Media Classic o passato esplicitamente utilizzando un comando di stile.

   Consulta [Personalizzazione del visualizzatore video](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) per ulteriori informazioni sullo stile del visualizzatore tramite CSS.

   Di seguito è riportato un esempio di definizione di una dimensione di visualizzatore statico in una pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   È possibile impostare `stagesize` modificatore nel record del predefinito visualizzatore in Dynamic Media Classic oppure trasmettilo esplicitamente con il codice di inizializzazione visualizzatore con `params` raccolta. Oppure, come chiamata API descritta nella sezione Riferimento comando, come indicato di seguito:

   ```html {.line-numbers}
   videoViewer.setParam("stagesize", "640,480");
   ```

   Si consiglia un approccio basato su CSS, che viene utilizzato in questo esempio.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, puoi creare un’istanza di `s7viewers.VideoViewer` classe, passa tutte le informazioni di configurazione al relativo costruttore e chiama `init()` su un&#39;istanza del visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto deve avere almeno `containerId` campo contenente il nome dell’ID contenitore del visualizzatore e nidificato `params` Oggetto JSON con parametri di configurazione supportati dal visualizzatore. In questo caso, `params` l&#39;oggetto deve avere almeno l&#39;URL Image Server passato come `serverUrl` proprietà, URL del server video passato come `videoserverurl` e la risorsa iniziale come `asset` parametro. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il `init()` metodo immediatamente prima della chiusura `BODY` o sul corpo `onload()` evento.

   Allo stesso tempo, l’elemento contenitore non deve ancora necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza del visualizzatore, trasferimento al costruttore delle opzioni di configurazione minime necessarie e chiamata di `init()` metodo. Questo esempio presuppone `videoViewer` è l’istanza del visualizzatore, `s7viewer` è il nome del segnaposto `DIV`, [!DNL http://s7d1.scene7.com/is/image/] è l’URL Image Server, [!DNL http://s7d1.scene7.com/is/content/] è l’URL del server video e [!DNL Scene7SharedAssets/Glacier_Climber_MP4] è la risorsa.

   ```html {.line-numbers}
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

   Il codice che segue è un esempio completo di una pagina web banale che incorpora il Visualizzatore video con una dimensione fissa:

   ```html {.line-numbers}
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

**Design reattivo con altezza illimitata**

Con l’incorporamento di un design reattivo, la pagina web solitamente dispone di un layout flessibile che determina le dimensioni in fase di esecuzione del contenitore del visualizzatore `DIV`. Ai fini di questo esempio, si supponga che la pagina web consenta il contenitore del visualizzatore `DIV` per occupare il 40% delle dimensioni della finestra del browser web, senza limitazioni di altezza. Il codice HTML della pagina Web sarà simile al seguente:

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

L’aggiunta del visualizzatore a una pagina di questo tipo è simile all’incorporamento di dimensioni fisse; l’unica differenza è che non è necessario definire esplicitamente le dimensioni del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del DIV del contenitore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell’incorporamento di dimensioni fisse. Aggiungi contenitore `DIV` al &quot;titolare&quot; esistente `DIV`. Il codice seguente è un esempio completo. Puoi vedere come cambiano le dimensioni del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```html {.line-numbers}
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

La pagina di esempi seguente illustra un utilizzo più reale del design responsive con altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Percorso demo alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Incorporamento design reattivo con larghezza e altezza definite**

Se è presente un design reattivo che incorpora con larghezza e altezza definite, lo stile della pagina web è diverso; fornisce entrambe le dimensioni al &quot; titolare&quot; `DIV` e centralo nella finestra del browser. Inoltre, la pagina web imposta le dimensioni del `HTML` e `BODY` al 100%:

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

I passaggi di incorporamento rimanenti sono identici all’incorporamento reattivo con altezza illimitata. L’esempio risultante è il seguente:

```html {.line-numbers}
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

**Incorporazione tramite API basata su Set**

Invece di utilizzare l’inizializzazione basata su JSON, puoi utilizzare l’API basata su setter e il costruttore no-args. Con tale API, il costruttore non accetta parametri e i parametri di configurazione vengono specificati utilizzando `setContainerId()`, `setParam()`, e `setAsset()` Metodi API con chiamate JavaScript separate.

L’esempio seguente illustra l’incorporamento a dimensione fissa con API basate su setter:

```html {.line-numbers}
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
