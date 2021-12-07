---
title: Visualizzatore video di ritaglio avanzato
description: Smart Crop Video Viewer è un lettore video che riproduce video in streaming e progressivi codificati nel formato H.264 con l’aggiunta del supporto Smart Crop. Viene fornito da Dynamic Media Classic o Adobe Experience Manager con Dynamic Media.
keywords: reattivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
source-git-commit: 2dc7b92da6c73a328a82c50dc5a052a3351ee2dc
workflow-type: tm+mt
source-wordcount: '2413'
ht-degree: 0%

---

# Video di ritaglio avanzato{#smart-crop-video}

Smart Crop Video Viewer è un lettore video che riproduce video in streaming e progressivi codificati nel formato H.264 con l’aggiunta del supporto Smart Crop. Viene fornito da Dynamic Media Classic o Experience Manager con Dynamic Media.

Vedi [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Sono supportati sia i set video singoli che quelli adattivi. Inoltre, il visualizzatore supporta l’utilizzo di video progressivi e flussi HLS ospitati su posizioni esterne. È progettato per funzionare sia sui browser Web desktop che mobili che supportano video HTML5. Questo visualizzatore supporta anche i sottotitoli codificati opzionali visualizzati sopra i contenuti video, la navigazione nei capitoli video e gli strumenti di condivisione dei social media.

Il visualizzatore video Smart Crop utilizza la riproduzione video in streaming HTML5 in formato HLS nella configurazione predefinita ogni volta che il sistema sottostante lo supporta. Nei sistemi che non supportano lo streaming HTML5, il visualizzatore torna alla distribuzione progressiva dei video HTML5.

Tipo di visualizzatore 518.

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS](https://s7d9.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS)

## Utilizzo di Smart Crop Video Viewer {#section-f21ac23d3f6449ad9765588d69584772}

Smart Crop Video Viewer rappresenta un file JavaScript principale e un set di file helper, un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS scaricati dal visualizzatore in fase di esecuzione.

È possibile utilizzare il Visualizzatore video di ritaglio avanzato in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con IS-Viewers. In alternativa, puoi utilizzare il visualizzatore in modalità incorporata, dove viene integrato in una pagina web di destinazione utilizzando l’API documentata.

L’attività di configurazione e skin del visualizzatore è simile a quella di altri visualizzatori. Tutta la skin viene ottenuta tramite CSS personalizzati.

Vedi [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore video di ritaglio avanzato {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore video Smart Crop fornisce una serie di controlli standard dell’interfaccia utente per la riproduzione video, ad esempio:

* Pulsante Riproduci/Pausa.
* Bolla temporale video di scorrimento video.
* Indicatore tempo/tempo totale riprodotto.
* Controllo del volume.
* Pulsante Schermo intero.
* Icona della didascalia chiusa.

Tutti questi controlli sono raggruppati in una barra di controllo nella parte inferiore dell’interfaccia utente del visualizzatore.

Sui dispositivi touch, il controllo del volume è nascosto dall&#39;interfaccia utente, perché è possibile controllare il volume solo utilizzando i pulsanti hardware.

Quando il visualizzatore funziona in modalità pop-up, il pulsante a schermo intero non è disponibile nell’interfaccia utente.

È possibile navigare rapidamente nel contenuto di un video quando viene attivato un capitolo video. I capitoli video vengono visualizzati come marcatori nella traccia di scorrimento video e mostrano il titolo del capitolo e la relativa descrizione su un rollover del mouse o con un singolo tocco sui sistemi touch. Gli utenti possono cercare un capitolo specifico selezionando un marcatore di capitolo o selezionando la bolla di descrizione del capitolo.

Il visualizzatore supporta sia l’input touch che l’input del mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Vedi [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Strumenti di condivisione social media con Smart Crop Video Viewer {#section-907d316fe1da4b87abb9775f02464704}

Il visualizzatore video Smart Crop supporta gli strumenti di condivisione dei social media. Sono disponibili come un singolo pulsante nell’interfaccia utente che si espande in una barra degli strumenti di condivisione quando l’utente vi fa clic o vi tocca.

La barra degli strumenti di condivisione contiene un&#39;icona per ogni tipo di canale di condivisione supportato come Facebook, Twitter, condivisione di e-mail, condivisione di codice da incorporare e condivisione di collegamenti. Quando si attivano gli strumenti di condivisione e-mail, incorporamento o collegamento, il visualizzatore visualizza una finestra di dialogo modale con un modulo di immissione dati corrispondente. Quando si chiamano Facebook o Twitter, il visualizzatore reindirizzerà l&#39;utente a una finestra di dialogo di condivisione standard da un servizio di social media. Anche quando uno strumento di condivisione viene attivato, la riproduzione video viene messa in pausa automaticamente.

Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di sicurezza del browser Web.

## Incorporazione di un visualizzatore video di ritaglio avanzato {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, quando selezionato, apre il visualizzatore in una finestra separata del browser. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare un design reattivo che viene visualizzato in modo diverso su diversi dispositivi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: a comparsa, incorporazione a dimensione fissa e incorporazione responsive della progettazione.

L’incorporazione di più video sulla stessa pagina è supportata sui tablet e sui dispositivi mobili. Di solito, è possibile riprodurre un solo video alla volta. Quando un utente inizia a riprodurre un video e poi prova a riprodurre un altro video, il primo video viene messo in pausa automaticamente. Il video messo in pausa automaticamente ricorda il tempo di riproduzione corrente, in modo che l&#39;utente possa sempre tornare ad esso e riprendere la riproduzione. L&#39;unica eccezione questa regola è nel browser Chrome su dispositivi Android™ 4.x, che può riprodurre video in parallelo.

**Informazioni sulla modalità a comparsa**

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda separata del browser Web. Prende l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l&#39;orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` Chiamata JavaScript configurata correttamente `A` Elemento HTML o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML predefinita per la modalità di funzionamento a comparsa. Si chiama [!DNL SmartCropVideoViewer.html] e si trova sotto la [!DNL html5/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/SmartCropVideoViewer.html]

Puoi ottenere la personalizzazione visiva applicando CSS personalizzati.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/SmartCropVideoViewer.html?asset=html5automation/frisbee-AVS" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento reattiva**

Nella modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe avere già alcuni contenuti del cliente non correlati al visualizzatore. Normalmente lo spettatore occupa solo una parte del patrimonio immobiliare della pagina web.

I casi d’uso principali sono le pagine web orientate ai desktop o ai dispositivi tablet, nonché le pagine di progettazione reattiva che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporazione a dimensione fissa viene utilizzata quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questa opzione è la migliore per le pagine web con layout di pagina statico.

L’incorporazione di design reattivo presuppone che il visualizzatore debba ridimensionare in fase di esecuzione in risposta alla modifica delle dimensioni del suo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta del visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

Nella modalità di incorporamento della progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questo metodo assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura laterale. Questo caso d’uso è il più comune per le pagine web che utilizzano un framework di layout dinamico come Bootstrap o Foundation.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza del contenitore del visualizzatore `DIV`, il visualizzatore riempie solo quell’area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio è quello di incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina web, effettua le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione di HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL SmartCropVideoViewer.js]. La [!DNL SmartCropVideoViewer.js] si trova sotto [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/SmartCropVideoViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene servito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SmartCropVideoViewer.js"></script>
```

>[!NOTE]
>
>Fai riferimento solo al visualizzatore principale JavaScript `include` nella pagina. Non fare riferimento a file JavaScript aggiuntivi nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente all’SDK di HTML5 `Utils.js` libreria caricata dal visualizzatore da `/s7viewers` percorso contestuale (cosiddetto SDK consolidato) `include`). Il motivo è che la posizione di `Utils.js` Per librerie di visualizzatori runtime simili, sono gestite completamente dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, è possibile inserire un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe le funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore DIV.

   Aggiungi un elemento DIV vuoto alla pagina in cui desideri che appaia il visualizzatore. L’ID dell’elemento DIV deve essere definito perché viene passato successivamente all’API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il segnaposto DIV è un elemento posizionato, il che significa che il `position` La proprietà CSS è impostata su `relative` o `absolute`.

   Assicurati che la funzione a schermo intero funzioni correttamente in Internet Explorer. Controlla che non ci siano altri elementi nel DOM con un ordine di impilamento più alto del tuo segnaposto DIV.

   Di seguito è riportato un esempio di elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore

   Puoi impostare la dimensione statica del visualizzatore dichiarandola per `.s7videoviewer` classe CSS di primo livello in unità assolute o utilizzando il modificatore `stagesize`.

   Puoi mettere le dimensioni in CSS direttamente nella pagina HTML o in un file CSS del visualizzatore personalizzato. In seguito viene assegnato a un record predefinito visualizzatore in Dynamic Media Classic o passato esplicitamente utilizzando un comando stile.

   Vedi [Personalizzazione del visualizzatore video di ritaglio avanzato](../../c-html5-s7-aem-asset-viewers/c-html5-video-reference/c-html5-video-viewer-20-customizingviewer/c-html5-video-viewer-20-customizingviewer.md#concept-072a52b10b5f4c0789393dc6e2134c0e) per ulteriori informazioni sullo stile del visualizzatore tramite CSS.

   Di seguito è riportato un esempio di definizione delle dimensioni di un visualizzatore statico in una pagina di HTML:

   ```
   #s7viewer.s7videoviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   È possibile impostare `stagesize` modificatore nel record predefinito visualizzatore in Dynamic Media Classic, oppure trasmettilo esplicitamente con il codice di inizializzazione del visualizzatore con `params` raccolta. Oppure, come chiamata API come descritto nella sezione Riferimento comando , come segue:

   ```
   smartCropVideoViewer.setParam("stagesize", "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza di `s7viewers.SmartCropVideoViewer` passare tutte le informazioni di configurazione al relativo costruttore e chiamare `init()` su un’istanza di visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Almeno questo oggetto deve avere `containerId` campo che contiene il nome dell’ID contenitore visualizzatore e nidificato `params` Oggetto JSON con parametri di configurazione supportati dal visualizzatore. In questo caso, `params` L&#39;oggetto deve avere almeno l&#39;URL Image Server passato come `serverUrl` proprietà, URL del server video passato come `videoserverurl` e la risorsa iniziale come `asset` parametro . L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il `init()` metodo immediatamente prima della chiusura `BODY` o sul corpo `onload()` evento.

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del `init()` metodo . Questo esempio presuppone `smartCropVideoViewer` è l’istanza del visualizzatore, `s7viewer` è il nome del segnaposto `DIV`, [!DNL http://s7d1.scene7.com/is/image/] è l’URL di Image Server, [!DNL http://s7d1.scene7.com/is/content/] è l’URL del server video, e [!DNL html5automation/frisbee-AVS] è la risorsa.

   ```
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

   Il codice seguente è un esempio completo di una pagina web banale che incorpora il Visualizzatore video di ritaglio avanzato con dimensioni fisse:

   ```
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

**Incorporazione di design reattivo con altezza illimitata**

Con l’incorporazione del design reattivo, la pagina web dispone normalmente di un layout flessibile che determina la dimensione in fase di esecuzione del contenitore del visualizzatore `DIV`. Ai fini di questo esempio, si supponga che la pagina web consenta il contenitore del visualizzatore `DIV` per prendere il 40% delle dimensioni della finestra del browser web, lasciando la sua altezza senza restrizioni. Il codice HTML della pagina web sarà simile al seguente:

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

L’aggiunta del visualizzatore a una pagina di questo tipo è simile all’incorporazione con dimensioni fisse; l’unica differenza è che non è necessario definire esplicitamente la dimensione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell&#39;incorporazione con dimensione fissa. Aggiungi contenitore `DIV` al &quot;titolare&quot; esistente `DIV`. Il codice seguente è un esempio completo. Puoi vedere come cambia la dimensione del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```
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

La pagina degli esempi seguenti illustra l’utilizzo più reale di elementi di design reattivi con altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Posizione demo alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Incorporazione responsive con larghezza e altezza definite**

Se è presente un incorporamento dinamico con larghezza e altezza definite, lo stile della pagina web è diverso; fornisce entrambe le dimensioni al &quot;titolare&quot; `DIV` e centralo nella finestra del browser. Inoltre, la pagina web imposta le dimensioni del `HTML` e `BODY` al 100%:

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

**Incorporazione tramite API basate su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. Con tale API, il costruttore non accetta alcun parametro e i parametri di configurazione vengono specificati utilizzando `setContainerId()`, `setParam()`e `setAsset()` Metodi API con chiamate JavaScript separate.

L’esempio seguente illustra l’incorporazione di dimensioni fisse con API basata su setter:

```
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
