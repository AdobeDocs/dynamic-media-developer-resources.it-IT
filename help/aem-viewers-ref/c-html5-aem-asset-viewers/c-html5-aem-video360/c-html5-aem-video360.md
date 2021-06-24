---
description: Il visualizzatore HTML5 Video360 è un lettore video a 360 gradi che riproduce video in streaming e progressivo a 360 codificati nel formato H.264, forniti da Dynamic Media Classic o AEM Dynamic Media.
solution: Experience Manager
title: Video360
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video VR 360
role: Developer,Business Practitioner
exl-id: 74dca3f6-ce89-4c5b-8459-c2c4ca8ed27c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '2590'
ht-degree: 0%

---

# Video360{#video}

Il visualizzatore HTML5 Video360 è un lettore video a 360° che riproduce video in streaming e progressivi a 360 codificati nel formato H.264, forniti da Dynamic Media Classic o da AEM Dynamic Media.

I video a 360 gradi, noti anche come video immersivi o video sferici, sono registrazioni video in cui una visualizzazione in ogni direzione viene registrata contemporaneamente, girata utilizzando una telecamera omnidirezionale o una raccolta di telecamere. Sono supportati sia i set video singoli che quelli adattivi. Il visualizzatore supporta inoltre l’utilizzo di video progressivi e flussi HLS ospitati su posizioni esterne.

Il rapporto di formato consigliato per video 360 è 2:1. L&#39;audio spaziale non è supportato. Il visualizzatore è progettato per funzionare solo con video a 360°; se si tenta di riprodurre un video diverso da 360, si verifica una riproduzione video distorta.

Il visualizzatore è progettato per funzionare sia con browser Web desktop che mobili che supportano video HTML5. Il visualizzatore supporta strumenti opzionali di condivisione social network.

Il visualizzatore Video360 utilizza la riproduzione video in streaming HTML5 in formato HLS nella configurazione predefinita ogni volta che il sistema sottostante lo supporta. Nei sistemi che non supportano lo streaming HTML5, il visualizzatore torna alla distribuzione video progressiva HTML5.

Il tipo di visualizzatore è 517.

## URL demo {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS](https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS)

## Requisiti di sistema {#section-b7270cc4290043399681dc504f043609}

Vedere [Requisiti di sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilizzo del visualizzatore video360 {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore HTML5 Video360 rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore HTML5 utilizzati da questo particolare visualizzatore, risorse, CSS) scaricati dal visualizzatore in fase di esecuzione.

Il visualizzatore HTML5 Video360 può essere utilizzato sia in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con IS-Viewers o in modalità incorporata, dove viene integrato nella pagina web di destinazione utilizzando API documentate.

La configurazione e lo skin sono simili a quelli degli altri visualizzatori descritti in questa guida. Tutta la skin viene ottenuta tramite i fogli di stile a cascata personalizzati (CSS).

Consulta [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento ai comandi comune a tutti i visualizzatori - URL](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-cmdref-url/c-html5-aem-video360-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

Il contenuto video a 360° richiede impostazioni di codifica più elevate rispetto al video standard a 360°. In altre parole, 360 contenuti devono avere una risoluzione più elevata rispetto ai video non-360 per ottenere la stessa qualità percepibile. Per i video a 360 si consiglia di considerare le seguenti impostazioni Predefinito video adattivo:

* 720p, 2500 kbps
* 1080p, 5000 kbps
* 1440p, 6600 kbps

Tuttavia, il servizio video codificato con impostazioni di alta qualità richiede una connessione a banda larga elevata sul dispositivo dell&#39;utente finale.

## Interazione con il visualizzatore video360 {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il visualizzatore HTML5 Video360 fornisce una serie di controlli standard dell&#39;interfaccia utente per la riproduzione video, come il pulsante di riproduzione/pausa, la bolla video dello scorrimento, l&#39;indicatore del tempo di riproduzione/totale, il controllo del volume e il pulsante a schermo intero. Tutti questi controlli sono raggruppati in una barra di controllo nella parte inferiore dell&#39;interfaccia utente del visualizzatore.

Tenere presente che sui dispositivi touch il controllo del volume è nascosto dall&#39;interfaccia utente, in quanto è possibile controllare il volume utilizzando solo i pulsanti hardware del dispositivo.

Quando il visualizzatore funziona in modalità pop-up, nell’interfaccia utente non è disponibile un pulsante a schermo intero.

Il visualizzatore supporta anche una varietà di strumenti di condivisione dei social media. Sono disponibili come un singolo pulsante nell’interfaccia utente che si espande in una barra degli strumenti di condivisione quando l’utente vi fa clic o vi tocca. La barra degli strumenti di condivisione contiene un&#39;icona per ogni tipo di canale di condivisione supportato come Facebook, Twitter, condivisione di e-mail, condivisione di codice da incorporare e condivisione di collegamenti. Quando si attivano gli strumenti di condivisione e-mail, incorporamento o collegamento, il visualizzatore visualizza una finestra di dialogo modale con un modulo di immissione dati corrispondente. Quando si chiamano Facebook o Twitter, il visualizzatore reindirizzerà l&#39;utente a una finestra di dialogo di condivisione standard da un servizio di social media. Inoltre, quando uno strumento di condivisione viene attivato, la riproduzione video viene messa in pausa automaticamente. Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di sicurezza del browser Web.

Il visualizzatore supporta la riproduzione di 360 video su cuffie VR (come Oculus Go e Oculus Rift), montaggi VR HMD (a testa montata) (come il cartone Google) e dispositivi non-VR abilitati (come browser desktop, tablet e telefoni cellulari non collegati ai montaggi VR HMD).

Non è necessaria alcuna configurazione aggiuntiva per visualizzare i contenuti video 360 sulle cuffie VR. Il visualizzatore rileva automaticamente la presenza di cuffie VR e mostra il pulsante &quot;VR&quot; sul contenuto video. L&#39;attivazione di questo pulsante &quot;VR&quot; consente il rendering video in modalità VR. Il visualizzatore supporta il rendering VR solo nei browser con supporto WebVR.

Per utilizzare i montaggi VR HMD, il modificatore `Video360Player.vrrender` deve essere impostato su `1` nella configurazione del visualizzatore, che forza il rendering stereoscopico.

Sulle cuffie VR e sui montaggi VR HMD si verifica un cambiamento del punto di vista in risposta al movimento delle cuffie, non è fornito altro controllo di riproduzione in modalità VR.

Quando si guarda un video a 360° su dispositivi abilitati per non VR, l&#39;utente finale può usare il mouse, il tocco o la tastiera per controllare la riproduzione video e il punto di vista.

Il visualizzatore supporta sia l’input touch che l’input del mouse su dispositivi Windows con touch screen e mouse, tuttavia questo supporto è limitato solo ai browser Web Chrome, Internet Explorer 11 e Edge.

Il visualizzatore è completamente accessibile da tastiera. Consulta [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporamento del visualizzatore video360 {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, quando fai clic su di essa, apre il visualizzatore in una finestra separata del browser. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare un design reattivo che viene visualizzato in modo diverso su diversi dispositivi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: a comparsa, incorporazione a dimensione fissa e incorporazione responsive della progettazione.

L’incorporazione di più video sulla stessa pagina è supportata sui tablet e sui dispositivi mobili. Nella maggior parte dei casi, è possibile riprodurre un solo video alla volta. Quando un utente inizia a riprodurre un video e poi prova a riprodurre un altro video, il primo video viene messo in pausa automaticamente. Il video messo in pausa automaticamente ricorda il tempo di riproduzione corrente, in modo che l&#39;utente possa sempre tornare ad esso e riprendere la riproduzione. L&#39;unica eccezione questa regola è nel browser Chrome su dispositivi Android 4.x, che può riprodurre video in parallelo.

**Informazioni sulla modalità a comparsa**

In modalità pop-up il visualizzatore viene aperto in una finestra o scheda separata del browser Web. Prende l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l&#39;orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` una chiamata JavaScript, un elemento `A` HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML predefinita per la modalità di funzionamento a comparsa. Si chiama [!DNL Video360Viewer.html] e si trova nella sottocartella [!DNL html5/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/Video360Viewer.html]

Puoi ottenere la personalizzazione visiva applicando CSS personalizzati.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
<a href="https://s7d9.scene7.com/s7viewers/html5/Video360Viewer.html?asset=Viewers/space_station_360-AVS" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento della progettazione reattiva**

Nella modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe avere già alcuni contenuti del cliente non correlati al visualizzatore. Il visualizzatore normalmente occupa solo una parte del patrimonio immobiliare di una pagina web.

I casi d’uso principali sono le pagine web orientate ai desktop o ai dispositivi tablet, nonché le pagine responsive progettate che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporazione a dimensione fissa viene utilizzata quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questa è la scelta migliore per le pagine web con layout statico.

L’incorporazione di design reattivo presuppone che il visualizzatore debba ridimensionare in fase di runtime in risposta alla modifica delle dimensioni del contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

Nella modalità di incorporamento della progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il proprio contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando senza limitazioni l’altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa funzionalità assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura laterale. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout di progettazione web reattivo come Bootstrap, Foundation e così via.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza del contenitore del visualizzatore `DIV`, il visualizzatore compila solo quell’area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio è quello di incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina web, effettua le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL Video360Viewer.js]. Il file [!DNL Video360Viewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/Video360Viewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Dynamic Media Classic di Adobe e viene servito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Dynamic Media Classic di Adobe in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script>
```

>[!NOTE]
>
>Dovresti fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non devi fare riferimento a file JavaScript aggiuntivi nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente alla libreria HTML5 SDK `Utils.js` caricata dal visualizzatore dal percorso contestuale `/s7viewers` (cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o librerie di visualizzatori runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, l’inserimento di un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore `DIV`.

   Aggiungi un elemento `DIV` vuoto alla pagina in cui desideri visualizzare il visualizzatore. L’ID dell’elemento `DIV` deve essere definito, perché viene passato successivamente all’API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il segnaposto `DIV` è un elemento posizionato, il che significa che la proprietà CSS `position` è impostata su `relative` o `absolute`.

   Affinché la funzione a schermo intero funzioni correttamente in Internet Explorer, accertati che non vi siano altri elementi nel DOM con un ordine di impilamento più elevato del segnaposto `DIV`.

   Di seguito è riportato un esempio di un elemento segnaposto definito `DIV`:

   ```
   <div id="s7viewer" style="position:relative;width:640px;height:360px;"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica del visualizzatore dichiarandola per la classe CSS di livello superiore `.s7video360viewer` in unità assolute o utilizzando il modificatore `stagesize`.

   Puoi inserire le dimensioni in CSS direttamente nella pagina HTML o in un file CSS per visualizzatori personalizzati, che viene poi assegnato a un record predefinito per visualizzatori in AEM Assets - on-demand, o passato esplicitamente utilizzando il comando `style` .

   Per ulteriori informazioni sullo stile del visualizzatore con CSS, consulta [Personalizzazione del visualizzatore Video360](../../c-html5-aem-asset-viewers/c-html5-aem-video360/c-html5-aem-video360-customizingviewer/c-html5-aem-video360-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) .

   Di seguito è riportato un esempio di definizione delle dimensioni di un visualizzatore statico nella pagina HTML:

   ```
   #s7viewer.s7video360viewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Puoi impostare il modificatore `stagesize` nel record predefinito del visualizzatore in AEM Assets - on-demand. Oppure, puoi passarlo esplicitamente con il codice di inizializzazione del visualizzatore con la raccolta `params` o come chiamata API come descritto nella sezione Riferimento comandi , come segue:

   ```
   video360viewer.setParam("stagesize", "640,640");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza della classe `s7viewers.Video360Viewer`, passa tutte le informazioni di configurazione al relativo costruttore e chiama il metodo `init()` su un’istanza di visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere un campo `containerId` che contiene il nome dell’ID del contenitore del visualizzatore e un oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore.

   In questo caso, l’oggetto `params` deve avere almeno l’URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice, l’URL del server video passato come proprietà `videoserverurl` , la risorsa iniziale come parametro `asset` e i dati interattivi come proprietà `interactivedata` . L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()` .

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web appena fatto. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del metodo `init()` . L&#39;esempio presuppone quanto segue:

   * L’istanza del visualizzatore è `video360Viewer`.
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

   Il codice seguente è un esempio completo di una pagina web banale che incorpora il visualizzatore Video360 con dimensioni fisse:

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

**Incorporazione di design reattivo con altezza illimitata**

Con l’incorporazione di design reattivo, la pagina web dispone normalmente di un layout flessibile che determina le dimensioni di runtime del contenitore del visualizzatore `DIV`. Nell’esempio seguente, si supponga che la pagina web consenta al contenitore del visualizzatore `DIV` di assumere il 40% delle dimensioni della finestra del browser Web, lasciando senza limitazioni l’altezza. Il codice HTML della pagina web sarà simile al seguente:

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

L’aggiunta del visualizzatore a una pagina di questo tipo è simile alla procedura per l’incorporazione a dimensione fissa. L’unica differenza è che non è necessario definire esplicitamente la dimensione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell&#39;incorporazione con dimensione fissa. Aggiungi il contenitore DIV al DIV esistente `"holder"`. Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

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

**Incorporazione reattiva con definizione di larghezza e altezza**

In caso di incorporamento dinamico con larghezza e altezza definite, lo stile della pagina web è diverso. Fornisce entrambe le dimensioni al DIV `"holder"` e lo centra nella finestra del browser. Inoltre, la pagina web imposta le dimensioni degli elementi `HTML` e `BODY` al 100%.

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

Gli altri passaggi di incorporamento sono identici ai passaggi utilizzati per l’incorporazione reattiva con altezza illimitata. L’esempio risultante è il seguente:

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

**Incorporazione tramite API basate su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L’utilizzo di questo costruttore API non accetta alcun parametro e i parametri di configurazione vengono specificati utilizzando i metodi `setContainerId()`, `setParam()` e `setAsset()` API con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con l’API basata su setter:

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
