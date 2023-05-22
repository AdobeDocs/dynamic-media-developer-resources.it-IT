---
title: A comparsa
description: Visualizzatore a comparsa è un visualizzatore di immagini. Visualizza un’immagine statica con la versione ingrandita mostrata nella vista a comparsa attivata da un utente. Questo visualizzatore funziona con i set di immagini e la navigazione viene eseguita utilizzando i campioni. È progettato per funzionare su desktop e dispositivi mobili.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Flyout
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2065'
ht-degree: 0%

---

# A comparsa{#flyout}

Visualizzatore a comparsa è un visualizzatore di immagini. Visualizza un’immagine statica con la versione ingrandita mostrata nella vista a comparsa attivata da un utente. Questo visualizzatore funziona con i set di immagini e la navigazione viene eseguita utilizzando i campioni. È progettato per funzionare su desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Il tipo di visualizzatore è 504.

Consulta [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilizzo del visualizzatore a comparsa {#section-f21ac23d3f6449ad9765588d69584772}

Il visualizzatore a comparsa rappresenta un file JavaScript principale e un set di file di supporto (un singolo file JavaScript da includere con tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione

Il visualizzatore a comparsa è destinato solo all&#39;uso incorporato, il che significa che è integrato nella pagina web utilizzando l&#39;API documentata. Per il visualizzatore a comparsa non è disponibile alcuna pagina Web pronta per la produzione.

La configurazione e l’interfaccia sono simili a quelle degli altri visualizzatori. Per applicare lo skin, potete utilizzare CSS personalizzato.

Consulta [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore a comparsa {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore a comparsa supporta gesti single-touch e multi-touch comuni in altre applicazioni mobili.

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
   <td colname="col2"> <p> Attiva la visualizzazione a comparsa o cambia tra il livello di zoom primario e secondario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento orizzontale </p> </td> 
   <td colname="col2"> <p> Scorre l'elenco dei campioni nella barra dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento verticale </p> </td> 
   <td colname="col2"> <p>Se il movimento viene eseguito all'interno dell'area dei campioni, esegue uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta inoltre l&#39;input tocco e mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Consulta [Accessibilità della tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore a comparsa {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. La pagina web può avere un layout di pagina statico o utilizzare una progettazione reattiva che viene visualizzata in modo diverso su dispositivi diversi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta due modalità operative principali: l’incorporamento a dimensione fissa e l’incorporamento reattivo.

La modalità di incorporamento a dimensione fissa viene utilizzata quando le dimensioni del visualizzatore non vengono modificate dopo il caricamento iniziale. Questa opzione è consigliata per le pagine Web con layout di pagina statico.

La modalità di incorporamento della progettazione reattiva presuppone che il visualizzatore debba ridimensionarsi durante il runtime in risposta alla modifica delle dimensioni del suo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

Quando si utilizza la modalità di incorporamento della progettazione reattiva con il visualizzatore a comparsa, assicurarsi di specificare punti di interruzione espliciti per l&#39;immagine della visualizzazione principale utilizzando `imagereload` parametro. Idealmente, fai corrispondere i punti di interruzione con i punti di interruzione di larghezza del visualizzatore come richiesto dal CSS della pagina web.

In modalità di incorporamento di una progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui un contenitore di pagine web `DIV` è dimensionato. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando libera la sua altezza, l’utente sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa funzionalità significa che la risorsa si adatta perfettamente alla vista senza alcuna spaziatura sui lati. Questo caso d’uso particolare è il più comune per le pagine web che utilizzano framework di layout di progettazione reattivi come Bootstrap e Foundation.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, quindi il visualizzatore occupa solo tale area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio di caso d’uso è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporamento a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuare le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere `FlyoutViewer.js`. `FlyoutViewer.js` è compreso nei seguenti [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Dynamic Media di Adobe e viene fornito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Dynamic Media di Adobe in cui sono installati i visualizzatori IS.

Di seguito è riportato un percorso relativo:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Fai riferimento solo al visualizzatore principale JavaScript `include` sulla pagina. Non fare riferimento ad altri file JavaScript nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente all’SDK di HTML 5 `Utils.js` libreria caricata dal visualizzatore da `/s7viewers` percorso di contesto (il cosiddetto SDK consolidato) `include`). Il motivo è che l&#39;ubicazione di `Utils.js` o librerie di visualizzatori runtime simili sono completamente gestite dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. L’Adobe non mantiene le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del DIV del contenitore.

   Aggiungi un elemento DIV vuoto alla pagina in cui vuoi che venga visualizzato il visualizzatore. L’ID dell’elemento DIV deve essere definito, perché questo ID viene successivamente passato all’API visualizzatore.

   Il segnaposto DIV è un elemento posizionato, il che significa che `position` Proprietà CSS impostata su `relative` o `absolute`.

   È responsabilità della pagina web specificare il `z-index` per l&#39;elemento DIV segnaposto. In questo modo la parte a comparsa del visualizzatore viene visualizzata sopra gli altri elementi della pagina web.

   Di seguito è riportato un esempio di un elemento DIV segnaposto definito:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore.

   Questo visualizzatore visualizza le miniature quando si lavora con set di più elementi. Sui sistemi desktop, le miniature sono posizionate sotto la vista principale. Allo stesso tempo, il visualizzatore consente di scambiare la risorsa principale durante il runtime utilizzando `setAsset()` API. In qualità di sviluppatore, puoi controllare il modo in cui il visualizzatore gestisce l’area delle miniature nell’area inferiore quando la nuova risorsa ha un solo elemento. È possibile mantenere intatte le dimensioni del visualizzatore esterno e lasciare che la visualizzazione principale aumenti la sua altezza e occupi l’area delle miniature. In alternativa, è possibile mantenere statica la dimensione della visualizzazione principale e comprimere l’area di visualizzazione esterna, consentendo lo spostamento verso l’alto del contenuto della pagina web, e quindi utilizzare l’area immobiliare della pagina gratuita rimasta dalle miniature.

   Per mantenere intatti i limiti esterni del visualizzatore, definisci le dimensioni per `.s7flyoutviewer` classe CSS di primo livello in unità assolute. Il ridimensionamento in CSS può essere inserito direttamente nella pagina HTML o in un file CSS visualizzatore personalizzato, successivamente assegnato a un record predefinito visualizzatore in Dynamic Media Classic o passato esplicitamente utilizzando il comando style.

   Consulta [Personalizzazione del visualizzatore a comparsa](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione delle dimensioni statiche del visualizzatore esterno in una pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puoi vedere il comportamento con un’area visualizzatore esterna fissa nella seguente pagina di esempio. Tieni presente che quando passi da un set all’altro, le dimensioni del visualizzatore esterno non cambiano:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   Per rendere statiche le quote della vista principale, definite le dimensioni del visualizzatore in unità assolute per l&#39;area interna `Container` Componente SDK tramite `.s7flyoutviewer .s7container` Selettore CSS. Inoltre, devi sovrascrivere la dimensione fissa definita per `.s7flyoutviewer` classe CSS di primo livello nel CSS visualizzatore predefinito, impostandola su `auto`.

   Di seguito è riportato un esempio di definizione delle dimensioni del visualizzatore per l&#39;interno `Container` Componente SDK, in modo che l’area di visualizzazione principale non ne modifichi le dimensioni quando si cambia la risorsa:

   ```html {.line-numbers}
   #s7viewer.s7flyoutviewer { 
    width: auto; 
    height: auto; 
   }  
   #s7viewer.s7flyoutviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Nella pagina di esempio seguente viene illustrato il comportamento del visualizzatore con una dimensione di visualizzazione principale fissa. Quando passi da un set all’altro, la vista principale rimane statica e il contenuto della pagina web si sposta verticalmente:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   Inoltre, il CSS visualizzatore predefinito fornisce una dimensione fissa per l’area esterna preconfigurata.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, puoi creare un’istanza di `s7viewers.FlyoutViewer` classe, passa tutte le informazioni di configurazione al relativo costruttore e chiama `init()` su un&#39;istanza del visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto deve avere almeno `containerId` campo contenente il nome dell’ID contenitore del visualizzatore e nidificato `params` Oggetto JSON con parametri di configurazione supportati dal visualizzatore. In questo caso, il `params` l&#39;oggetto deve avere almeno l&#39;URL Image Server passato come `serverUrl` e la risorsa iniziale come `asset` parametro. API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il `init()` metodo immediatamente prima della chiusura `BODY` o sul corpo `onload()` evento.

   Allo stesso tempo, l’elemento contenitore non deve ancora necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando questa azione si verifica, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza del visualizzatore, mediante il passaggio delle opzioni di configurazione minime necessarie al costruttore e la chiamata al `init()` metodo. L’esempio presuppone `flyoutViewer` è l’istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; `http://s7d1.scene7.com/is/image/` è l’URL di Image Server; e `Scene7SharedAssets/ImageSet-Views-Sample` è la risorsa:

   ```html {.line-numbers}
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

   Il codice che segue è un esempio completo di una pagina web banale che incorpora il visualizzatore a comparsa con una dimensione fissa:

   ```html {.line-numbers}
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

## Design reattivo con altezza illimitata {#section-056cb574713c4d07be6d07cf3c598839}

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

L’aggiunta del visualizzatore a tale pagina è simile alla procedura per l’incorporamento a dimensione fissa. L’unica differenza consiste nel fatto che devi sovrascrivere il dimensionamento fisso del CSS visualizzatore predefinito con le dimensioni impostate in unità relative.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell’incorporamento di dimensioni fisse, con le tre eccezioni seguenti:

* aggiungi il contenitore `DIV` al &quot;detentore&quot; esistente `DIV`;
* aggiunto `imagereload` parametro con punti di interruzione espliciti;
* invece di impostare una dimensione fissa del visualizzatore utilizzando le unità assolute, utilizza gli stili CSS che impostano la larghezza e l&#39;altezza del visualizzatore al 100%, come illustrato di seguito:

```html {.line-numbers}
#s7viewer.s7flyoutviewer { 
 width: 100%; 
 height: 100%; 
}
```

Il codice seguente è un esempio completo. Osserva come cambiano le dimensioni del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```html {.line-numbers}
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

La pagina di esempi seguente illustra usi più reali dell’incorporamento di design responsive con altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Percorso demo alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Dimensione flessibile che incorpora con larghezza e altezza definite {#section-0a329016f9414d199039776645c693de}

In presenza di un’incorporazione di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina web è diverso. Fornisce entrambe le dimensioni al `"holder"` DIV e la centra nella finestra del browser. Inoltre, la pagina web imposta le dimensioni del `HTML` e `BODY` al 100%.

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

## Incorporazione tramite API basata su Set {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Invece di utilizzare l’inizializzazione basata su JSON, puoi utilizzare l’API basata su setter e il costruttore no-args. L’utilizzo di questo costruttore API non accetta parametri e i parametri di configurazione vengono specificati utilizzando `setContainerId()`, `setParam()`, e `setAsset()` metodi API, con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con API basate su setter:

```html {.line-numbers}
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
