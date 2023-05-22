---
title: Video360
description: Il visualizzatore HTML5 Video360 è un lettore video a 360 gradi che riproduce in streaming e video progressivo a 360 codificato nel formato H.264, fornito da Dynamic Media Classic o da Adobe Experience Manager, Dynamic Media.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,360 VR Video
role: Developer,User
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2569'
ht-degree: 0%

---

# Video360{#video}

Il visualizzatore HTML5 Video360 è un lettore video a 360 gradi che riproduce in streaming e video progressivo a 360 codificato nel formato H.264, fornito da Dynamic Media Classic o da Adobe Experience Manager, Dynamic Media.

I video a 360 gradi, noti anche come video immersivi o video sferici, sono registrazioni video in cui una visione in ogni direzione viene registrata contemporaneamente, girata utilizzando una fotocamera omnidirezionale o una raccolta di telecamere. Sono supportati sia set per video singolo che set per video adattivi. Il visualizzatore supporta anche l’utilizzo di video progressivi e flussi HLS in hosting su posizioni esterne.

Le proporzioni consigliate per i video 360 sono 2:1. Audio spaziale non supportato. Il visualizzatore è progettato per funzionare solo con video 360; un tentativo di riprodurre un video non 360 genera una riproduzione video distorta.

Il visualizzatore è progettato per funzionare sia su browser Web desktop che mobili che supportano video HTML5. Il visualizzatore supporta strumenti opzionali per la condivisione tramite social network.

Il Visualizzatore video360 utilizza la riproduzione video in streaming HTML5 in formato HLS nella sua configurazione predefinita ogni volta che il sistema sottostante lo supporta. Sui sistemi che non supportano lo streaming HTML5, il visualizzatore torna alla distribuzione di video progressivi HTML5.

Il tipo di visualizzatore è 517.

## URL demo {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Requisiti di sistema {#section-b7270cc4290043399681dc504f043609}

Consulta [Requisiti di sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilizzo di Video360 Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

HTML5 Video360 Viewer rappresenta un file JavaScript principale e un set di file di supporto (un singolo file JavaScript da includere con tutti i componenti SDK HTML5 Viewer utilizzati da questo visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

HTML5 Video360 Viewer può essere utilizzato sia in modalità popup utilizzando una pagina HTML pronta per la produzione fornita con IS-Viewers che in modalità incorporata, dove viene integrato nella pagina web di destinazione utilizzando l’API documentata.

La configurazione e lo skin sono simili a quelli degli altri visualizzatori descritti in questa guida. Tutte le operazioni di skin vengono eseguite tramite CSS (Cascading Style Sheets) personalizzati.

Consulta [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comando comune a tutti i visualizzatori - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Il contenuto video 360 richiede impostazioni di codifica più elevate rispetto al video standard non 360. In altre parole, per ottenere la stessa qualità percepibile, il contenuto 360 deve avere una risoluzione più alta rispetto al video non 360. Si consiglia di prendere in considerazione le seguenti impostazioni del predefinito per video adattivo per video 360:

* 720p, 2500 kbps
* 1080p, 5000 kbps
* 1440p, 6600 kbps

Tuttavia, è importante notare che per trasmettere un video codificato con tali impostazioni di alta qualità è necessaria una connessione a banda larga sul dispositivo di un utente finale.

## Interazione con il visualizzatore Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il visualizzatore HTML5 Video360 fornisce un set di controlli standard dell’interfaccia utente per la riproduzione video, come il pulsante di riproduzione/pausa, la bolla temporale del video di scorrimento, l’indicatore del tempo totale/tempo di riproduzione, il controllo del volume e il pulsante a schermo intero. Tutti questi controlli sono raggruppati in una barra di controllo nella parte inferiore dell’interfaccia utente del visualizzatore.

Sui dispositivi touch, il controllo del volume è nascosto dall&#39;interfaccia utente, perché è possibile controllare il volume solo utilizzando i pulsanti hardware del dispositivo.

Quando il visualizzatore funziona in modalità pop-up, nell’interfaccia utente non è disponibile un pulsante a schermo intero.

Il visualizzatore supporta anche vari strumenti di condivisione dei social media. Sono disponibili come pulsante singolo nell’interfaccia utente, che si espande in una barra degli strumenti di condivisione quando l’utente fa clic o tocca su di essa. La barra degli strumenti Condivisione contiene un’icona per ogni tipo di canale di condivisione supportato, ad esempio Facebook, Twitter, condivisione e-mail, condivisione di codice da incorporare e condivisione di collegamenti. Quando gli strumenti di condivisione e-mail, condivisione di incorporamento o condivisione di collegamenti sono attivati, il visualizzatore visualizza una finestra di dialogo modale con il modulo di immissione dati corrispondente. Quando si chiama Facebook o Twitter, il visualizzatore reindirizza l&#39;utente a una finestra di dialogo di condivisione standard da un servizio di social media. Inoltre, quando uno strumento di condivisione è attivato, la riproduzione video viene sospesa automaticamente. Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di sicurezza del browser Web.

Il visualizzatore supporta la riproduzione video 360 nei seguenti casi:

* Cuffie VR (come Oculus Go e Oculus Rift)
* Montaggi VR HMD (display montato sulla testa) (come Google Cardboard)
* Dispositivi non abilitati per VR (come browser desktop, tablet e telefoni cellulari non collegati ai supporti VR HMD)

Non è necessaria alcuna configurazione aggiuntiva per visualizzare il contenuto video 360 sulle cuffie VR. Il visualizzatore rileva automaticamente la presenza di cuffie VR e mostra il pulsante &quot;VR&quot; sopra il contenuto video. L’attivazione di questo pulsante &quot;VR&quot; attiva il rendering video in modalità VR. Il visualizzatore supporta il rendering VR solo nei browser che supportano WebVR.

Per utilizzare VR HMD monta il `Video360Player.vrrender` il modificatore deve essere impostato su `1` nella configurazione del visualizzatore, che forza il rendering stereoscopico.

Sulle cuffie VR e sui montaggi VR HMD, il cambiamento del punto di vista avviene in risposta al movimento delle cuffie, non è fornito un altro controllo della riproduzione in modalità VR.

Quando si guardano video 360 su dispositivi non dotati di VR, l&#39;utente finale può usare il mouse, il tocco o la tastiera per controllare la riproduzione video e il punto di vista.

Il visualizzatore supporta sia l’input tocco che quello del mouse su dispositivi Windows con touch screen e mouse, tuttavia questo supporto è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Il visualizzatore è completamente accessibile da tastiera. Consulta [Accessibilità della tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione di Video360 Viewer {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, se selezionato, apre il visualizzatore in una finestra del browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare una progettazione reattiva che viene visualizzata in modo diverso su dispositivi diversi o per dimensioni diverse della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità operative principali: popup, incorporamento di dimensioni fisse e incorporamento di progetti reattivi.

È possibile incorporare più video sulla stessa pagina su tablet e dispositivi mobili. Di solito è possibile riprodurre un solo video alla volta. Quando un utente avvia la riproduzione di un video e tenta di riprodurne un altro, il primo video viene messo automaticamente in pausa. Il video messo in pausa automatica ricorda il tempo di riproduzione corrente, in modo che l’utente possa sempre recuperarlo e riprendere la riproduzione. L&#39;unica eccezione a questa regola è nel browser Chrome su dispositivi Android™ 4.x, che può riprodurre video in parallelo.

**Informazioni sulla modalità popup**

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda del browser Web separata. Occupa l’intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l’orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` Chiamata JavaScript configurata correttamente `A` HTML o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML preconfigurata per la modalità di funzionamento popup. Si chiama [!DNL Video360Viewer.html] e si trova sotto il [!DNL html5/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Puoi ottenere una personalizzazione visiva applicando CSS personalizzata.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```html {.line-numbers}
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento a progettazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe già avere alcuni contenuti per i clienti non correlati al visualizzatore. Il visualizzatore occupa normalmente solo una parte del patrimonio immobiliare di una pagina web.

I casi d’uso principali sono le pagine web orientate per desktop o dispositivi tablet e le pagine progettate responsive che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questo metodo è la scelta migliore per le pagine web con un layout statico.

L’incorporamento reattivo della progettazione presuppone che il visualizzatore debba essere ridimensionato in fase di esecuzione in risposta alla modifica delle dimensioni del suo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

In modalità di incorporamento di un design reattivo, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il suo contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando libera la sua altezza, lo spettatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa funzionalità assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura sui lati. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout di progettazione web responsive come Bootstrap e Foundation.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore riempie solo tale area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporamento a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuare le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL Video360Viewer.js]. Il [!DNL Video360Viewer.js] il file si trova sotto [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene fornito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo è simile al seguente:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Fai riferimento solo al visualizzatore principale JavaScript `include` sulla pagina. Non fare riferimento ad altri file JavaScript nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente all’SDK di HTML 5 `Utils.js` libreria caricata dal visualizzatore da `/s7viewers` percorso di contesto (il cosiddetto SDK consolidato) `include`). Il motivo è che l&#39;ubicazione di `Utils.js` o librerie di visualizzatori runtime simili sono completamente gestite dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. L’Adobe non mantiene le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore `DIV`.

   Aggiungi un elemento vuoto `DIV` nella pagina in cui si desidera visualizzare il visualizzatore. Il `DIV` deve avere il proprio ID definito perché questo ID viene passato successivamente all&#39;API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Segnaposto `DIV` è un elemento posizionato, il che significa che `position` Proprietà CSS impostata su `relative` o `absolute`.

   Affinché la funzione a schermo intero funzioni correttamente in Internet Explorer, accertati che nel DOM non siano presenti altri elementi con un ordine di impilamento superiore rispetto al segnaposto `DIV`.

   Di seguito è riportato un esempio di segnaposto definito `DIV` elemento:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica del visualizzatore dichiarandolo per `.s7video360viewer` classe CSS di primo livello in unità assolute oppure utilizzando `stagesize` modificatore.

   È possibile inserire il dimensionamento in CSS direttamente nella pagina HTML o in un file CSS visualizzatore personalizzato, che viene successivamente assegnato a un record di predefinito visualizzatore in Adobe Experience Manager Assets - On-demand, o trasmesso esplicitamente utilizzando `style` comando.

   Consulta [Personalizzazione del visualizzatore Video360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione di una dimensione di visualizzatore statico nella pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   È possibile impostare `stagesize` modificatore nel record del predefinito visualizzatore in AEM Assets - on-demand. In alternativa, puoi trasmetterlo esplicitamente con il codice di inizializzazione del visualizzatore con `params` o come chiamata API come descritto nella sezione Riferimento comando, come segue:

   ```html {.line-numbers}
   video360viewer.setParam("stagesize", "640,640");
   ```

   Si consiglia un approccio basato su CSS, che viene utilizzato in questo esempio.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, puoi creare un’istanza di `s7viewers.Video360Viewer` classe, passa tutte le informazioni di configurazione al relativo costruttore e chiama `init()` su un&#39;istanza del visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto deve avere almeno `containerId` campo contenente il nome dell’ID contenitore del visualizzatore e nidificato `params` Oggetto JSON con parametri di configurazione supportati dal visualizzatore.

   In questo caso, il `params` l&#39;oggetto deve avere almeno l&#39;URL Image Server passato come `serverUrl` e la risorsa iniziale come `asset` parametro. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice, l’URL del server video passato come `videoserverurl` proprietà, risorsa iniziale come `asset` e dati interattivi come `interactivedata` proprietà. API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il `init()` metodo immediatamente prima della chiusura `BODY` o sul corpo `onload()` evento.

   Allo stesso tempo, l’elemento contenitore non deve ancora necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza del visualizzatore, mediante il passaggio delle opzioni di configurazione minime necessarie al costruttore e la chiamata al `init()` metodo. Nell&#39;esempio si presuppone quanto segue:

   * L’istanza del visualizzatore è `video360Viewer`.
   * Nome del segnaposto `DIV` è `s7viewer`.
   * L’URL di Image Server è `https://s7d9.scene7.com/is/image`.
   * L&#39;URL del server video è `https://s7d9.scene7.com/is/content`.
   * La risorsa è `Viewers/space_station_360-AVS`.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script>
   ```

   Il codice riportato di seguito è un esempio completo di una semplice pagina Web che incorpora il Visualizzatore video360 con una dimensione fissa:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
   <script type="text/javascript"> 
   var video360Viewer = new s7viewers.Video360Viewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/space_station_360-AVS", 
    "serverurl":"https://s7d9.scene7.com/is/image/", 
    "videoserverurl":"https://s7d9.scene7.com/is/content/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Design reattivo con altezza illimitata**

Con l’incorporamento di un design reattivo, la pagina web solitamente dispone di un layout flessibile che determina la dimensione di runtime del contenitore del visualizzatore `DIV`. Nell’esempio seguente, si supponga che la pagina web consenta il contenitore del visualizzatore `DIV` per occupare il 40% delle dimensioni della finestra del browser web, senza limitazioni di altezza. Il codice HTML della pagina Web sarà simile al seguente:

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

L’aggiunta del visualizzatore a tale pagina è simile alla procedura per l’incorporamento a dimensione fissa. L’unica differenza è che non è necessario definire esplicitamente la dimensione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del DIV del contenitore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell’incorporamento di dimensioni fisse. Aggiungi il DIV contenitore al file esistente `"holder"` DIV. Il codice seguente è un esempio completo. Osserva come cambiano le dimensioni del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporamento reattivo con definizione di larghezza e altezza**

Se è presente un’incorporazione reattiva con larghezza e altezza definite, lo stile della pagina web è diverso. Fornisce entrambe le dimensioni al `"holder"` DIV e centralo nella finestra del browser. Inoltre, la pagina web imposta le dimensioni del `HTML` e `BODY` al 100%.

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

Il resto dei passaggi di incorporamento è identico ai passaggi utilizzati per l’incorporamento reattivo con altezza illimitata. L’esempio risultante è il seguente:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
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
var video360Viewer = new s7viewers.Video360Viewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/space_station_360-AVS", 
 "serverurl":"https://s7d9.scene7.com/is/image/", 
 "videoserverurl":"https://s7d9.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporazione tramite API basata su set**

Invece di utilizzare l’inizializzazione basata su JSON, puoi utilizzare l’API basata su setter e il costruttore no-args. L’utilizzo di questo costruttore API non accetta parametri e i parametri di configurazione vengono specificati utilizzando `setContainerId()`, `setParam()`, e `setAsset()` Metodi API con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con l’API basata su setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d9.scene7.com/s7viewers/html5/js/Video360Viewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7video360viewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var video360Viewer = new s7viewers.Video360Viewer(); 
video360Viewer.setContainerId("s7viewer"); 
video360Viewer.setParam("serverurl", "https://s7d9.scene7.com/is/image/"); 
video360Viewer.setParam("videoserverurl", "https://s7d9.scene7.com/is/content/"); 
video360Viewer.setAsset("Viewers/space_station_360-AVS"); 
video360Viewer.init(); 
</script> 
</body> 
</html>
```
