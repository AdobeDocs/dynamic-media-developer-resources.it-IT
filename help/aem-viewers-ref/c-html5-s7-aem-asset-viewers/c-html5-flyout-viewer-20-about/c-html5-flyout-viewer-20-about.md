---
description: Il visualizzatore a comparsa è un visualizzatore di immagini. Viene visualizzata un’immagine statica con la versione ingrandita mostrata nella visualizzazione a comparsa attivata da un utente. Questo visualizzatore funziona con i set di immagini e la navigazione viene effettuata utilizzando i campioni. È progettato per funzionare su computer desktop e dispositivi mobili.
keywords: responsive
seo-description: Il visualizzatore a comparsa è un visualizzatore di immagini. Viene visualizzata un’immagine statica con la versione ingrandita mostrata nella visualizzazione a comparsa attivata da un utente. Questo visualizzatore funziona con i set di immagini e la navigazione viene effettuata utilizzando i campioni. È progettato per funzionare su computer desktop e dispositivi mobili.
seo-title: A comparsa
solution: Experience Manager
title: A comparsa
topic: Dynamic media
uuid: 588e1baa-4165-4aec-8fbe-1a916c0f409f
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2130'
ht-degree: 0%

---


# A comparsa{#flyout}

Il visualizzatore a comparsa è un visualizzatore di immagini. Viene visualizzata un’immagine statica con la versione ingrandita mostrata nella visualizzazione a comparsa attivata da un utente. Questo visualizzatore funziona con i set di immagini e la navigazione viene effettuata utilizzando i campioni. È progettato per funzionare su computer desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Il tipo di visualizzatore è 504.

Consultate Requisiti di [sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilizzo del visualizzatore a comparsa {#section-f21ac23d3f6449ad9765588d69584772}

Il visualizzatore a comparsa rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione

Il visualizzatore a comparsa è destinato solo all’uso incorporato, il che significa che è integrato nella pagina Web tramite l’API documentata. Per il visualizzatore a comparsa non è disponibile alcuna pagina Web pronta per la produzione.

La configurazione e l’interfaccia sono simili a quelle degli altri visualizzatori. Potete utilizzare un CSS personalizzato per applicare l&#39;interfaccia.

Consultate Riferimento [comando comune a tutti i visualizzatori - Attributi](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) di configurazione e Riferimento [comando comuni a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore a comparsa {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore a comparsa supporta i gesti touch singola e multi-touch comuni in altre applicazioni mobili.

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
   <td colname="col2"> <p> Attiva la visualizzazione a comparsa o le modifiche tra il livello di zoom principale e secondario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento o scorrimento orizzontale </p> </td> 
   <td colname="col2"> <p> Consente di scorrere l’elenco dei campioni nella barra dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento verticale </p> </td> 
   <td colname="col2"> <p>Se il gesto viene eseguito all’interno dell’area dei campioni, viene eseguito uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta inoltre l&#39;input touch e l&#39;input del mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser Web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile tramite tastiera.

Consultate Accesso [e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861)da tastiera.

## Incorporazione del visualizzatore a comparsa {#section-6bb5d3c502544ad18a58eafe12a13435}

Diverse pagine Web hanno esigenze diverse per il comportamento del visualizzatore. La pagina Web può avere un layout di pagina statico oppure utilizzare un design reattivo che viene visualizzato in modo diverso su diversi dispositivi o per diverse dimensioni di finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta due modalità di funzionamento principali: incorporazione a dimensione fissa e incorporazione reattiva del design.

La modalità di incorporazione a dimensione fissa viene utilizzata quando il visualizzatore non ne modifica la dimensione dopo il caricamento iniziale. Questa opzione è ideale per le pagine Web con layout di pagina statico.

La modalità di incorporazione della progettazione reattiva presuppone che il visualizzatore debba ridimensionare durante il runtime in seguito alla modifica delle dimensioni del contenitore `DIV`. L’esempio più comune è l’aggiunta di un visualizzatore a una pagina Web con layout di pagina flessibile.

Quando usate la modalità di incorporamento reattiva del design con il visualizzatore a comparsa, accertatevi di specificare punti di interruzione espliciti per l’immagine della vista principale utilizzando il `imagereload` parametro. Idealmente, potete far corrispondere i punti di interruzione con i punti di interruzione della larghezza del visualizzatore come indicato dalla pagina Web CSS.

In modalità di incorporazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui una pagina Web ridimensiona il proprio contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente l’altezza in base alle proporzioni della risorsa utilizzata. Ciò significa che la risorsa si adatta perfettamente alla vista senza riempimenti laterali. Questo caso di utilizzo è il più comune per le pagine Web che utilizzano framework di layout reattivi come Bootstrap, Foundation e così via.

In caso contrario, se la pagina Web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore, il visualizzatore riempie solo tale area e `DIV`segue le dimensioni fornite dal layout della pagina Web. Un buon esempio di utilizzo consiste nell’incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser Web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuate le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell&#39;intestazione HTML. Prima di poter utilizzare l&#39;API del visualizzatore, accertatevi di includerla `FlyoutViewer.js`. `FlyoutViewer.js` si trova nella seguente [!DNL html5/js/] sottocartella della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Potete usare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Scene7 e distribuito dallo stesso dominio. In caso contrario, specificate un percorso completo per uno dei server Adobe Scene7 in cui sono installati i visualizzatori IS.

Un percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>È consigliabile fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non dovete fare riferimento ad altri file JavaScript nel codice della pagina Web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fate riferimento direttamente alla libreria SDK HTML5 caricata dal `Utils.js` visualizzatore dal percorso `/s7viewers` contestuale (il cosiddetto SDK consolidato `include`). Il motivo è che la posizione delle librerie di visualizzatori runtime `Utils.js` o simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva `includes` sul server le versioni precedenti del visualizzatore secondario.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi codice JavaScript secondario utilizzato `include` dal visualizzatore sulla pagina si interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione di prodotto.

1. Definizione del contenitore DIV.

   Aggiungete un elemento DIV vuoto alla pagina in cui desiderate visualizzare il visualizzatore. L&#39;ID dell&#39;elemento DIV deve essere definito perché in seguito l&#39;ID viene passato all&#39;API del visualizzatore.

   Il segnaposto DIV è un elemento posizionato, il che significa che la proprietà `position` CSS è impostata su `relative` o `absolute`.

   È responsabilità della pagina Web specificare l&#39;elemento DIV `z-index` del segnaposto. In questo modo la porzione a comparsa del visualizzatore viene visualizzata sopra agli altri elementi della pagina Web.

   Esempio di un elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore.

   Questo visualizzatore visualizza le miniature quando si utilizzano i set di più elementi. Sui sistemi desktop, le miniature vengono posizionate sotto la vista principale. Allo stesso tempo, il visualizzatore consente lo scambio della risorsa principale durante l&#39;esecuzione tramite `setAsset()` API. In qualità di sviluppatore, potete controllare in che modo il visualizzatore gestisce l’area delle miniature nell’area inferiore quando la nuova risorsa dispone di un solo elemento. È possibile mantenere intatte le dimensioni del visualizzatore esterno e lasciare che la vista principale ne aumenti l’altezza e occupi l’area delle miniature. In alternativa, potete mantenere statiche le dimensioni di visualizzazione principale e comprimere l’area del visualizzatore esterno, consentendo al contenuto della pagina Web di spostarsi verso l’alto, quindi utilizzare l’area reale della pagina gratuita a sinistra dalle miniature.

   Per mantenere intatti i limiti del visualizzatore esterno, definite la dimensione della classe CSS di livello `.s7flyoutviewer` principale in unità assolute. Il ridimensionamento in CSS può essere inserito direttamente nella pagina HTML o in un file CSS del visualizzatore personalizzato, che verrà successivamente assegnato a un record di predefinito per visualizzatori in Scene7 Publishing System, oppure trasmesso in modo esplicito tramite il comando stile.

   Consultate [Personalizzazione del visualizzatore](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) a comparsa per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione delle dimensioni statiche del visualizzatore esterno in una pagina HTML:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Potete visualizzare il comportamento con un’area fissa del visualizzatore esterno sulla pagina di esempio seguente. Tenete presente che quando passate da un set all’altro, le dimensioni del visualizzatore esterno non cambiano:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-outer-area.html)

   Per rendere statiche le dimensioni di visualizzazione principali, definite le dimensioni del visualizzatore in unità assolute per il componente `Container` SDK interno utilizzando il selettore `.s7flyoutviewer .s7container` CSS. Inoltre, potete ignorare la dimensione fissa definita per la classe CSS di livello `.s7flyoutviewer` principale nel CSS del visualizzatore predefinito, impostandola su `auto`.

   Di seguito è riportato un esempio di definizione delle dimensioni del visualizzatore per il componente `Container` SDK interno, in modo che l’area di visualizzazione principale non cambi le dimensioni quando si passa da una risorsa all’altra:

   ```
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La pagina di esempio seguente mostra il comportamento del visualizzatore con una dimensione di visualizzazione principale fissa. Quando passate da un set all’altro, la vista principale rimane statica e il contenuto della pagina Web si sposta in verticale:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/FlyoutViewer-fixed-main-view.html)

   Inoltre, il CSS predefinito per visualizzatori offre una dimensione fissa per l&#39;area esterna out-of-the-box.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi descritti qui sopra, potete creare un&#39;istanza della `s7viewers.FlyoutViewer` classe, trasmettere tutte le informazioni di configurazione al relativo costruttore e chiamare `init()` il metodo su un&#39;istanza di visualizzatore. Le informazioni di configurazione vengono trasmesse al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere il `containerId` `params` campo che contiene il nome dell&#39;ID del contenitore del visualizzatore e l&#39;oggetto JSON nidificato con i parametri di configurazione supportati dal visualizzatore. In questo caso, l’ `params` oggetto deve avere almeno l’URL Image Server passato come `serverUrl` proprietà e la risorsa iniziale come `asset` parametro. L&#39;API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore del visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser ritardano la creazione del DOM fino alla fine della pagina Web. Per garantire la massima compatibilità, chiamate il `init()` metodo immediatamente prima del `BODY` tag di chiusura o dell’ `onload()` evento body.

   Allo stesso tempo, l&#39;elemento contenitore non deve necessariamente far parte del layout della pagina Web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` lo stile assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del `init()` metodo. L’esempio presuppone che `flyoutViewer` sia l’istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; `http://s7d1.scene7.com/is/image/` è l’URL del server immagini; ed `Scene7SharedAssets/ImageSet-Views-Sample` è la risorsa:

   ```
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Il codice seguente è un esempio completo di una pagina Web banale che incorpora il visualizzatore a comparsa con una dimensione fissa:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative;z-index:1;"></div> 
   <script type="text/javascript"> 
   var flyoutViewer = new s7viewers.FlyoutViewer({ 
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

## Incorporazione responsive con altezza illimitata {#section-056cb574713c4d07be6d07cf3c598839}

Con l’incorporazione reattiva della progettazione, la pagina Web dispone in genere di un layout flessibile che specifica le dimensioni runtime del contenitore del visualizzatore `DIV`. Ad esempio, si supponga che la pagina Web consenta al contenitore del visualizzatore `DIV` di occupare il 40% delle dimensioni della finestra del browser Web, lasciando invariata l’altezza. Il codice HTML della pagina Web sarà simile al seguente:

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

L’aggiunta del visualizzatore a tale pagina è simile alla procedura per l’incorporamento a dimensione fissa. L’unica differenza è che dovete ignorare il ridimensionamento fisso dal CSS del visualizzatore predefinito con la dimensione impostata in unità relative.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi indicati sopra sono identici a quelli con l&#39;incorporamento a dimensione fissa con le tre eccezioni seguenti:

* aggiungere il contenitore `DIV` al &quot;titolare&quot; esistente `DIV`;
* aggiunto `imagereload` parametro con punti di interruzione espliciti;
* invece di impostare una dimensione fissa per il visualizzatore usando unità assolute, usate CSS che imposta la larghezza e l’altezza del visualizzatore su 100%, come segue:

```
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
.holder { 
 width: 40%; 
} 
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La pagina degli esempi seguente illustra gli usi più reali dell’incorporamento reattivo di design con altezza illimitata:

[Live Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Incorporazione di dimensioni flessibili con larghezza e altezza definite {#section-0a329016f9414d199039776645c693de}

In caso di incorporamento di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina Web è diverso. Fornisce entrambe le dimensioni al `"holder"` DIV e lo centra nella finestra del browser. Inoltre, la pagina Web imposta la dimensione dell’elemento `HTML` e `BODY` dell’elemento su 100%.

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

Gli altri passaggi di incorporamento sono identici ai passaggi utilizzati per incorporare design reattivi con altezza illimitata. L’esempio risultante è il seguente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
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
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
} 
</style> 
</head> 
<body> 
<div class="holder"> 
<div id="s7viewer" style="position:relative;z-index:1"></div> 
</div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/ImageSet-Views-Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "imagereload":"1,breakpoint,200;400;800;1600" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporazione tramite l&#39;API basata su Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L&#39;utilizzo di questo costruttore di API non accetta parametri e i parametri di configurazione vengono specificati utilizzando `setContainerId()`, `setParam()`e metodi `setAsset()` API, con chiamate JavaScript separate.

L&#39;esempio seguente illustra l&#39;utilizzo dell&#39;incorporamento a dimensione fissa con l&#39;API basata su setter:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/FlyoutViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7flyoutviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head><body> 
<div id="s7viewer" style="position:relative;z-index:1;"></div> 
<script type="text/javascript"> 
var flyoutViewer = new s7viewers.FlyoutViewer(); 
flyoutViewer.setContainerId("s7viewer"); 
flyoutViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
flyoutViewer.setAsset("Scene7SharedAssets/ImageSet-Views-Sample"); 
flyoutViewer.init(); 
</script> 
</body> 
</html>
```

