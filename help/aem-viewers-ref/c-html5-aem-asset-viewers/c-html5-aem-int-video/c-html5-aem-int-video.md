---
description: Interactive Video Viewer è un lettore video che riproduce in streaming e video progressivo codificato in formato H.264.
solution: Experience Manager
title: Video interattivo
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '2234'
ht-degree: 0%

---

# Video interattivo{#interactive-video}

Interactive Video Viewer è un lettore video che riproduce in streaming e video progressivo codificato in formato H.264.

Il visualizzatore mostra anche i campioni di prodotto interattivi accanto al contenuto video. Sono supportati sia i set video singoli che quelli adattivi. È progettato per funzionare sia sui browser web desktop che mobili che supportano video HTML5. Il visualizzatore supporta i sottotitoli codificati opzionali visualizzati sopra il contenuto video, la navigazione nei capitoli video e gli strumenti di condivisione social network. Lo scopo di questo visualizzatore è quello di aiutarti a implementare un’esperienza &quot;video acquistabile&quot;. In altre parole, gli utenti possono selezionare un campione associato a una particolare area geografica del video e venire reindirizzati a una visualizzazione rapida o a una pagina di dettagli del prodotto sul sito web del cliente.

Il tipo di visualizzatore è 510.

## URL demo {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

e

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-video/AXIS/index.html)

## Requisiti di sistema {#section-b7270cc4290043399681dc504f043609}

Vedere [Requisiti di sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilizzo del visualizzatore video interattivo {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore video interattivo rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Il visualizzatore video interattivo può essere utilizzato in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con i visualizzatori Image Server. Può essere utilizzato anche in modalità incorporata, dove viene integrato nella pagina web di destinazione utilizzando l’API documentata.

La configurazione e lo skin sono simili a quelli degli altri visualizzatori descritti in questa guida. Tutta la skin viene ottenuta tramite i fogli di stile a cascata personalizzati (CSS).

Consulta [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento ai comandi comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore video interattivo {#section-642e66ca38cd4032992840ec6c0b0cd2}

Interactive Video Viewer fornisce una serie di controlli standard dell’interfaccia utente per la riproduzione video, come un pulsante Play/Pause, uno scorrimento video, una bolla del tempo video, un indicatore del tempo di riproduzione/totale, il controllo del volume, il pulsante a schermo intero e l’interruttore per i sottotitoli. Tutti questi controlli sono raggruppati in una barra di controllo direttamente sotto la vista principale.

Tenere presente che sui dispositivi touch il controllo del volume è nascosto dall&#39;interfaccia utente, in quanto è possibile controllare il volume utilizzando solo i pulsanti hardware del dispositivo.

Quando il visualizzatore funziona in modalità pop-up, nell’interfaccia utente non è disponibile un pulsante a schermo intero.

Il visualizzatore mostra un pannello con campioni interattivi a destra dell’area di visualizzazione video. L’elenco dei campioni avanza automaticamente durante la riproduzione del video, in modo che vengano visualizzati i campioni corrispondenti all’area video corrente. Quando si tocca o fai clic su un campione, viene attivata un’azione associata al campione durante l’authoring. A seconda di come è stato configurato, il trigger può reindirizzare a una pagina diversa del sito web o restituire informazioni di prodotto alla logica della pagina web, che a sua volta può attivare l’apertura di una Visualizzazione rapida che mostra il contenuto del prodotto correlato.

È possibile navigare rapidamente nel contenuto video quando si attiva il filtro video. I capitoli video vengono visualizzati come marcatori nella traccia di scorrimento video e mostrano il titolo e la descrizione del capitolo su roll over (o su un singolo tocco su sistemi touch). Il cliente può &quot;cercare&quot; un capitolo specifico facendo clic su un marcatore capitolo o toccando una bolla di descrizione capitolo.

Il visualizzatore supporta anche una varietà di strumenti di condivisione dei social media. Sono disponibili come un singolo pulsante nell’interfaccia utente che si espande in una barra degli strumenti di condivisione quando l’utente vi fa clic o vi tocca. La barra degli strumenti di condivisione contiene un&#39;icona per ogni tipo di canale di condivisione supportato come Facebook, Twitter, condivisione e-mail, condivisione del codice di incorporamento e condivisione dei collegamenti. Quando si attivano gli strumenti di condivisione e-mail, incorporamento o collegamento, il visualizzatore visualizza una finestra di dialogo modale con un modulo di immissione dati corrispondente. Quando si chiamano Facebook o Twitter, il visualizzatore reindirizzerà l&#39;utente a una finestra di dialogo di condivisione standard da un servizio di social media. Inoltre, quando uno strumento di condivisione viene attivato, la riproduzione video viene messa in pausa automaticamente. Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di sicurezza del browser Web.

Il visualizzatore è completamente accessibile da tastiera. Consulta [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione di un visualizzatore video interattivo {#section-6bb5d3c502544ad18a58eafe12a13435}

Il visualizzatore video interattivo è progettato per essere incorporato nella pagina di hosting. Una pagina web di questo tipo può avere un layout statico o può essere &quot;reattiva&quot; e può essere visualizzata in modo diverso su diversi dispositivi o per diverse dimensioni della finestra del browser.

Per soddisfare queste esigenze, il visualizzatore supporta due modalità di funzionamento principali: incorporazione a dimensione fissa e incorporazione reattiva.

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

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL InterativeVideoViewer.js]. Il file [!DNL InteractiveVideoViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

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
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica del visualizzatore dichiarandola per la classe CSS di livello superiore `.s7interactivevideoviewer` in unità assolute o utilizzando il modificatore `stagesize`.

   Puoi inserire le dimensioni in CSS direttamente nella pagina HTML o in un file CSS per visualizzatori personalizzati, che viene poi assegnato a un record predefinito per visualizzatori in AEM Assets - on-demand, o passato esplicitamente utilizzando il comando `style` .

   Per ulteriori informazioni sullo stile del visualizzatore con CSS, consulta [Personalizzazione del visualizzatore video interattivo](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) .

   Di seguito è riportato un esempio di definizione delle dimensioni di un visualizzatore statico nella pagina HTML:

   ```
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   Puoi impostare il modificatore `stagesize` nel record predefinito del visualizzatore in AEM Assets - on-demand. Oppure, puoi passarlo esplicitamente con il codice di inizializzazione del visualizzatore con la raccolta `params` o come chiamata API come descritto nella sezione Riferimento comandi , come segue:

   ```
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza della classe `s7viewers.InteractiveVideoViewer`, passa tutte le informazioni di configurazione al relativo costruttore e chiama il metodo `init()` su un’istanza di visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere un campo `containerId` che contiene il nome dell’ID del contenitore del visualizzatore e un oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore.

   In questo caso, l’oggetto `params` deve avere almeno l’URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice, l’URL del server video passato come proprietà `videoserverurl` , la risorsa iniziale come parametro `asset` e i dati interattivi come proprietà `interactivedata` . L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()` .

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web appena fatto. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. Ciò che accade, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del metodo `init()` . L&#39;esempio presuppone quanto segue:

   * L’istanza del visualizzatore è `interactiveVideoViewer`.
   * Il nome del segnaposto `DIV` è `s7viewer`.
   * L&#39;URL del server immagini è `https://aodmarketingna.assetsadobe.com/is/image/`.
   * L’URL del server video è `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * L’URL del contenuto è `https://aodmarketingna.assetsadobe.com/`.
   * La risorsa è `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * I dati interattivi sono `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
   } 
   }).init(); 
   </script>
   ```

   Il codice seguente è un esempio completo di una pagina web banale che incorpora il Visualizzatore video interattivo con dimensioni fisse:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;"></div> 
   <script type="text/javascript"> 
   var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
   "config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
    "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
    "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
    "contenturl":"https://aodmarketingna.assetsadobe.com/", 
   "interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La pagina degli esempi seguenti illustra gli utilizzi più reali dell’incorporazione di design reattivo a altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- OLD DEMO LOCATION-KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
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
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4", 
"config":"/etc/dam/presets/viewer/Shoppable_Video_Dark", 
 "serverurl":"https://aodmarketingna.assetsadobe.com/is/image/", 
 "videoserverurl":"https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna", 
 "contenturl":"https://aodmarketingna.assetsadobe.com/", 
"interactivedata":"is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt" 
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
<script type="text/javascript" src="https://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactivevideoviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative;width:640px;height:360px;"></div> 
<script type="text/javascript"> 
var interactiveVideoViewer = new s7viewers.InteractiveVideoViewer(); 
interactiveVideoViewer.setContainerId("s7viewer"); 
interactiveVideoViewer.setParam("config", "/etc/dam/presets/viewer/Shoppable_Video_Dark"); 
interactiveVideoViewer.setParam("serverurl", "https://aodmarketingna.assetsadobe.com/is/image/"); 
interactiveVideoViewer.setParam("videoserverurl", "https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna"); 
interactiveVideoViewer.setParam("contenturl", "https://aodmarketingna.assetsadobe.com/"); 
interactiveVideoViewer.setParam("interactivedata", "is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt"); 
interactiveVideoViewer.setAsset("/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4"); 
interactiveVideoViewer.init(); 
</script> 
</body> 
</html>
```
