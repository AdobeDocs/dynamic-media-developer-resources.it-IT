---
description: Il visualizzatore a comparsa è un visualizzatore di immagini. Mostra un’immagine statica con la versione ingrandita mostrata nella visualizzazione a comparsa che un utente attiva. Questo visualizzatore funziona con i set di immagini e la navigazione viene eseguita utilizzando i campioni. È progettato per funzionare su desktop e dispositivi mobili.
keywords: reattivo
solution: Experience Manager
title: A comparsa
feature: Dynamic Media Classic,Visualizzatori,SDK/API,A comparsa
role: Developer,User
exl-id: 9b60330f-5348-431d-9682-cf97aace3679
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2084'
ht-degree: 0%

---

# A comparsa{#flyout}

Il visualizzatore a comparsa è un visualizzatore di immagini. Mostra un’immagine statica con la versione ingrandita mostrata nella visualizzazione a comparsa che un utente attiva. Questo visualizzatore funziona con i set di immagini e la navigazione viene eseguita utilizzando i campioni. È progettato per funzionare su desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Il tipo di visualizzatore è 504.

Consulta [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample](https://s7d9.scene7.com/s7viewers/html5/FlyoutViewer.html?asset=Scene7SharedAssets/ImageSet-Views-Sample)

## Utilizzo del visualizzatore a comparsa {#section-f21ac23d3f6449ad9765588d69584772}

Il visualizzatore a comparsa rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione

Il visualizzatore a comparsa è destinato solo all’uso integrato, il che significa che è integrato nella pagina web utilizzando un’API documentata. Non è disponibile alcuna pagina web pronta per la produzione per il visualizzatore a comparsa.

La configurazione e lo skin sono simili a quelli degli altri visualizzatori. Puoi utilizzare CSS personalizzati per applicare la skin.

Consulta [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento ai comandi comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore a comparsa {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore a comparsa supporta gesti touch singoli e touch comuni ad altre applicazioni mobili.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Singolo tocco </p> </td> 
   <td colname="col2"> <p> Attiva la visualizzazione a comparsa o le modifiche tra il livello di zoom primario e secondario. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento orizzontale o rapido </p> </td> 
   <td colname="col2"> <p> Scorre l’elenco dei campioni nella barra dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento verticale </p> </td> 
   <td colname="col2"> <p>Se il movimento viene eseguito all’interno dell’area dei campioni, viene eseguito uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta anche l’input touch e il mouse su dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Consulta [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore a comparsa {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. La pagina web può avere layout di pagina statico o utilizzare design reattivo che viene visualizzato in modo diverso su diversi dispositivi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta due modalità di funzionamento principali: incorporazione a dimensione fissa e incorporazione responsive del design.

La modalità di incorporamento a dimensione fissa viene utilizzata quando il visualizzatore non modifica le dimensioni dopo il caricamento iniziale. Questa opzione è ideale per le pagine web con layout di pagina statico.

La modalità di incorporamento della progettazione reattiva presuppone che il visualizzatore debba ridimensionare durante il runtime in risposta alla modifica delle dimensioni del contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

Quando utilizzi la modalità di incorporamento della progettazione reattiva con il visualizzatore a comparsa, accertati di specificare punti di interruzione espliciti per l’immagine della visualizzazione principale utilizzando il parametro `imagereload` . Se lo desideri, abbina i tuoi punti di interruzione con i punti di interruzione della larghezza del visualizzatore come indicato dal CSS della pagina web.

In modalità di incorporamento della progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui una pagina web ridimensiona il proprio contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Ciò significa che la risorsa si adatta perfettamente alla vista senza alcuna spaziatura laterale. Questo caso d’uso specifico è il più comune per le pagine web che utilizzano framework di layout di progettazione reattiva come Bootstrap, Foundation e così via.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza del contenitore del visualizzatore `DIV`, il visualizzatore compila solo quell’area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio di utilizzo è quello di incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina web, effettua le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere `FlyoutViewer.js`. `FlyoutViewer.js` si trova nella seguente  [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/FlyoutViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Dynamic Media di Adobe e viene servito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Dynamic Media di Adobe in cui sono installati i visualizzatori IS.

Un percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/FlyoutViewer.js"></script>
```

>[!NOTE]
>
>Dovresti fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non devi fare riferimento a file JavaScript aggiuntivi nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente alla libreria HTML5 SDK `Utils.js` caricata dal visualizzatore dal percorso contestuale `/s7viewers` (cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o librerie di visualizzatori runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, l’inserimento di un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore DIV.

   Aggiungi un elemento DIV vuoto alla pagina in cui desideri che appaia il visualizzatore. L’ID dell’elemento DIV deve essere definito, perché viene successivamente passato all’API del visualizzatore.

   Il segnaposto DIV è un elemento posizionato, il che significa che la proprietà CSS `position` è impostata su `relative` o `absolute`.

   È responsabilità della pagina web specificare il `z-index` corretto per l’elemento DIV segnaposto. In questo modo la porzione a comparsa del visualizzatore viene visualizzata sopra gli altri elementi della pagina web.

   Di seguito è riportato un esempio di elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative;z-index:1"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore.

   Questo visualizzatore visualizza le miniature quando si lavora con set di più elementi. Nei sistemi desktop, le miniature vengono posizionate sotto la vista principale. Allo stesso tempo, il visualizzatore consente lo scambio della risorsa principale durante il runtime utilizzando l’API `setAsset()`. In qualità di sviluppatore, puoi controllare come il visualizzatore gestisce l’area delle miniature nell’area inferiore, quando la nuova risorsa ha un solo elemento. È possibile mantenere intatta la dimensione del visualizzatore esterno e lasciare che la vista principale aumenti la sua altezza e occupare l&#39;area delle miniature. In alternativa, è possibile mantenere statiche le dimensioni della visualizzazione principale e comprimere l’area del visualizzatore esterno, consentendo in tal modo al contenuto della pagina web di spostarsi verso l’alto, e quindi utilizzare l’area immobiliare della pagina gratuita lasciata dalle miniature.

   Per mantenere intatti i limiti del visualizzatore esterno, definisci le dimensioni della classe CSS di livello superiore `.s7flyoutviewer` in unità assolute. Le dimensioni in CSS possono essere posizionate direttamente sulla pagina HTML o in un file CSS per visualizzatori personalizzati, che viene successivamente assegnato a un record predefinito per visualizzatori in Dynamic Media Classic, o passato esplicitamente utilizzando il comando stile.

   Per ulteriori informazioni sullo stile del visualizzatore con CSS, consulta [Personalizzazione del visualizzatore a comparsa](../../c-html5-s7-aem-asset-viewers/c-html5-flyout-viewer-20-about/c-html5-flyout-viewer-20-customizingviewer/c-html5-flyout-viewer-20-customizingviewer.md#concept-82f8c71adbe54680a0c2f83f81e5f451) .

   Di seguito è riportato un esempio di definizione delle dimensioni statiche del visualizzatore esterno in una pagina HTML:

   ```
   #s7viewer.s7flyoutviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puoi vedere il comportamento con un’area di visualizzazione esterna fissa nella pagina di esempio seguente. Quando si passa da un set all’altro, le dimensioni del visualizzatore esterno non cambiano:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-outer-area.html)

   Per rendere statiche le dimensioni di visualizzazione principali, definisci le dimensioni del visualizzatore in unità assolute per il componente SDK interno `Container` utilizzando il selettore CSS `.s7flyoutviewer .s7container`. Inoltre, è necessario ignorare la dimensione fissa definita per la classe CSS di livello principale `.s7flyoutviewer` nel CSS del visualizzatore predefinito, impostandola su `auto`.

   Di seguito è riportato un esempio di definizione delle dimensioni del visualizzatore per il componente interno `Container` SDK in modo che l’area di visualizzazione principale non cambi le dimensioni quando si cambia la risorsa:

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

   La pagina di esempio seguente mostra il comportamento del visualizzatore con una dimensione di visualizzazione principale fissa. Quando si passa da un set all’altro, la visualizzazione principale rimane statica e il contenuto della pagina web si sposta in verticale:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/flyout/FlyoutViewer-fixed-main-view.html)

   Inoltre, il CSS del visualizzatore predefinito fornisce una dimensione fissa per l’area esterna preconfigurata.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza della classe `s7viewers.FlyoutViewer`, passa tutte le informazioni di configurazione al relativo costruttore e chiama il metodo `init()` su un’istanza di visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere il campo `containerId` che contiene il nome dell’ID del contenitore del visualizzatore e l’oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore. In questo caso, l’oggetto `params` deve avere almeno l’URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()` .

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web per ora. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del metodo `init()` . L’esempio presuppone che `flyoutViewer` sia l’istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; `http://s7d1.scene7.com/is/image/` è l&#39;URL di Image Server; e `Scene7SharedAssets/ImageSet-Views-Sample` è la risorsa:

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

   Il codice seguente è un esempio completo di una pagina web banale che incorpora il visualizzatore a comparsa con dimensioni fisse:

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

## Incorporazione di design reattivo con altezza illimitata {#section-056cb574713c4d07be6d07cf3c598839}

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

L’aggiunta del visualizzatore a una pagina di questo tipo è simile alla procedura per l’incorporazione a dimensione fissa. L’unica differenza è che devi sovrascrivere il ridimensionamento fisso dal CSS del visualizzatore predefinito con la dimensione impostata in unità relative.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell&#39;incorporazione della dimensione fissa con le seguenti tre eccezioni:

* aggiungere il contenitore `DIV` al &quot;titolare&quot; esistente `DIV`;
* è stato aggiunto il parametro `imagereload` con punti di interruzione espliciti;
* invece di impostare una dimensione fissa del visualizzatore utilizzando unità assolute, utilizza CSS che imposta la larghezza e l’altezza del visualizzatore su 100% come nell’esempio seguente:

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

La pagina degli esempi seguenti illustra gli utilizzi più reali dell’incorporazione di design reattivo a altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Posizione demo alternativa](https://experienceleague.adobe.com/tools/vlist/vlist.html)

## Incorporazione di dimensioni flessibili con larghezza e altezza definite {#section-0a329016f9414d199039776645c693de}

In caso di incorporamento di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina web è diverso. Fornisce entrambe le dimensioni al DIV `"holder"` e lo centra nella finestra del browser. Inoltre, la pagina web imposta le dimensioni degli elementi `HTML` e `BODY` al 100%.

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

Gli altri passaggi di incorporamento sono identici ai passaggi utilizzati per incorporare design reattivo con altezza illimitata. L’esempio risultante è il seguente:

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

## Incorporazione tramite API basate su Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L’utilizzo di questo costruttore API non accetta alcun parametro e i parametri di configurazione vengono specificati utilizzando i metodi `setContainerId()`, `setParam()` e `setAsset()` API con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con l’API basata su setter:

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
