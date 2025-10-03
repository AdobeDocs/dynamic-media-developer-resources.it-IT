---
title: Zoom
description: Visualizzatore zoom è un visualizzatore di immagini che visualizza un'immagine ingrandita. Questo visualizzatore funziona con i set di immagini e la navigazione viene eseguita utilizzando i campioni. Sono disponibili strumenti di zoom, supporto per schermo intero, campioni e un pulsante di chiusura opzionale. È progettato per funzionare su desktop e dispositivi mobili.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 81a74026-fb15-4f57-a4c7-1ab005950245
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '2278'
ht-degree: 0%

---

# Zoom{#zoom}

Visualizzatore zoom è un visualizzatore di immagini che visualizza un&#39;immagine ingrandita. Questo visualizzatore funziona con i set di immagini e la navigazione viene eseguita utilizzando i campioni. Sono disponibili strumenti di zoom, supporto per schermo intero, campioni e un pulsante di chiusura opzionale. È progettato per funzionare su desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Visualizzatore di tipo 502.

Consulta [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Utilizzo del Visualizzatore zoom {#section-e6c68406ecdc4de781df182bbd8088b4}

Il Visualizzatore zoom rappresenta un file JavaScript principale e un set di file di supporto (un singolo JavaScript include con tutti i componenti del Visualizzatore SDK utilizzati da questo particolare visualizzatore, risorse, CSS) scaricati dal visualizzatore in fase di esecuzione.

È possibile utilizzare il Visualizzatore zoom in modalità pop-up utilizzando una pagina HTML pronta per la produzione fornita con i visualizzatori IS o in modalità incorporata, in cui viene integrato nella pagina web di destinazione utilizzando l’API documentata.

La configurazione e l’interfaccia sono simili a quelle degli altri visualizzatori. Tutte le operazioni di skin vengono eseguite tramite CSS personalizzato.

Vedi [Riferimento al comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento al comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore zoom {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il Visualizzatore zoom supporta i seguenti gesti touch comuni in altre applicazioni mobili. Quando il visualizzatore non è in grado di elaborare il gesto di scorrimento dell’utente, inoltra l’evento al browser web per eseguire lo scorrimento nativo della pagina. Questo tipo di funzionalità consente all’utente di navigare attraverso la pagina anche se il visualizzatore occupa la maggior parte dell’area dello schermo del dispositivo.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Tocco singolo </p> </td> 
   <td colname="col2"> <p> Seleziona la nuova miniatura nei campioni. Nella vista principale nasconde o rivela gli elementi dell’interfaccia utente. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Doppio tocco </p> </td> 
   <td colname="col2"> <p> Esegue lo zoom di un livello fino al raggiungimento dell'ingrandimento massimo. Il doppio tocco successivo ripristina lo stato di visualizzazione iniziale del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pizzicare </p> </td> 
   <td colname="col2"> <p>Ingrandisce o riduce. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento orizzontale </p> </td> 
   <td colname="col2"> <p> Scorre l'elenco dei campioni nella barra dei campioni. </p> <p> Se l'immagine è in uno stato di reimpostazione e il parametro <span class="codeph"> frametransition </span> è impostato su slide, la risorsa viene modificata con l'animazione della diapositiva. Per le altre modalità <span class="codeph"> di frametransition </span>, il movimento esegue lo scorrimento nativo della pagina. </p> <p> Se l'immagine è ingrandita, l'immagine viene spostata orizzontalmente. Se l'immagine viene spostata sul bordo della vista e viene eseguito un passaggio nella stessa direzione, il movimento esegue lo scorrimento nativo della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento verticale </p> </td> 
   <td colname="col2"> <p> Se l'immagine è reimpostata, il movimento esegue lo scorrimento nativo della pagina. </p> <p> Quando l'immagine viene ingrandita, l'immagine viene spostata verticalmente. Se l'immagine viene spostata sul bordo della vista e viene eseguito un passaggio nella stessa direzione, il movimento esegue lo scorrimento nativo della pagina. </p> <p> Se il movimento viene eseguito all'interno dell'area dei campioni, esegue uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta sia l&#39;input tocco che l&#39;input del mouse su dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Consulta [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione visualizzatore zoom {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, se selezionato, apre il visualizzatore in una finestra del browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout statico o utilizzare un design reattivo che viene visualizzato in modo diverso su dispositivi diversi o per finestre del browser di dimensioni diverse. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità operative principali: popup, incorporamento di dimensioni fisse e incorporamento di progetti reattivi.

**Informazioni sulla modalità popup**

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda del browser Web separata. Occupa l’intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l’orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando `window.open()` chiamata JavaScript, `A` elemento HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML preconfigurata per la modalità operativa popup. La pagina HTML predefinita è denominata `ZoomViewer.html` e si trova nella sottocartella `html5/` della distribuzione IS-Viewers standard, come indicato di seguito:

`<s7viewers_root>/html5/ZoomViewer.html`

Applica CSS personalizzato per ottenere un aspetto personalizzato per la pagina.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore nella nuova finestra:

```html {.line-numbers}
 <a href="http://s7d1.scene7.com/s7viewers/html5/ZoomViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample" 
target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento di progettazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe già includere contenuto del cliente non correlato al visualizzatore. Il visualizzatore occupa normalmente solo una parte del patrimonio immobiliare della pagina web.

I casi d’uso principali sono le pagine web orientate per desktop o dispositivi tablet e le pagine progettate responsive che regolano automaticamente il layout, a seconda del tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questa opzione è la scelta migliore per le pagine web con un layout statico.

La modalità di incorporamento della progettazione reattiva presuppone che il ridimensionamento del visualizzatore sia necessario durante il runtime a causa della modifica delle dimensioni del relativo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout flessibile.

In modalità di incorporamento di progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`, lasciando libera la sua altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa logica assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura sui lati. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout reattivi come Bootstrap e Foundation.

Se la pagina Web imposta sia la larghezza che l&#39;altezza del contenitore del visualizzatore `DIV`, il visualizzatore riempirà tale area e seguirà le dimensioni fornite dalla pagina Web. Ad esempio, incorporando il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

## Incorporamento a dimensione fissa {#section-44f365e6c0dd40709467a459afa82a7f}

Per aggiungere il visualizzatore a una pagina Web, effettuare le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del DIV del contenitore.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l&#39;API del visualizzatore, assicurati di includere [!DNL ZoomViewer.js]. Il file [!DNL ZoomViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/ZoomViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene fornito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo è simile al seguente:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/ZoomViewer.js"></script>
```

>[!NOTE]
>
>Fare riferimento solo al file JavaScript `include` del visualizzatore principale nella pagina. Non fare riferimento ad altri file JavaScript nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente alla libreria `Utils.js` di HTML5 SDK caricata dal visualizzatore dal percorso di contesto `/s7viewers` (cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o di librerie di visualizzatori di runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non mantiene sul server le versioni precedenti del visualizzatore secondario `includes`.
>
>
>Di conseguenza, il posizionamento di un riferimento diretto a qualsiasi JavaScript `include` secondario utilizzato dal visualizzatore nella pagina interrompe la funzionalità del visualizzatore in futuro, quando viene distribuita una nuova versione del prodotto.

1. Definizione del DIV del contenitore.

   Aggiungi un elemento DIV vuoto alla pagina in cui vuoi che venga visualizzato il visualizzatore. L’ID dell’elemento DIV deve essere definito perché questo ID viene passato successivamente all’API del visualizzatore.

   Il DIV segnaposto è un elemento posizionato, il che significa che la proprietà CSS `position` è impostata su `relative` o `absolute`.

   Di seguito è riportato un esempio di un elemento DIV segnaposto definito:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore.

   Questo visualizzatore visualizza le miniature quando si lavora con set con più elementi; nei sistemi desktop le miniature sono posizionate sotto la vista principale. Allo stesso tempo, il visualizzatore consente lo scambio della risorsa principale in fase di esecuzione utilizzando l&#39;API `setAsset()`. In qualità di sviluppatore, puoi controllare il modo in cui il visualizzatore gestisce l’area delle miniature nella parte inferiore quando la nuova risorsa ha un solo elemento. È possibile mantenere intatte le dimensioni del visualizzatore esterno e lasciare che la visualizzazione principale aumenti la sua altezza e occupi l’area delle miniature. In alternativa, è possibile mantenere statica la dimensione della visualizzazione principale e comprimere l’area di visualizzazione esterna, consentendo lo spostamento verso l’alto del contenuto della pagina web e l’utilizzo di spazio libero sullo schermo rimasto dalle miniature.

   Per mantenere intatti i limiti del visualizzatore esterno, definire la dimensione per la classe CSS di primo livello `.s7zoomviewer` in unità assolute. Il ridimensionamento in CSS può essere inserito direttamente nella pagina HTML. In alternativa, può essere inserito in un file CSS visualizzatore personalizzato, che viene successivamente assegnato a un record di predefinito visualizzatore in Dynamic Media Classic o passato esplicitamente utilizzando un comando di stile.

   Per ulteriori informazioni sullo stile del visualizzatore con CSS, vedere [Personalizzazione del visualizzatore zoom](../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-customizingviewer/c-html5-20-zoom-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0).

   Di seguito è riportato un esempio di definizione di una dimensione statica del visualizzatore esterno nella pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

<!-- You can see the behavior with a fixed outer viewer in the following example. Notice that when you switch between sets, the outer viewer size does not change: -->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=it](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-outer-area.html?lang=it)

-->

Per rendere statiche le dimensioni della visualizzazione principale, definire le dimensioni del visualizzatore in unità assolute per il componente SDK `Container` interno utilizzando il selettore CSS `.s7zoomviewer` `.s7container` o il modificatore `stagesize`.

Di seguito è riportato un esempio di definizione delle dimensioni del visualizzatore per il componente SDK `Container` interno in modo che l&#39;area di visualizzazione principale non cambi le dimensioni quando si cambia la risorsa:

```html {.line-numbers}
#s7viewer.s7zoomviewer .s7container { 
 width: 640px; 
 height: 480px; 
}
```

<!-- The following demo page shows the viewer behavior with a fixed main view size. Notice that when you switch between sets, the main view remains static and the web page content moves vertically. -->

<!--

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=it](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/zoom/ZoomViewer-fixed-main-view.html?lang=it)

-->

È possibile impostare il modificatore `stagesize` nel record del predefinito visualizzatore in Dynamic Media Classic. In alternativa, è possibile trasmetterlo in modo esplicito con il codice di inizializzazione del visualizzatore con la raccolta `params` o come chiamata API come descritto nella sezione Riferimento comando della presente Guida, come indicato di seguito:

```html {.line-numbers}
 zoomViewer.setParam("stagesize", 
"640,480");
```

Si consiglia un approccio basato su CSS, che viene utilizzato in questo esempio.

1. Creazione e inizializzazione del visualizzatore.

   Dopo aver completato i passaggi precedenti, si crea un&#39;istanza della classe `s7viewers.ZoomViewer`, si passano tutte le informazioni di configurazione al relativo costruttore e si chiama il metodo `init()` su un&#39;istanza del visualizzatore.

   Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto deve avere almeno il campo `containerId` che contiene il nome dell&#39;ID contenitore del visualizzatore e l&#39;oggetto JSON `params` nidificato con i parametri di configurazione supportati dal visualizzatore. In questo caso, l&#39;oggetto `params` deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sul corpo dell&#39;evento `onload()`.

   Allo stesso tempo, l’elemento contenitore non deve ancora necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza del visualizzatore, di passaggio delle opzioni di configurazione minime necessarie al costruttore e di chiamata al metodo `init()`. In questo esempio si presuppone che `zoomViewer` sia l&#39;istanza del visualizzatore, `s7viewer` sia il nome del segnaposto DIV, `http://s7d1.scene7.com/is/image/` sia l&#39;URL di Image Server e `Scene7SharedAssets/ImageSet-Views-Sample` sia la risorsa.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Il codice che segue è un esempio completo di una pagina web banale che incorpora il Visualizzatore video con una dimensione fissa:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7zoomviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var zoomViewer = new s7viewers.ZoomViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

## Design reattivo con altezza illimitata {#section-b9ca11a7e7aa4f74ab43244cbca37ae0}

Con l’incorporamento di un design reattivo, la pagina web in genere ha un layout flessibile che determina la dimensione di runtime del contenitore del visualizzatore `DIV`. Nell&#39;esempio seguente, si supponga che la pagina Web consenta al contenitore del visualizzatore `DIV` di occupare il 40% delle dimensioni della finestra del browser Web, senza limitazioni per l&#39;altezza. Il codice HTML della pagina Web sarà simile al seguente:

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

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del DIV del contenitore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell’incorporamento di dimensioni fisse. Aggiungere il DIV contenitore al DIV `"holder"` esistente. Il codice seguente è un esempio completo. Osserva come cambiano le dimensioni del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La pagina di esempi seguente illustra usi più reali dell’incorporamento di design responsive con altezza illimitata:

[Demo Live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

## Incorporamento di dimensioni flessibili con larghezza e altezza definite {#section-3674e6c032594441a6576b7fb1de6e64}

In presenza di un’incorporazione di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina web è diverso. Fornisce entrambe le dimensioni al DIV `"holder"` e lo centra nella finestra del browser. La pagina Web imposta inoltre le dimensioni dell&#39;elemento `HTML` e dell&#39;elemento `BODY` al 100%.

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

Il resto dei passaggi di incorporamento è identico ai passaggi utilizzati per l&#39;incorporamento di progetti reattivi con altezza illimitata. L’esempio risultante è il seguente:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
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
var zoomViewer = new s7viewers.ZoomViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

## Incorporazione tramite API basata su setter {#section-44e014925f24418b900696003855c0a9}

Invece di utilizzare l’inizializzazione basata su JSON, puoi utilizzare l’API basata su setter e il costruttore no-args. L&#39;utilizzo di questo costruttore API non accetta parametri e i parametri di configurazione sono specificati utilizzando i metodi API `setContainerId()`, `setParam()` e `setAsset()` con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con API basate su setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/ZoomViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7zoomviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var zoomViewer = new s7viewers.ZoomViewer(); 
zoomViewer.setContainerId("s7viewer"); 
zoomViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
zoomViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
zoomViewer.init(); 
</script> 
</body> 
</html> 
```
