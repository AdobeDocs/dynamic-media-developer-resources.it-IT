---
description: Il visualizzatore HTML5 Video360 è un lettore video a 360 gradi che riproduce in streaming e in progressivo 360 video codificati nel formato H.264, distribuito da Scene7 Publishing System o da AEM Dynamic Media.
seo-description: Il visualizzatore HTML5 Video360 è un lettore video a 360 gradi che riproduce in streaming e in progressivo 360 video codificati nel formato H.264, distribuito da Scene7 Publishing System o da AEM Dynamic Media.
seo-title: Video360
solution: Experience Manager
title: Video360
topic: Dynamic media
uuid: b03e6289-e012-4c62-835f-814463a27774
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '2613'
ht-degree: 0%

---


# Video360{#video}

Il visualizzatore HTML5 Video360 è un lettore video a 360 gradi che riproduce in streaming e in progressivo 360 video codificati nel formato H.264, distribuito da Scene7 Publishing System o da AEM Dynamic Media.

I video a 360 gradi, noti anche come video immersivi o sferici, sono registrazioni video in cui viene contemporaneamente registrata una visualizzazione in ogni direzione, ripresi utilizzando una telecamera omnidirezionale o una raccolta di telecamere. Sono supportati sia i singoli video che i set video adattivi. Il visualizzatore supporta inoltre l’utilizzo di video progressivi e flussi HLS ospitati su luoghi esterni.

Le proporzioni consigliate per i video 360 sono 2:1. L&#39;audio spaziale non è supportato. Il visualizzatore è progettato per funzionare solo con video 360; se si tenta di riprodurre un video diverso da 360, la riproduzione video risulta distorta.

Il visualizzatore è progettato per funzionare sia sui browser Web desktop che sui browser mobili che supportano video HTML5. Il visualizzatore supporta strumenti di condivisione mediante social network opzionali.

Il visualizzatore Video360 utilizza la riproduzione di video in streaming HTML5 in formato HLS nella configurazione predefinita ogni volta che il sistema sottostante lo supporta. Sui sistemi che non supportano lo streaming HTML5, il visualizzatore torna alla distribuzione video progressiva HTML5.

Il tipo di visualizzatore è 517.

## URL demo {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Requisiti di sistema {#section-b7270cc4290043399681dc504f043609}

Vedere [Requisiti di sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilizzo del visualizzatore Video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore HTML5 Video360 rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK per visualizzatori HTML5 utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Il visualizzatore HTML5 Video360 può essere utilizzato sia in modalità popup utilizzando la pagina HTML pronta per la produzione fornita con i visualizzatori IS, sia in modalità incorporata, in cui viene integrato nella pagina Web di destinazione tramite l’API documentata.

La configurazione e l’interfaccia sono simili a quelle degli altri visualizzatori descritti in questa guida. L&#39;associazione di interfacce viene realizzata tramite fogli di stile CSS personalizzati.

Consultate [Riferimento comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comune a tutti i visualizzatori - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Il contenuto video 360 richiede impostazioni di codifica più elevate rispetto al video standard non 360. In altre parole, i contenuti 360 devono avere una risoluzione più elevata rispetto ai video non 360 per ottenere la stessa qualità percepibile. Per i video a 360 si consiglia di considerare le seguenti impostazioni del predefinito per video adattivi:

* 720p, 2500 kbps
* 1080p, 5000 kbps
* 1440p, 6600 kbps

Tuttavia, la trasmissione di video codificati con impostazioni di alta qualità richiede una connessione a banda larga elevata sul dispositivo dell&#39;utente finale.

## Interazione con il visualizzatore Video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il visualizzatore HTML5 Video360 offre una serie di controlli standard dell’interfaccia utente per la riproduzione video, come il pulsante di riproduzione/pausa, la bolla temporale del video nella barra di scorrimento video, l’indicatore del tempo di riproduzione/totale, il controllo del volume e il pulsante a schermo intero. Tutti questi controlli sono raggruppati in una barra di controllo nella parte inferiore dell’interfaccia utente del visualizzatore.

Sui dispositivi touch il controllo del volume è nascosto dall&#39;interfaccia utente, perché è possibile controllare il volume solo utilizzando i pulsanti hardware del dispositivo.

Quando il visualizzatore funziona in modalità pop-up, nell’interfaccia utente non è disponibile un pulsante a schermo intero.

Il visualizzatore supporta anche una varietà di strumenti di condivisione per social media. Sono disponibili come pulsante singolo nell&#39;interfaccia utente che si espande in una barra degli strumenti di condivisione quando l&#39;utente fa clic su di essa o vi tocca. La barra degli strumenti di condivisione contiene un&#39;icona per ciascun tipo di canale di condivisione supportato, ad esempio Facebook, Twitter, condivisione e-mail, condivisione del codice da incorporare e condivisione dei collegamenti. Quando si attivano gli strumenti di condivisione e-mail, incorpora o collega, il visualizzatore visualizza una finestra di dialogo modale con un modulo di immissione dati corrispondente. Quando Facebook o Twitter vengono chiamati, il visualizzatore reindirizzerà l&#39;utente a una finestra di dialogo di condivisione standard da un servizio social media. Inoltre, quando uno strumento di condivisione viene attivato, la riproduzione video viene messa in pausa automaticamente. Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di protezione del browser Web.

Il visualizzatore supporta la riproduzione di video 360 su cuffie VR (come Oculus Go e Oculus Rift), montaggi VR HMD (visualizzazione a testa montata) (come Google Cardboard) e dispositivi non VR (come browser desktop, tablet e telefoni cellulari non connessi ai montaggi VR HMD).

Per visualizzare il contenuto video 360 sulle cuffie VR non è necessaria alcuna configurazione aggiuntiva. Il visualizzatore rileva automaticamente la presenza di cuffie VR e mostra il pulsante &quot;VR&quot; sul contenuto video. Attivando questo pulsante &quot;VR&quot; il rendering video viene attivato in modalità VR. Il visualizzatore supporta il rendering VR solo nei browser con supporto WebVR.

Per poter utilizzare l&#39;HMD VR, il modificatore `Video360Player.vrrender` deve essere impostato su `1` nella configurazione del visualizzatore, che forza il rendering stereoscopico.

Sulle cuffie VR e sui montaggi HMD VR il punto di vista cambia in risposta al movimento delle cuffie, non altri controlli di riproduzione sono forniti in modalità VR.

Quando si guarda un video a 360 su dispositivi non VR, l’utente finale può usare il mouse, il tocco o la tastiera per controllare la riproduzione video e il punto di vista.

Il visualizzatore supporta sia l&#39;input touch che l&#39;input del mouse su dispositivi Windows con touch screen e mouse, tuttavia questo supporto è limitato solo a Chrome, Internet Explorer 11 e browser Web Edge.

Il visualizzatore è completamente accessibile tramite tastiera. Vedere [Accessibilità e navigazione da tastiera](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporamento del visualizzatore Video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Diverse pagine Web hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina Web fornisce un collegamento che, quando viene fatto clic, apre il visualizzatore in una finestra browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest&#39;ultimo caso, la pagina Web può avere un layout di pagina statico oppure utilizzare un design reattivo che viene visualizzato in modo diverso su diversi dispositivi o per diverse dimensioni di finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: finestre a comparsa, incorporamento a dimensione fissa e incorporazione reattiva della progettazione.

L&#39;incorporamento di più video sulla stessa pagina è supportato su tablet e dispositivi mobili. Nella maggior parte dei casi, è possibile riprodurre un solo video alla volta. Quando un utente avvia la riproduzione di un video e tenta di riprodurre un altro video, il primo video viene automaticamente messo in pausa. Il video che è stato messo in pausa automatica ricorda il tempo di riproduzione corrente, in modo che l’utente possa sempre tornare al video e riprendere la riproduzione. L&#39;unica eccezione questa regola è nel browser Chrome su dispositivi Android 4.x, che può riprodurre video in parallelo.

**Informazioni sulla modalità a comparsa**

In modalità pop-up, il visualizzatore viene aperto in una finestra o in una scheda separata del browser Web. Richiede l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l&#39;orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando la chiamata `window.open()` JavaScript, l&#39;elemento HTML configurato correttamente `A` o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML out-of-box per la modalità operativa a comparsa. Si chiama [!DNL Video360Viewer.html] e si trova nella sottocartella [!DNL html5/] della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Potete ottenere la personalizzazione visiva applicando CSS personalizzato.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina Web esistente, che potrebbe già presentare contenuti per clienti non correlati al visualizzatore. In genere, il visualizzatore occupa solo una parte del patrimonio immobiliare di una pagina Web.

I casi d’uso principali sono le pagine Web orientate per desktop o dispositivi tablet, nonché le pagine reattive progettate che adattano automaticamente il layout in base al tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica la dimensione dopo il caricamento iniziale. Questa è la scelta migliore per le pagine Web con layout statico.

L&#39;incorporazione reattiva della progettazione presuppone che il visualizzatore debba ridimensionare in fase di esecuzione in seguito alla modifica delle dimensioni del suo contenitore `DIV`. L’esempio più comune è l’aggiunta di un visualizzatore a una pagina Web con layout di pagina flessibile.

In modalità di incorporazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina Web ridimensiona il contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente l’altezza in base alle proporzioni della risorsa utilizzata. Questa funzione assicura che la risorsa si adatti perfettamente alla vista senza riempimenti laterali. Questo caso di utilizzo è il più comune per le pagine Web che utilizzano framework di layout reattivi per la progettazione Web come Bootstrap, Foundation e così via.

In caso contrario, se la pagina Web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore riempie solo tale area e ha le stesse dimensioni del layout della pagina Web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser Web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuate le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell&#39;intestazione HTML. Prima di poter utilizzare l&#39;API del visualizzatore, accertatevi di includere [!DNL Video360Viewer.js]. Il file [!DNL Video360Viewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Potete utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Dynamic Media Classic  Adobe e viene distribuito dallo stesso dominio. In caso contrario, specificate un percorso completo per uno dei server Dynamic Media Classic  Adobe in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>È consigliabile fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non dovete fare riferimento ad altri file JavaScript nel codice della pagina Web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fate riferimento direttamente alla libreria HTML5 SDK `Utils.js` caricata dal visualizzatore dal percorso contestuale `/s7viewers` (il cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o librerie di visualizzatori runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore.  Adobe non conserva sul server versioni precedenti del visualizzatore secondario `includes`.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi codice JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina, si interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione di prodotto.

1. Definizione del contenitore `DIV`.

   Aggiungete un elemento `DIV` vuoto alla pagina in cui desiderate visualizzare il visualizzatore. L&#39;ID dell&#39;elemento `DIV` deve essere definito perché l&#39;ID viene passato successivamente all&#39;API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il segnaposto `DIV` è un elemento posizionato, il che significa che la proprietà `position` CSS è impostata su `relative` o `absolute`.

   Affinché la funzione a schermo intero funzioni correttamente in Internet Explorer, accertatevi che nel DOM non vi siano altri elementi con un ordine di impilamento superiore a quello del segnaposto `DIV`.

   Di seguito è riportato un esempio di un elemento segnaposto definito `DIV`:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   Potete impostare le dimensioni statiche per il visualizzatore dichiarandolo per la classe CSS di livello principale `.s7video360viewer` in unità assolute oppure utilizzando il modificatore `stagesize`.

   Potete inserire le dimensioni in CSS direttamente nella pagina HTML o in un file CSS del visualizzatore personalizzato, che verrà quindi assegnato a un record di predefinito per visualizzatori in  AEM Assets - su richiesta, o trasmesso esplicitamente tramite il comando `style`.

   Per ulteriori informazioni sullo stile del visualizzatore con CSS, consultate [Personalizzazione del visualizzatore Video360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0).

   Di seguito è riportato un esempio di definizione di una dimensione visualizzatore statica nella pagina HTML:

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Potete impostare il modificatore `stagesize` nel record del predefinito per visualizzatori in  AEM Assets - su richiesta. Oppure, potete trasmetterlo esplicitamente con il codice di inizializzazione del visualizzatore con la raccolta `params`, o come chiamata API come descritto nella sezione Riferimento comando, come segue:

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi descritti qui sopra, potete creare un&#39;istanza della classe `s7viewers.Video360Viewer`, trasmettere tutte le informazioni di configurazione al relativo costruttore e chiamare il metodo `init()` su un&#39;istanza di visualizzatore. Le informazioni di configurazione vengono trasmesse al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere un campo `containerId` che contiene il nome dell&#39;ID contenitore del visualizzatore e un oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore.

   In questo caso, l&#39;oggetto `params` deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. L&#39;API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice, l&#39;URL del server video trasmesso come proprietà `videoserverurl`, la risorsa iniziale come parametro `asset` e i dati interattivi come proprietà `interactivedata`. L&#39;API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore del visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser ritardano la creazione del DOM fino alla fine della pagina Web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()`.

   Allo stesso modo, l&#39;elemento contenitore non deve necessariamente far parte del layout della pagina Web per il momento. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del metodo `init()`. L&#39;esempio presuppone quanto segue:

   * L&#39;istanza del visualizzatore è `video360Viewer`.
   * Il nome del segnaposto `DIV` è `s7viewer`.
   * L&#39;URL del server immagini è `https://s7d9.scene7.com/is/image`.
   * L’URL del server video è `https://s7d9.scene7.com/is/content`.
   * La risorsa è `Viewers/space_station_360-AVS`.

   ```
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

   Il codice seguente è un esempio completo di una pagina Web banale che incorpora il visualizzatore Video360 con una dimensione fissa:

   ```
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

**Incorporazione responsive con altezza illimitata**

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

**Incorporazione reattiva con larghezza e altezza definite**

In caso di incorporamento reattivo con larghezza e altezza definite, lo stile della pagina Web è diverso. Fornisce entrambe le dimensioni al DIV `"holder"` e lo centra nella finestra del browser. Inoltre, la pagina Web imposta la dimensione dell&#39;elemento `HTML` e `BODY` su 100%.

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

**Incorporazione tramite l&#39;API basata su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L&#39;utilizzo di questo costruttore di API non accetta parametri e i parametri di configurazione vengono specificati utilizzando i metodi `setContainerId()`, `setParam()` e `setAsset()` API con chiamate JavaScript separate.

L&#39;esempio seguente illustra l&#39;utilizzo dell&#39;incorporamento a dimensione fissa con l&#39;API basata su setter:

```
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

