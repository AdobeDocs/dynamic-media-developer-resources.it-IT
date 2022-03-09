---
title: Visualizzatore panoramico
description: HTML5 Panoramic Viewer è un visualizzatore di immagini che visualizza un’immagine panoramica. Lo scopo di questo visualizzatore è quello di visualizzare un panorama sferico, noto anche come immagine equirettangolare. Supporta la panoramica e la panoramica automatica tramite movimento giroscopico. È progettato per funzionare su desktop e dispositivi mobili. La modalità di visualizzazione della realtà virtuale è disponibile sul supporto dei dispositivi mobili.
keywords: reattivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1953'
ht-degree: 0%

---

# Panoramico{#panoramic}

HTML5 Panoramic Viewer è un visualizzatore di immagini che visualizza un’immagine panoramica. Lo scopo di questo visualizzatore è quello di visualizzare un panorama sferico, noto anche come immagine equirettangolare. Supporta la panoramica e la panoramica automatica tramite movimento giroscopico. È progettato per funzionare su desktop e dispositivi mobili. La modalità di visualizzazione della realtà virtuale è disponibile sul supporto dei dispositivi mobili.

Vedi [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).


Tipo di visualizzatore 514.

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample](http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample)

## Utilizzo del visualizzatore panoramico {#section-f21ac23d3f6449ad9765588d69584772}

HTML5 Panoramic Viewer rappresenta un file JavaScript principale e un set di file helper scaricati dal visualizzatore in fase di esecuzione. L’insieme di file helper è un’unica inclusione JavaScript con tutti i componenti SDK per visualizzatori HTML5 utilizzati da questo particolare visualizzatore, risorse, CSS.
HTML5 Panoramic Viewer può essere utilizzato sia in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con IS-Viewers o in modalità incorporata, dove viene integrato nella pagina web di destinazione utilizzando un’API documentata.
La configurazione e lo skin sono simili a quelli degli altri visualizzatori HTML5. Tutta la skin può essere ottenuta tramite CSS personalizzati.

Vedi [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con HTML5 Panoramic Viewer {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

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
   <td colname="col2"> <p>Panning automatica e trascinamento per la navigazione. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Dispositivo touch </p> </td> 
   <td colname="col2"> <p>Per impostazione predefinita, effettua il panning automatico e trascina per navigare. Navigare per movimento giroscopico in modalità di rendering VR (vrrender=true).
 </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta sia l’input touch che l’input del mouse su dispositivi Windows con touch screen e mouse, tuttavia questo supporto è limitato solo ai browser Web Chrome, Internet Explorer 11 e Edge.
Il visualizzatore panoramico può eseguire il rendering delle immagini panoramiche in modalità Virtual Reality (VR) specificando il modificatore vrrender. Quando il rendering è abilitato, un&#39;immagine panoramica viene visualizzata in schermate suddivise. Un caso d&#39;uso comune sarebbe quello di servire l&#39;immagine in un cellulare montato in una cuffia di realtà virtuale, fornendo immagini separate per ogni occhio. Lo spettatore risponde al movimento giroscopico della testa e naviga attraverso l&#39;immagine.

## Incorporazione del visualizzatore panoramico HTML5 {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento. Selezionando quel collegamento, il visualizzatore viene aperto in una finestra separata del browser. In altri casi, potrebbe essere necessario incorporare il visualizzatore nella pagina di hosting. In quest&#39;ultimo caso, la pagina web può avere layout statico o essere &quot;reattiva&quot; e visualizzata in modo diverso su dispositivi diversi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: a comparsa, incorporazione a dimensione fissa e incorporazione reattiva.

**Informazioni sulla modalità a comparsa**

Nella modalità a comparsa, il visualizzatore viene aperto in una finestra o scheda separata del browser Web. Prende l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l&#39;orientamento del dispositivo venga modificato.

Questa modalità è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` Chiamata JavaScript, configurata correttamente Un elemento HTML o qualsiasi altro modo appropriato.

Si consiglia di utilizzare una pagina HTML predefinita per la modalità di funzionamento a comparsa. Si chiama [!DNL PanoramicViewer.html] e si trova sotto la [!DNL html5/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/PanoramicViewer.html]

È possibile personalizzare visivamente l’applicazione di CSS personalizzati.

Ecco un esempio di codice HTML che apre il visualizzatore nella nuova finestra:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/PanoramicViewer.html?asset=Scene7SharedAssets/PanoramicImage-Sample" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento reattiva**

Nella modalità incorporata il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe avere già alcuni contenuti del cliente non correlati al visualizzatore. Il visualizzatore normalmente occupa solo una parte del patrimonio immobiliare della pagina web.

I casi d’uso principali sono le pagine web orientate ai desktop o ai dispositivi tablet, nonché le pagine web reattive che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporazione a dimensione fissa viene utilizzata quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questo metodo è la scelta migliore per le pagine web con layout statico.

L’incorporazione reattiva presuppone che il visualizzatore debba ridimensionare in fase di esecuzione in risposta alla modifica delle dimensioni del suo contenitore DIV. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout flessibile.

In modalità reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il proprio DIV contenitore. Se la pagina web imposta solo la larghezza del contenitore DIV, lasciando senza limitazioni l’altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questo metodo assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura laterale. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout reattivo come Bootstrap, Foundation e così via.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza per il contenitore DIV del visualizzatore, quest’ultimo riempie quell’area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio è quello di incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina web, effettua le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione di HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL PanoramicViewer.js]. La [!DNL PanoramicViewer.js] si trova sotto [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/PanoramicViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene servito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/PanoramicViewer.js"></script>
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


   Di seguito è riportato un esempio di elemento DIV segnaposto definito:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore

   Puoi impostare la dimensione statica del visualizzatore dichiarandola per `.s7panoramicviewer` classe CSS di primo livello in unità assolute o utilizzando il modificatore `stagesize`.

   Le dimensioni in CSS possono essere posizionate direttamente sulla pagina HTML o in un file CSS per visualizzatori personalizzati, che viene successivamente assegnato a un record predefinito visualizzatore in AOD o passato esplicitamente utilizzando il comando stile. Per ulteriori informazioni sullo stile del visualizzatore con CSS, consulta Personalizzazione della sezione Visualizzatore . Di seguito è riportato un esempio di definizione della dimensione statica del visualizzatore nella pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7panoramicviewer {
     width: 1024px;
     height: 512px;
   }
   ```

   `stagesize` Il modificatore può essere passato esplicitamente con il codice di inizializzazione del visualizzatore con l&#39;insieme params o come chiamata API come descritto nella sezione Riferimento comandi , come segue:

   ```html {.line-numbers}
   panoramicViewer.setParam("stagesize", "512,256");
   ```

   L’approccio basato su CSS è consigliato e viene utilizzato in questo esempio.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza di `s7viewers.PanoramicViewer` , passare tutte le informazioni di configurazione al relativo costruttore e chiamare `init(`) su un’istanza di visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere un campo containerId che contiene il nome dell’ID del contenitore del visualizzatore e un oggetto JSON di parametri nidificati con i parametri di configurazione supportati dal visualizzatore. In questo caso l&#39;oggetto params deve avere almeno l&#39;URL Image Server passato come `serverUrl` e la risorsa iniziale come parametro della risorsa. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il `init()` metodo immediatamente prima della chiusura `BODY` o sul corpo `onload()` evento.

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del `init()` metodo . Questo esempio presuppone `panoramicViewer` è l’istanza del visualizzatore, `s7viewer` è il nome del segnaposto `DIV`, [!DNL http://s7d1.scene7.com/is/image/] è l’URL di Image Server e [!DNL Scene7SharedAssets/PanoramicImage-Sample] è la risorsa.

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

   Il codice seguente è un esempio completo di una pagina web banale che incorpora il visualizzatore panoramico con dimensioni fisse:

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

**Incorporazione di design reattivo con altezza illimitata**

Con l’incorporazione reattiva, la pagina web dispone normalmente di un layout flessibile che determina la dimensione in fase di esecuzione del DIV contenitore del visualizzatore. Ai fini di questo esempio supponiamo che la pagina web consenta al contenitore del visualizzatore DIV di prendere l’80% delle dimensioni della finestra del browser web, lasciando senza restrizioni la sua altezza. Il codice HTML della pagina web potrebbe essere simile al seguente:

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

L’aggiunta del visualizzatore a tale pagina è simile all’incorporamento a dimensione fissa, con l’unica differenza che non è necessario definire esplicitamente la dimensione del visualizzatore:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell&#39;incorporazione con dimensione fissa. Il contenitore DIV deve essere aggiunto al DIV &quot;titolare&quot; esistente. Il codice seguente è un esempio completo: puoi vedere come cambia la dimensione del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

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

La pagina degli esempi seguenti illustra l’utilizzo più reale di elementi di design reattivi con altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Posizione demo alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

**Incorporazione responsive con larghezza e altezza definite**

Se è presente un incorporamento dinamico con larghezza e altezza definite, lo stile della pagina web è diverso; fornisce entrambe le dimensioni al &quot;titolare&quot; `DIV` e centralo nella finestra del browser. Inoltre, la pagina web imposta le dimensioni del `HTML` e `BODY` al 100%:

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

Gli altri passaggi di incorporamento sono identici a quelli di incorporamento reattivo con altezza illimitata. L&#39;esempio risultante è

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

**Incorporazione tramite API basate su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. Con tale API, il costruttore non accetta alcun parametro e i parametri di configurazione vengono specificati utilizzando `setContainerId()`, `setParam()`e `setAsset()` Metodi API con chiamate JavaScript separate.

L’esempio seguente illustra l’incorporazione di dimensioni fisse con API basata su setter:

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
