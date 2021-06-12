---
description: Il visualizzatore a 360 gradi è un visualizzatore di immagini che fornisce una visualizzazione dell’immagine a 360 gradi o anche una visualizzazione multidimensionale, se si utilizza un set 360 gradi appropriato. È dotato di strumenti di zoom e rotazione, supporto a schermo intero e un pulsante di chiusura opzionale. È progettato per funzionare su desktop e dispositivi mobili.
keywords: reattivo
solution: Experience Manager
title: Spin
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set 360 gradi
role: Developer,Business Practitioner
exl-id: 4c802d42-ea5b-4f28-b6ef-2689aa16839d
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '2135'
ht-degree: 0%

---

# Centrifuga{#spin}

Il visualizzatore a 360 gradi è un visualizzatore di immagini che fornisce una visualizzazione dell’immagine a 360 gradi o anche una visualizzazione multidimensionale, se si utilizza un set 360 gradi appropriato. È dotato di strumenti di zoom e rotazione, supporto a schermo intero e un pulsante di chiusura opzionale. È progettato per funzionare su desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Tipo di visualizzatore 503.

Consulta [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400](https://s7d9.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&amp;stagesize=500,400)

## Utilizzo del visualizzatore a 360 gradi {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore a 360 gradi rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Il visualizzatore a 360 gradi può essere utilizzato sia in modalità pop-up utilizzando una pagina HTML pronta per la produzione fornita con IS-Viewers o in modalità incorporata, dove viene integrato nella pagina web di destinazione utilizzando un’API documentata.

La configurazione e lo skin sono simili a quelli degli altri visualizzatori. Tutta la skin può essere ottenuta tramite CSS personalizzati.

Consulta [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento ai comandi comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore a 360 gradi {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il visualizzatore a 360 gradi supporta i seguenti gesti di contatto comuni ad altre applicazioni mobili. Quando il visualizzatore non è in grado di elaborare il gesto di scorrimento rapido di un utente, inoltra l’evento al browser web per eseguire un scorrimento nativo della pagina. Questo consente all’utente di navigare nella pagina anche se il visualizzatore occupa la maggior parte dell’area dello schermo del dispositivo.

<table id="table_ED747CC7178448919C34A4FCD18922D0"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Gesto </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>Doppio tocco </p> </td> 
   <td colname="col2"> <p> Esegue lo zoom di un livello fino a raggiungere l'ingrandimento massimo. Il doppio tocco successivo ripristina lo stato di visualizzazione iniziale del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pizzico </p> </td> 
   <td colname="col2"> <p>Ingrandisce o riduce l’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento orizzontale o rapido </p> </td> 
   <td colname="col2"> <p> Se l'immagine è in uno stato di reset, gira in orizzontale attraverso il set. </p> <p> Se l'immagine viene ingrandita, l'immagine viene spostata in orizzontale. Se l’immagine viene spostata sul bordo della visualizzazione e lo scorrimento viene ancora eseguito in quella direzione, il movimento esegue uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento o scorrimento verticale </p> </td> 
   <td colname="col2"> <p> Se l’immagine è in uno stato di ripristino, cambia l’angolo di visualizzazione verticale nel caso in cui venga utilizzato un set 360 gradi multidimensionale. In un set 360 gradi monodimensionale o quando un set 360 gradi multidimensionale si trova sull’ultimo o sul primo asse, in modo che lo scorrimento verticale non comporti una modifica dell’angolo di visualizzazione verticale, il movimento esegue uno scorrimento nativo della pagina. </p> <p> Se l'immagine viene ingrandita, l'immagine viene spostata verticalmente. Se l’immagine viene spostata sul bordo della visualizzazione e lo scorrimento viene ancora eseguito in quella direzione, il movimento esegue uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Il visualizzatore supporta anche l’input touch e l’input del mouse su dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Consulta [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore a 360 gradi {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, quando fai clic su di essa, apre il visualizzatore in una finestra separata del browser. In altri casi, è necessario incorporare il diritto del visualizzatore nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare un design reattivo che viene visualizzato in modo diverso su diversi dispositivi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: incorporazione a dimensione fissa e design reattivo.

**Informazioni sulla modalità a comparsa**

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda separata del browser Web. Prende l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o se viene modificato l&#39;orientamento di un dispositivo mobile.

La modalità pop-up è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` una chiamata JavaScript, un elemento `A` HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML predefinita per la modalità operativa a comparsa. In questo caso, si chiama [!DNL SpinViewer.html] e si trova all’interno della sottocartella [!DNL html5/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/SpinViewer.html]

Puoi ottenere la personalizzazione visiva applicando CSS personalizzati.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
<a 
href="http://s7d1.scene7.com/s7viewers/html5/SpinViewer.html?asset=Scene7SharedAssets/SpinSet_Sample&stagesize=500,400" 
target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento della progettazione reattiva**

Nella modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe avere già alcuni contenuti del cliente non correlati al visualizzatore. Il visualizzatore normalmente occupa solo una parte del patrimonio immobiliare di una pagina web.

I casi d’uso principali sono le pagine web orientate ai desktop o ai dispositivi tablet, nonché le pagine di progettazione reattiva che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporazione a dimensione fissa viene utilizzata quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questa è la scelta migliore per le pagine web con layout statico.

L’incorporazione di design reattivo presuppone che il visualizzatore debba ridimensionare in fase di runtime in risposta alla modifica delle dimensioni del contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

Nella modalità di incorporamento della progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il proprio contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando senza limitazioni l’altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa funzionalità assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura laterale. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout di progettazione reattiva come Bootstrap, Foundation e così via.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza del contenitore del visualizzatore `DIV`, il visualizzatore compila solo quell’area e segue le dimensioni fornite dal layout della pagina web. Un buon esempio può essere l’incorporazione del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a 360 gradi a una pagina web, effettua le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere `SpinViewer.js`. `SpinViewer.js` si trova nella  [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

   `<s7viewers_root>/html5/js/SpinViewer.js`

   Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Dynamic Media di Adobe e viene servito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Dynamic Media di Adobe in cui sono installati i visualizzatori IS.

   Il percorso relativo si presenta come segue:

   ```
    <script language="javascript" type="text/javascript" src="/s7viewers/html5/js/SpinViewer.js"></script>
   ```

   >[!NOTE]
   >
   >Dovresti fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non devi fare riferimento a file JavaScript aggiuntivi nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente alla libreria HTML5 SDK `Utils.js` caricata dal visualizzatore dal percorso contestuale `/s7viewers` (cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o librerie di visualizzatori runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva le versioni precedenti del visualizzatore secondario `includes` sul server.
   >
   >
   >Di conseguenza, l’inserimento di un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore DIV.

   Aggiungi un elemento DIV vuoto alla pagina in cui desideri che appaia il visualizzatore. L’ID dell’elemento DIV deve essere definito perché viene passato successivamente all’API del visualizzatore.

   Il segnaposto DIV è un elemento posizionato, il che significa che la proprietà CSS `position` è impostata su `relative` o `absolute`.

   Di seguito è riportato un esempio di elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica del visualizzatore dichiarandola per la classe CSS di livello superiore `.s7spinviewer` in unità assolute o utilizzando il modificatore `stagesize`.

   Puoi inserire le dimensioni in CSS direttamente nella pagina HTML o in un file CSS per visualizzatori personalizzati, che viene poi assegnato a un record predefinito per visualizzatori in Dynamic Media Classic, o passato esplicitamente utilizzando un comando stile.

   Consulta [Personalizzazione del visualizzatore a 360 gradi](../../c-html5-s7-aem-asset-viewers/c-html5-spin-viewer-about/c-html5-spin-viewer-customizingviewer/c-html5-spin-viewer-customizingviewer.md#concept-464f3bfa55764bc09c92d8c7480b0b55) per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione delle dimensioni di un visualizzatore statico nella pagina HTML:

   ```
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puoi impostare il modificatore `stagesize` nel record predefinito del visualizzatore in Dynamic Media Classic, oppure passarlo esplicitamente con il codice di inizializzazione del visualizzatore con la raccolta `params`, o come chiamata API come descritto nella sezione Riferimento comandi , come segue:

   ```
    spinViewer.setParam("stagesize", 
   "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza della classe `s7viewers.SpinViewer`, passa tutte le informazioni di configurazione al relativo costruttore e chiama il metodo `init()` su un’istanza di visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Come minimo, questo oggetto ha un campo `containerId` che contiene il nome dell’ID del contenitore di visualizzatori e un oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore. In questo caso dell’oggetto `params`, deve avere almeno l’URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()` .

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web per ora. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` ad esso assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del metodo `init()` . L’esempio presuppone che `spinViewer` sia l’istanza del visualizzatore, che `s7viewer` sia il nome del segnaposto `DIV`, che [!DNL http://s7d1.scene7.com/is/image/] sia l’URL di Image Server e che la risorsa sia [!DNL Scene7SharedAssets/SpinSet_Sample].

   ```
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Il codice seguente è un esempio completo di una pagina web banale che incorpora il visualizzatore 360 gradi con dimensioni fisse:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7spinviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var spinViewer = new s7viewers.SpinViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Scene7SharedAssets/SpinSet_Sample", 
    "serverurl":"http://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporazione di design reattivo con altezza illimitata**

Con l’incorporazione di design reattivo, la pagina web dispone normalmente di un layout flessibile che determina le dimensioni di runtime del contenitore del visualizzatore `DIV`. Ai fini di questo esempio, si supponga che la pagina web consenta al contenitore del visualizzatore `DIV` di assumere il 40% delle dimensioni della finestra del browser Web, lasciando senza limitazioni l’altezza. Il codice HTML della pagina web risultante avrà un aspetto simile al seguente:

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

L’aggiunta del visualizzatore a una pagina di questo tipo è simile all’incorporazione a dimensione fissa, con l’unica differenza che non è necessario definire in modo esplicito le dimensioni del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell&#39;incorporazione a dimensione fissa. Aggiungi il contenitore `DIV` al &quot; holder&quot; esistente `DIV`. Il codice seguente è un esempio completo. Puoi vedere come cambia la dimensione del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La pagina degli esempi seguenti illustra casi d’uso più reali di incorporamento dinamico del design con altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Posizione demo alternativa](https://experienceleague.adobe.com/tools/vlist/vlist.html)

**Incorporazione di dimensioni flessibili con larghezza e altezza definite**

In caso di incorporamento di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina web è diverso. In altre parole, fornisce entrambe le dimensioni al &quot; holder&quot; `DIV` e lo centra nella finestra del browser. Inoltre, la pagina web imposta le dimensioni degli elementi `HTML` e `BODY` su 100%:

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

I passaggi rimanenti per l’incorporazione sono identici a quelli per l’incorporazione di progetti reattivi con altezza illimitata. L’esempio risultante è il seguente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
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
var spinViewer = new s7viewers.SpinViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/SpinSet_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporazione tramite API basate su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. Con tale costruttore API non accetta alcun parametro e i parametri di configurazione vengono specificati utilizzando i metodi `setContainerId()`, `setParam()` e `setAsset()` API con chiamate JavaScript separate.

L’esempio seguente mostra l’incorporazione di dimensioni fisse con API basata su setter:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/SpinViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7spinviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var spinViewer = new s7viewers.SpinViewer(); 
spinViewer.setContainerId("s7viewer"); 
spinViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
spinViewer.setAsset("Scene7SharedAssets/SpinSet_Sample"); 
spinViewer.init(); 
</script> 
</body> 
</html>
```
