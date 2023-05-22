---
title: Video interattivo
description: Interactive Video Viewer è un lettore video che riproduce video in streaming e progressivi codificati nel formato H.264.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: e54b0b1f-b015-4592-82e2-99f5080543e3
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2211'
ht-degree: 0%

---

# Video interattivo{#interactive-video}

Interactive Video Viewer è un lettore video che riproduce video in streaming e progressivi codificati nel formato H.264.

Il visualizzatore mostra anche campioni di prodotto interattivi accanto al contenuto video. Sono supportati sia set per video singolo che set per video adattivi. È progettato per funzionare sia su browser Web desktop che mobili che supportano video HTML5. Il visualizzatore supporta i sottotitoli facoltativi visualizzati sopra al contenuto video, alla navigazione dei capitoli video e agli strumenti di condivisione per social network. Lo scopo di questo visualizzatore è quello di aiutarti a implementare un’esperienza &quot;video acquistabile&quot;. In altre parole, gli utenti possono selezionare un campione associato a una particolare area temporale video e venire reindirizzati a una pagina Quickview o a una pagina dei dettagli del prodotto sul sito web del cliente.

Il tipo di visualizzatore è 510.

## URL demo {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/glacier/InteractiveVideoViewerDemo.html)

E

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-video/AXIS/index.html)

## Requisiti di sistema {#section-b7270cc4290043399681dc504f043609}

Consulta [Requisiti di sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilizzo del Visualizzatore video interattivo {#section-e6c68406ecdc4de781df182bbd8088b4}

Visualizzatore video interattivo rappresenta un file JavaScript principale e un set di file di supporto scaricati dal visualizzatore in fase di esecuzione. Un singolo JavaScript è incluso con tutti i componenti SDK del Visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS.

Il Visualizzatore video interattivo può essere utilizzato in modalità pop-up utilizzando una pagina HTML pronta per la produzione fornita con i Visualizzatori Image Server. Può essere utilizzato anche in modalità incorporata, dove viene integrato nella pagina web di destinazione utilizzando l’API documentata.

La configurazione e lo skin sono simili a quelli degli altri visualizzatori descritti in questa guida. Tutte le operazioni di skin vengono eseguite tramite CSS (Cascading Style Sheets) personalizzati.

Consulta [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore video interattivo {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il Visualizzatore video interattivo offre una serie di controlli standard dell’interfaccia utente per la riproduzione di video, ad esempio un pulsante di riproduzione/pausa, uno scorrimento video, una bolla temporale, un indicatore del tempo totale/tempo di riproduzione, un controllo del volume, un pulsante a schermo intero e un interruttore per sottotitoli. Tutti questi controlli sono raggruppati in una barra di controllo direttamente sotto la visualizzazione principale.

Sui dispositivi touch, il controllo del volume è nascosto dall&#39;interfaccia utente, perché è possibile controllare il volume solo utilizzando i pulsanti hardware del dispositivo.

Quando il visualizzatore funziona in modalità pop-up, nell’interfaccia utente non è disponibile un pulsante a schermo intero.

Il visualizzatore mostra un pannello con campioni interattivi a destra dell’area di visualizzazione video. L&#39;elenco dei campioni avanza automaticamente durante la riproduzione del video, in modo che vengano visualizzati i campioni corrispondenti all&#39;area video corrente. Toccando o facendo clic su un campione viene attivata un&#39;azione associata a tale campione durante il tempo di creazione. A seconda della configurazione, il trigger può essere reindirizzato a una pagina diversa del sito Web. In alternativa, può trasmettere le informazioni sul prodotto alla logica della pagina web, che a sua volta può attivare l’apertura di un Quickview che mostra il contenuto del prodotto correlato.

È possibile navigare rapidamente tra i contenuti video quando il capitolo video è attivato. I capitoli video vengono visualizzati come marcatori nella traccia di scorrimento video e mostrano il titolo e la descrizione del capitolo al passaggio del mouse (o a un singolo tocco sui sistemi touch). Il cliente può effettuare una ricerca in un particolare capitolo facendo clic su un marcatore di capitolo o toccando una bolla di descrizione del capitolo.

Il visualizzatore supporta anche vari strumenti di condivisione dei social media. Sono disponibili come pulsante singolo nell’interfaccia utente, che si espande in una barra degli strumenti di condivisione quando l’utente fa clic o tocca su di essa. La barra degli strumenti Condivisione contiene un’icona per ogni tipo di canale di condivisione supportato, ad esempio Facebook, Twitter, condivisione e-mail, condivisione di codice da incorporare e condivisione di collegamenti. Quando gli strumenti di condivisione e-mail, condivisione di incorporamento o condivisione di collegamenti sono attivati, il visualizzatore visualizza una finestra di dialogo modale con il modulo di immissione dati corrispondente. Quando si chiama Facebook o Twitter, il visualizzatore reindirizza l&#39;utente a una finestra di dialogo di condivisione standard da un servizio di social media. Inoltre, quando uno strumento di condivisione è attivato, la riproduzione video viene sospesa automaticamente. Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di sicurezza del browser Web.

Il visualizzatore è completamente accessibile da tastiera. Consulta [Accessibilità della tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore video interattivo {#section-6bb5d3c502544ad18a58eafe12a13435}

Il Visualizzatore video interattivo è incorporato nella pagina di hosting. Tale pagina web può avere un layout statico, o può essere &quot;reattiva&quot; e visualizzata in modo diverso su dispositivi diversi o per diverse dimensioni della finestra del browser.

Per soddisfare queste esigenze, il visualizzatore supporta due modalità operative principali: l’incorporamento a dimensione fissa e l’incorporamento reattivo.

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento a progettazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe già avere alcuni contenuti per i clienti non correlati al visualizzatore. Il visualizzatore occupa normalmente solo una parte del patrimonio immobiliare di una pagina web.

I casi d’uso principali sono le pagine web orientate per desktop o dispositivi tablet e le pagine progettate responsive che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questa funzionalità è la scelta migliore per le pagine web con un layout statico.

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

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL InterativeVideoViewer.js]. Il [!DNL InteractiveVideoViewer.js] il file si trova sotto [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveVideoViewer.js]

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
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica del visualizzatore dichiarandolo per `.s7interactivevideoviewer` classe CSS di primo livello in unità assolute oppure utilizzando `stagesize` modificatore.

   Puoi inserire il dimensionamento in CSS direttamente nella pagina HTML. Oppure, puoi inserirlo in un file CSS visualizzatore personalizzato, che viene successivamente assegnato a un record di predefinito visualizzatore in Adobe Experience Manager Assets - On-demand, o trasmesso esplicitamente utilizzando `style` comando.

   Consulta [Personalizzazione del visualizzatore video interattivo](../../c-html5-aem-asset-viewers/c-html5-aem-int-video/c-html5-aem-int-video-customizingviewer/c-html5-aem-int-video-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione di una dimensione di visualizzatore statico nella pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7interactivevideoviewer { 
    width: 640px; 
    height: 640px; 
   }
   ```

   È possibile impostare `stagesize` modificatore nel record del predefinito visualizzatore in Experience Manager Assets - On-demand. In alternativa, puoi trasmetterlo esplicitamente con il codice di inizializzazione del visualizzatore con `params` o come chiamata API come descritto nella sezione Riferimento comando, come segue:

   ```html {.line-numbers}
   interactivevideoviewer.setParam("stagesize", "640,640");
   ```

   Si consiglia un approccio basato su CSS, che viene utilizzato in questo esempio.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, puoi creare un’istanza di `s7viewers.InteractiveVideoViewer` classe, passa tutte le informazioni di configurazione al relativo costruttore e chiama `init()` su un&#39;istanza del visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto deve avere almeno `containerId` campo contenente il nome dell’ID contenitore del visualizzatore e nidificato `params` Oggetto JSON con parametri di configurazione supportati dal visualizzatore.

   In questo caso, il `params` l&#39;oggetto deve avere almeno l&#39;URL Image Server passato come `serverUrl` e la risorsa iniziale come `asset` parametro. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice, l’URL del server video passato come `videoserverurl` proprietà, risorsa iniziale come `asset` e dati interattivi come `interactivedata` proprietà. API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il `init()` metodo immediatamente prima della chiusura `BODY` o sul corpo `onload()` evento.

   Allo stesso tempo, l’elemento contenitore non fa ancora necessariamente parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza del visualizzatore, mediante il passaggio delle opzioni di configurazione minime necessarie al costruttore e la chiamata al `init()` metodo. Nell&#39;esempio si presuppone quanto segue:

   * L’istanza del visualizzatore è `interactiveVideoViewer`.
   * Nome del segnaposto `DIV` è `s7viewer`.
   * L’URL di Image Server è `https://aodmarketingna.assetsadobe.com/is/image/`.
   * L&#39;URL del server video è `https://gateway-na.assetsadobe.com/DMGateway/public/aodmarketingna`.
   * L’URL del contenuto è `https://aodmarketingna.assetsadobe.com/`.
   * La risorsa è `/content/dam/mac/aodmarketingna/dm-viewers-content/video/Glacier.mp4`.
   * I dati interattivi sono `is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.svideo.vtt`.

   ```html {.line-numbers}
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

   Il codice che segue è un esempio completo di una pagina web banale che incorpora il Visualizzatore video interattivo con una dimensione fissa:

   ```html {.line-numbers}
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

La pagina di esempi seguente illustra usi più reali dell’incorporamento di design responsive con altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Percorso demo alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

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

**Incorporazione tramite API basata su set**

Invece di utilizzare l’inizializzazione basata su JSON, puoi utilizzare l’API basata su setter e il costruttore no-args. L’utilizzo di questo costruttore API non accetta parametri e i parametri di configurazione vengono specificati utilizzando `setContainerId()`, `setParam()`, e `setAsset()` Metodi API con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con l’API basata su setter:

```html {.line-numbers}
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
