---
title: Visualizzatore video ritaglio avanzato
description: Il visualizzatore video con ritaglio avanzato riproduce video in streaming e progressivi codificati nel formato H.264 con l’aggiunta del supporto per il ritaglio avanzato. Viene fornito da Dynamic Media Classic o Adobe Experience Manager con Dynamic Media.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 937be8a2-307e-47bb-9fc8-d354f780a214
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '2364'
ht-degree: 0%

---

# Ritaglio video automatico{#smart-crop-video}

Il visualizzatore video con ritaglio avanzato riproduce video in streaming e progressivi codificati nel formato H.264 con l’aggiunta del supporto per il ritaglio avanzato. Viene fornito da Dynamic Media Classic o Experience Manager con Dynamic Media.

Consulta [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Sono supportati sia set per video singolo che set per video adattivi. Inoltre, il visualizzatore supporta l’utilizzo di video progressivi e flussi HLS in hosting su posizioni esterne. È progettato per funzionare su browser Web desktop e mobili che supportano video HTML5. Questo visualizzatore supporta anche sottotitoli codificati facoltativi visualizzati sopra al contenuto video, alla navigazione dei capitoli video e agli strumenti di condivisione dei social media.

Il Visualizzatore video ritaglio avanzato utilizza la riproduzione video in streaming di HTML5 in formato HLS nella sua configurazione predefinita ogni volta che il sistema sottostante lo supporta. Sui sistemi che non supportano lo streaming su HTML5, il visualizzatore torna alla distribuzione di video progressivi HTML5.

Visualizzatore di tipo 518.


## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)


## Utilizzo del visualizzatore ritaglio video automatico {#section-f21ac23d3f6449ad9765588d69584772}

Il Visualizzatore video ritaglio avanzato rappresenta un file JavaScript principale e un set di file di supporto, un singolo JavaScript da includere con tutti i componenti del Visualizzatore SDK utilizzati da questo particolare visualizzatore, le risorse e i file CSS scaricati dal visualizzatore in fase di esecuzione.

È possibile utilizzare il Visualizzatore video ritaglio avanzato in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con i visualizzatori IS. In alternativa, puoi utilizzare il visualizzatore in modalità incorporata, dove viene integrato in una pagina web di destinazione utilizzando l’API documentata.

L’operazione di configurazione e interpolazione del visualizzatore è simile a quella di altri visualizzatori. Tutte le operazioni di skin vengono eseguite tramite CSS personalizzato.

Vedi [Riferimento al comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento al comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore video Ritaglio avanzato {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il Visualizzatore video ritaglio avanzato fornisce un set di controlli standard dell’interfaccia utente per la riproduzione di video, ad esempio:

* Pulsante Riproduci/Pausa.
* Bolla temporale del video di scorrimento video.
* Indicatore tempo di riproduzione/tempo totale.
* Controllo del volume.
* pulsante a schermo intero.
* Attiva/disattiva sottotitoli codificati.

Tutti questi controlli sono raggruppati in una barra di controllo nella parte inferiore dell&#39;interfaccia utente del visualizzatore.

Sui dispositivi touch, il controllo del volume è nascosto dall&#39;interfaccia utente, perché è possibile controllare il volume solo utilizzando i pulsanti hardware.

Quando il visualizzatore funziona in modalità pop-up, il pulsante a schermo intero non è disponibile nell’interfaccia utente.

È possibile navigare rapidamente nel contenuto di un video quando il capitolo video è attivato. I capitoli video vengono visualizzati come marcatori nella traccia di scorrimento video e mostrano il titolo del capitolo e la descrizione associata al passaggio del mouse o con un solo tocco sui sistemi touch. Gli utenti possono cercare un capitolo particolare selezionando un marcatore di capitolo o selezionando la bolla di descrizione del capitolo.

Il visualizzatore supporta sia l&#39;input tocco che l&#39;input del mouse su dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Consulta [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Strumenti per la condivisione di social media con il visualizzatore video Ritaglio avanzato {#section-907d316fe1da4b87abb9775f02464704}

Il Visualizzatore video ritaglio avanzato supporta gli strumenti di condivisione dei social media. Sono disponibili come pulsante singolo nell’interfaccia utente, che si espande in una barra degli strumenti di condivisione quando l’utente fa clic o tocca su di essa.

La barra degli strumenti Condivisione contiene un’icona per ogni tipo di canale di condivisione supportato, ad esempio Facebook, Twitter, condivisione e-mail, condivisione di codice da incorporare e condivisione di collegamento. Quando gli strumenti di condivisione e-mail, condivisione di incorporamento o condivisione di collegamenti sono attivati, il visualizzatore visualizza una finestra di dialogo modale con il modulo di immissione dati corrispondente. Quando si chiama Facebook o Twitter, il visualizzatore reindirizza l&#39;utente a una finestra di dialogo di condivisione standard da un servizio di social media. Inoltre, quando uno strumento di condivisione è attivato, la riproduzione video viene sospesa automaticamente.

Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di sicurezza del browser Web.

## Incorporazione di un visualizzatore video con ritaglio avanzato {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, se selezionato, apre il visualizzatore in una finestra del browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare una progettazione reattiva che viene visualizzata in modo diverso su dispositivi diversi o per dimensioni diverse della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità operative principali: popup, incorporamento di dimensioni fisse e incorporamento di progetti reattivi.

È possibile incorporare più video sulla stessa pagina su tablet e dispositivi mobili. Di solito è possibile riprodurre un solo video alla volta. Quando un utente avvia la riproduzione di un video e tenta di riprodurne un altro, il primo video viene messo automaticamente in pausa. Il video messo in pausa automatica ricorda il tempo di riproduzione corrente, in modo che l’utente possa sempre recuperarlo e riprendere la riproduzione. L&#39;unica eccezione a questa regola è nel browser Chrome su dispositivi Android™ 4.x, che possono riprodurre video in parallelo.

**Informazioni sulla modalità popup**

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda del browser Web separata. Occupa l’intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l’orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando `window.open()` chiamata JavaScript, `A` elemento HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML preconfigurata per la modalità di funzionamento popup. Si chiama [!DNL SmartCropVideoViewer.html] e si trova nella sottocartella [!DNL html5/] della distribuzione IS-Viewers standard:

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

Puoi ottenere una personalizzazione visiva applicando CSS personalizzata.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento reattivo**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe già avere alcuni contenuti per i clienti non correlati al visualizzatore. Il visualizzatore occupa normalmente solo una parte del patrimonio immobiliare della pagina web.

I casi d’uso principali sono le pagine web orientate per desktop o dispositivi tablet e le pagine di progettazione reattive che regolano automaticamente il layout a seconda del tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando le dimensioni del visualizzatore non vengono modificate dopo il caricamento iniziale. Questa è la scelta migliore per le pagine web con un layout di pagina statico.

L&#39;incorporamento reattivo della progettazione presuppone che il visualizzatore debba essere ridimensionato in fase di esecuzione in risposta alla modifica delle dimensioni del relativo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta del visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

In modalità di incorporamento di progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina Web ridimensiona il contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`, lasciando libera la sua altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questo metodo assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura sui lati. Questo caso d’uso è il più comune per le pagine web che utilizzano un framework di layout di progettazione reattivo come Bootstrap o Foundation.

In caso contrario, se la pagina Web imposta sia la larghezza che l&#39;altezza per il contenitore del visualizzatore `DIV`, il visualizzatore occupa solo tale area e segue le dimensioni fornite dal layout della pagina Web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuare le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l&#39;API del visualizzatore, assicurati di includere [!DNL SmartCropVideoViewer.js]. Il file [!DNL SmartCropVideoViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene fornito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
```

>[!NOTE]
>
>Fare riferimento solo al file JavaScript `include` del visualizzatore principale nella pagina. Non fare riferimento ad altri file JavaScript nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente alla libreria `Utils.js` di HTML5 SDK caricata dal visualizzatore dal percorso di contesto `/s7viewers` (cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o di librerie di visualizzatori di runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non mantiene sul server le versioni precedenti del visualizzatore secondario `includes`.
>
>
>Di conseguenza, il posizionamento di un riferimento diretto a qualsiasi JavaScript `include` secondario utilizzato dal visualizzatore nella pagina interrompe la funzionalità del visualizzatore in futuro, quando viene distribuita una nuova versione del prodotto.

1. Definizione del DIV del contenitore.

   Aggiungi un elemento DIV vuoto alla pagina in cui vuoi che venga visualizzato il visualizzatore. L’ID dell’elemento DIV deve essere definito perché questo ID viene passato successivamente all’API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il DIV segnaposto è un elemento posizionato, il che significa che la proprietà CSS `position` è impostata su `relative` o `absolute`.

   Verificare che la funzione a schermo intero funzioni correttamente in Internet Explorer. Verifica che nel DOM non siano presenti altri elementi con un ordine di sovrapposizione più elevato rispetto al DIV segnaposto.

   Di seguito è riportato un esempio di un elemento DIV segnaposto definito:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica per il visualizzatore dichiarandolo per la classe CSS di primo livello `.s7videoviewer` in unità assolute oppure utilizzando il modificatore `stagesize`.

   È possibile inserire il formato CSS direttamente nella pagina HTML o in un file CSS visualizzatore personalizzato. Viene successivamente assegnato a un record di predefiniti visualizzatore in Dynamic Media Classic o passato esplicitamente utilizzando un comando di stile.

   Per ulteriori informazioni sullo stile del visualizzatore tramite CSS, vedere [Personalizzazione del visualizzatore video con ritaglio avanzato](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e).

   Di seguito è riportato un esempio di definizione di una dimensione di visualizzatore statico in una pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   È possibile impostare il modificatore `stagesize` nel record del predefinito visualizzatore in Dynamic Media Classic oppure trasmetterlo in modo esplicito con il codice di inizializzazione del visualizzatore con la raccolta `params`. Oppure, come chiamata API descritta nella sezione Riferimento comando, come indicato di seguito:

   ```html {.line-numbers}
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   Si consiglia un approccio basato su CSS, che viene utilizzato in questo esempio.

1. Creazione e inizializzazione del visualizzatore.

   Dopo aver completato i passaggi precedenti, si crea un&#39;istanza della classe `s7viewers.SmartCropVideoViewer`, si passano tutte le informazioni di configurazione al relativo costruttore e si chiama il metodo `init()` su un&#39;istanza del visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto deve avere almeno il campo `containerId` che contiene il nome dell&#39;ID contenitore del visualizzatore e l&#39;oggetto JSON `params` nidificato con i parametri di configurazione supportati dal visualizzatore. In questo caso, l&#39;oggetto `params` deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl`, l&#39;URL del server video passato come proprietà `videoserverurl` e la risorsa iniziale come parametro `asset`. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sul corpo dell&#39;evento `onload()`.

   Allo stesso tempo, l’elemento contenitore non deve ancora necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza del visualizzatore, passaggio al costruttore delle opzioni di configurazione minime necessarie e chiamata del metodo `init()`. In questo esempio si presuppone che `smartCropVideoViewer` sia l&#39;istanza del visualizzatore, `s7viewer` il nome del segnaposto `DIV`, [!DNL http://s7d1.scene7.com/is/image/] l&#39;URL di Image Server, [!DNL http://s7d1.scene7.com/is/content/] l&#39;URL del server video e [!DNL html5automation/frisbee-AVS] la risorsa.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   ```

   Il codice che segue è un esempio completo di una pagina web banale che incorpora il visualizzatore video Ritaglio avanzato con una dimensione fissa:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
   var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"html5automation/frisbee-AVS", 
    "serverurl":"http://s7d1.scene7.com/is/image/", 
    "videoserverurl":"http://s7d1.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Incorporamento di progettazione reattiva con altezza illimitata**

Con la progettazione reattiva incorporata, la pagina web in genere ha un layout flessibile che determina la dimensione in fase di esecuzione del contenitore del visualizzatore `DIV`. Ai fini di questo esempio, si supponga che la pagina Web consenta al contenitore del visualizzatore `DIV` di occupare il 40% delle dimensioni della finestra del browser Web, senza limitazioni di altezza. Il codice HTML della pagina Web sarà simile al seguente:

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

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del DIV del contenitore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell’incorporamento di dimensioni fisse. Aggiungere il contenitore `DIV` al &quot; titolare&quot; esistente `DIV`. Il codice seguente è un esempio completo. Puoi vedere come cambiano le dimensioni del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
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

<!--

[Alternate demo location](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=it)

-->

**Incorporamento di progettazione reattiva con larghezza e altezza definite**

Se è presente una progettazione reattiva che incorpora con larghezza e altezza definite, lo stile della pagina Web è diverso. Fornisce entrambe le dimensioni al &quot; titolare&quot; `DIV` e centralo nella finestra del browser. La pagina Web imposta inoltre le dimensioni dell&#39;elemento `HTML` e dell&#39;elemento `BODY` al 100%:

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"html5automation/frisbee-AVS", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Incorporamento tramite API basata su Set**

Invece di utilizzare l’inizializzazione basata su JSON, puoi utilizzare l’API basata su setter e il costruttore no-args. Con tale API, il costruttore non accetta parametri e i parametri di configurazione sono specificati utilizzando i metodi API `setContainerId()`, `setParam()` e `setAsset()` con chiamate JavaScript separate.

L’esempio seguente illustra l’incorporamento a dimensione fissa con API basate su setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SmartCropVideoViewer.js"></script> 
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
var smartCropVideoViewer = new s7viewers.SmartCropVideoViewer(); 
smartCropVideoViewer.setContainerId("s7viewer"); 
smartCropVideoViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
smartCropVideoViewer.setParam("videoserverurl", "http://s7d1.scene7.com/is/content/"); 
smartCropVideoViewer.setAsset("html5automation/frisbee-AVS"); 
smartCropVideoViewer.init(); 
</script> 
</body> 
</html> 
```
