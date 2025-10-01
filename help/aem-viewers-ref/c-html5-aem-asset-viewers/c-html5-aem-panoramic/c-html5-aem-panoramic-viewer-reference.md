---
title: Visualizzatore panoramico
description: Visualizzatore panoramico di HTML5 è un visualizzatore di immagini che visualizza un'immagine panoramica. Lo scopo di questo visualizzatore è quello di visualizzare un panorama sferico, noto anche come immagine equirettangolare. Supporta l'auto-panning e la panning con movimento giroscopico. È progettato per funzionare su desktop e dispositivi mobili. La modalità di visualizzazione realtà virtuale è disponibile sul supporto di dispositivi mobili.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: baf8015dc93cfa6be0a841243a7e3524f06f1639
workflow-type: tm+mt
source-wordcount: '1920'
ht-degree: 0%

---

# Panoramico{#panoramic}

Visualizzatore panoramico di HTML5 è un visualizzatore di immagini che visualizza un&#39;immagine panoramica. Lo scopo di questo visualizzatore è quello di visualizzare un panorama sferico, noto anche come immagine equirettangolare. Supporta l&#39;auto-panning e la panning con movimento giroscopico. È progettato per funzionare su desktop e dispositivi mobili. La modalità di visualizzazione realtà virtuale è disponibile sul supporto di dispositivi mobili.

Consulta [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Visualizzatore di tipo 514.

<!--
## Demo URL {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)
-->

## Utilizzo del visualizzatore panoramico {#section-f21ac23d3f6449ad9765588d69584772}

Visualizzatore panoramico di HTML5 rappresenta un file JavaScript principale e un insieme di file di supporto scaricati dal visualizzatore in fase di esecuzione. Il set di file di supporto è un singolo JavaScript che include tutti i componenti SDK del visualizzatore HTML5 utilizzati da questo particolare visualizzatore, risorse e CSS.
HTML5 Panoramic Viewer può essere utilizzato sia in modalità popup utilizzando una pagina HTML pronta per la produzione fornita con gli IS-Viewers che in modalità incorporata, dove è integrato nella pagina web di destinazione utilizzando l’API documentata.
La configurazione e l&#39;interfaccia sono simili a quelle degli altri visualizzatori HTML5. Tutte le operazioni di skin possono essere eseguite tramite CSS personalizzato.

Vedi [Riferimento al comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento al comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore panoramico di HTML5 {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

HTML5 Panoramic Viewer supporta la panoramica e la navigazione automatica mediante trascinamento o movimento giroscopico.

<table id="table_panoramic"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Navigazione </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Desktop </p> </td> 
   <td colname="col2"> <p>Spostamento automatico e trascinamento per spostarsi. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dispositivo touch </p> </td> 
   <td colname="col2"> <p>Per impostazione predefinita, trascina e scorri automaticamente per navigare. Navigare con movimento giroscopico in modalità di rendering VR (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta sia l&#39;input tocco che l&#39;input del mouse su dispositivi Windows con touch screen e mouse, tuttavia questo supporto è limitato solo ai browser Web Chrome, Internet Explorer 11 e Edge.
Il visualizzatore panoramico può riprodurre immagini panoramiche in modalità realtà virtuale (VR) specificando il modificatore vrrender. Quando il rendering è abilitato, un’immagine panoramica viene visualizzata in schermate divise. Un caso d’uso comune sarebbe quello di servire l’immagine in un telefono cellulare montato in una cuffia per realtà virtuale, fornendo immagini separate per ciascun occhio. L&#39;osservatore risponde al movimento giroscopico della testa e naviga attraverso l&#39;immagine.

## Incorporazione del visualizzatore panoramico HTML5 {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento. Selezionando tale collegamento si apre il visualizzatore in una finestra del browser separata. In altri casi, potrebbe essere necessario incorporare il visualizzatore nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout statico, essere &quot;reattiva&quot; e visualizzare in modo diverso su dispositivi diversi o per dimensioni diverse della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità operative principali: popup, incorporamento a dimensione fissa e incorporamento reattivo.

**Informazioni sulla modalità popup**

Nella modalità a comparsa, il visualizzatore viene aperto in una finestra o scheda del browser Web separata. Occupa l’intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l’orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando `window.open()` chiamata JavaScript, un elemento A HTML configurato correttamente o in qualsiasi altro modo appropriato.

Si consiglia di utilizzare una pagina HTML preconfigurata per la modalità di funzionamento popup. Si chiama [!DNL PanoramicViewer.html] e si trova nella sottocartella [!DNL html5/] della distribuzione IS-Viewers standard:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

La personalizzazione visiva può essere ottenuta applicando CSS personalizzati.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore nella nuova finestra:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento reattivo**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe già includere contenuto del cliente non correlato al visualizzatore. Il visualizzatore occupa normalmente solo una parte del patrimonio immobiliare della pagina web.

I casi d’uso principali sono le pagine web orientate per desktop o dispositivi tablet e le pagine web dinamiche che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando le dimensioni del visualizzatore non vengono modificate dopo il caricamento iniziale. Questo metodo è la scelta migliore per le pagine web con layout statico.

L’incorporamento reattivo presuppone che il visualizzatore debba ridimensionarsi in fase di esecuzione in risposta alla modifica delle dimensioni del DIV contenitore. Il caso d’uso più comune è l’aggiunta del visualizzatore a una pagina web che utilizza un layout flessibile.

In modalità reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il DIV contenitore. Se la pagina web imposta solo la larghezza dell’elemento DIV del contenitore, lasciando libera la sua altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questo metodo assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura sui lati. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout reattivi come Bootstrap, Foundation e simili.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza per il DIV contenitore del visualizzatore, il visualizzatore riempie tale area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuare le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l&#39;API del visualizzatore, assicurati di includere [!DNL PanoramicViewer.js]. Il file [!DNL PanoramicViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene fornito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
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


   Di seguito è riportato un esempio di un elemento DIV segnaposto definito:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica per il visualizzatore dichiarandolo per la classe CSS di primo livello `.s7panoramicviewer` in unità assolute oppure utilizzando il modificatore `stagesize`.

   Il ridimensionamento in CSS può essere inserito direttamente nella pagina HTML o in un file CSS visualizzatore personalizzato, che viene successivamente assegnato a un record di predefinito visualizzatore in AOD o passato esplicitamente utilizzando il comando style. Per ulteriori informazioni sullo stile del visualizzatore con CSS, consulta Personalizzazione del visualizzatore. Di seguito è riportato un esempio di definizione delle dimensioni statiche del visualizzatore nella pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   Il modificatore `stagesize` può essere passato esplicitamente con il codice di inizializzazione del visualizzatore con la raccolta params o come chiamata API come descritto nella sezione Riferimento comando, come segue:

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   L’approccio basato su CSS è consigliato e viene utilizzato in questo esempio.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, si crea un&#39;istanza della classe `s7viewers.PanoramicViewer`, si passano tutte le informazioni di configurazione al relativo costruttore e si chiama il metodo `init(`) su un&#39;istanza del visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto deve avere almeno un campo containerId che contiene il nome dell’ID contenitore del visualizzatore e un oggetto JSON parametri nidificati con parametri di configurazione supportati dal visualizzatore. In questo caso, l&#39;oggetto params deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro della risorsa. API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sul corpo dell&#39;evento `onload()`.

   Allo stesso tempo, l’elemento contenitore non deve ancora necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza del visualizzatore, passaggio al costruttore delle opzioni di configurazione minime necessarie e chiamata del metodo `init()`. In questo esempio si presuppone che `panoramicViewer` sia l&#39;istanza del visualizzatore, `s7viewer` il nome del segnaposto `DIV`, [!DNL http://s7d1.scene7.com/is/image/] l&#39;URL di Image Server e [!DNL Scene7SharedAssets/PanoramicImage-Sample] la risorsa.

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var panoramicViewer = new s7viewers.PanoramicViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
     "asset":"Scene7SharedAssets/PanoramicImage-Sample",
     "serverurl":"http://s7d1.scene7.com/is/image/"
   } 
   }).init(); 
   </script> 
   ```

   Il codice che segue è un esempio completo di una pagina Web banale che incorpora il visualizzatore panoramico con una dimensione fissa:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
    <head>
    <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
    <style type="text/css">
    #s7viewer.s7panoramicviewer {
        width: 1024px;
        height: 512px;
    }
    </style>
    </head>
    <body>
    <div id="s7viewer" style="position:relative"></div>
    <script type="text/javascript">
    var panoramicViewer = new s7viewers.PanoramicViewer({
        "containerId":"s7viewer",
    "params":{
        "asset":"Scene7SharedAssets/PanoramicImage-Sample",
        "serverurl":"http://s7d1.scene7.com/is/image/"
    }
    }).init();
    </script>
    </body>
    </html>
   ```

**Incorporamento di progettazione reattiva con altezza illimitata**

Con l’incorporamento reattivo, la pagina web solitamente dispone di un layout flessibile che determina le dimensioni in fase di esecuzione del DIV contenitore del visualizzatore. Ai fini di questo esempio, supponiamo che la pagina web consenta al contenitore DIV del visualizzatore di occupare l’80% delle dimensioni della finestra del browser web, lasciando libera la sua altezza. Il codice HTML della pagina web potrebbe essere simile al seguente:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<style type="text/css"> 
.holder {
    width: 80%;
}
</style>
</head>
<body>
<div class="holder"></div>
</body>
</html> 
```

L’aggiunta del visualizzatore a tale pagina è simile all’incorporamento di dimensioni fisse, con l’unica differenza che non è necessario definire esplicitamente le dimensioni del visualizzatore:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del DIV del contenitore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell’incorporamento di dimensioni fisse. Il DIV contenitore deve essere aggiunto al DIV &quot;contenitore&quot; esistente. Il codice seguente è un esempio completo: potresti vedere come cambiano le dimensioni del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
.holder {
    width: 80%;
}
</style>
</head>
<body>
<div class="holder">
<div id="s7viewer" style="position:relative"></div>
</div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
}
}).init();
</script>
</body>
</html>
```

La pagina di esempi seguente illustra un utilizzo più reale del design responsive con altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Percorso demo alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=it)

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

Il resto dei passaggi di incorporamento è identico all’incorporamento reattivo con altezza illimitata. L’esempio risultante è

```html {.line-numbers}
<!DOCTYPE html>
<html>
<head>
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
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
var panoramicViewer = new s7viewers.PanoramicViewer({
    "containerId":"s7viewer",
"params":{
    "asset":"Scene7SharedAssets/PanoramicImage-Sample",
    "serverurl":"http://s7d1.scene7.com/is/image/"
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
<script language="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/PanoramicViewer.js"></script>
<style type="text/css">
#s7viewer.s7panoramicviewer {
    width: 1024;
    height: 512;
}
</style>
</head>
<body>
<div id="s7viewer" style="position:relative"></div>
<script type="text/javascript">
var panoramicViewer = new s7viewers.PanoramicViewer();
panoramicViewer.setContainerId("s7viewer");
panoramicViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/");
panoramicViewer.setAsset("Scene7SharedAssets/PanoramicImage-Sample");
panoramicViewer.init();
</script>
</body>
</html>
```
