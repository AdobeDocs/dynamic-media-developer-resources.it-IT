---
title: eCatalog
description: eCatalog Viewer è un visualizzatore di cataloghi che visualizza le brochure elettroniche in modalità "spread by spread" o "page by page". L’eCatalog consente agli utenti di navigare all’interno del catalogo utilizzando elementi dell’interfaccia utente aggiuntivi o in modalità miniature dedicata. Gli utenti possono anche eseguire lo zoom avanti su ogni pagina per ottenere maggiori dettagli.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 8e243fa5-e375-41ce-8b49-2571023130c1
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2134'
ht-degree: 0%

---

# eCatalog{#ecatalog}

eCatalog Viewer è un visualizzatore di cataloghi che visualizza le brochure elettroniche in modalità &quot;spread by spread&quot; o &quot;page by page&quot;. L’eCatalog consente agli utenti di navigare all’interno del catalogo utilizzando elementi dell’interfaccia utente aggiuntivi o in modalità miniature dedicata. Gli utenti possono anche eseguire lo zoom avanti su ogni pagina per ottenere maggiori dettagli.

>[!NOTE]
>
>Le immagini che utilizzano Image Rendering (IR) o User-Generated Content (UGC) non sono supportate da questo visualizzatore.

Visualizzatore di tipo 507.

Consulta [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

Questo visualizzatore funziona con gli ecatalog e supporta mappe immagine opzionali e strumenti di condivisione social. Dispone di strumenti per lo zoom, strumenti per la navigazione nel catalogo, supporto per la visualizzazione a schermo intero, miniature e un pulsante di chiusura opzionale. Il visualizzatore supporta anche gli strumenti di condivisione social, Stampa, Scarica e Preferiti. È progettato per funzionare su desktop e dispositivi mobili.

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist](https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist)

## Utilizzo di eCatalog Viewer {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore eCatalog rappresenta un file JavaScript principale e un set di file di supporto (un singolo JavaScript da includere con tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione

È possibile utilizzare eCatalog Viewer in modalità pop-up utilizzando una pagina HTML pronta per la produzione fornita con IS-Viewers o in modalità incorporata, in cui viene integrato nella pagina web di destinazione utilizzando l’API documentata.

La configurazione e l’interfaccia sono simili a quelle degli altri visualizzatori. Tutte le operazioni di skin vengono eseguite tramite CSS personalizzato.

Vedi [Riferimento al comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento al comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore eCatalog {#section-642e66ca38cd4032992840ec6c0b0cd2}

Il visualizzatore eCatalog supporta i seguenti gesti touch comuni in altre applicazioni mobili.

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
   <td colname="col2"> <p> Seleziona la nuova miniatura nei campioni. </p> </td> 
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
   <td colname="col2"> <p> Scorre l'elenco delle pagine del catalogo se viene utilizzata una transizione di frame diapositiva. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento verticale </p> </td> 
   <td colname="col2"> <p>Quando l’immagine è in stato di ripristino, esegue uno scorrimento nativo della pagina. </p> <p>Quando le miniature sono attive, scorre l'elenco delle miniature. </p> </td> 
  </tr> 
 </tbody> 
</table>

È possibile abilitare un effetto di animazione realistico per il capovolgimento della pagina per spostarsi tra le pagine del catalogo. In questi casi, l’utente può tenere premuto e trascinare l’angolo di una pagina e capovolgerla.

Questo visualizzatore supporta anche l&#39;input del mouse e del touch-screen sui dispositivi Windows. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera come descritto in [Accesso facilitato da tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Strumenti di condivisione per social media con visualizzatore eCatalog {#section-eb575084a99647c3a9591f439f40b412}

Il visualizzatore eCatalog supporta gli strumenti di condivisione social. Sono disponibili come pulsante nella barra di controllo principale che si espande in una barra degli strumenti di condivisione quando un utente fa clic o tocca su di essa.

La barra degli strumenti Condivisione contiene icone per ogni tipo di canale di condivisione supportato, tra cui Facebook, Twitter, condivisione e-mail, condivisione codice di incorporamento e condivisione collegamenti. Quando gli strumenti di condivisione e-mail, condivisione di incorporamento o condivisione di collegamenti sono attivati, il visualizzatore visualizza una finestra di dialogo modale con il modulo di immissione dati corrispondente. Quando si chiama Facebook o Twitter, il visualizzatore reindirizza l’utente a una finestra di dialogo di condivisione standard da un servizio social. Gli strumenti di condivisione non sono disponibili in modalità a schermo intero a causa di restrizioni di sicurezza del browser Web.

## Incorporazione del visualizzatore eCatalog {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, se selezionato, apre il visualizzatore in una finestra del browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare una progettazione reattiva che viene visualizzata in modo diverso su dispositivi diversi o per dimensioni diverse della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità operative principali: popup, incorporamento di dimensioni fisse e incorporamento di progetti reattivi.

**Informazioni sulla modalità popup**

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda del browser Web separata. Occupa l’intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l’orientamento di un dispositivo mobile venga modificato.

La modalità pop-up è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando `window.open()` chiamata JavaScript, `A` elemento HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML preconfigurata per la modalità di funzionamento popup. In questo caso, si chiama [!DNL eCatalogViewer.html] e si trova nella sottocartella [!DNL html5/] della distribuzione IS-Viewers standard:

[!DNL <s7viewers_root>/html5/eCatalogViewer.html]

Puoi ottenere una personalizzazione visiva applicando CSS personalizzata.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```html {.line-numbers}
<a href="https://s7d1.scene7.com/s7viewers/html5/eCatalogViewer.html?asset=Viewers/Pluralist" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento di progettazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe già avere alcuni contenuti per i clienti non correlati al visualizzatore. Il visualizzatore occupa normalmente solo una parte del patrimonio immobiliare di una pagina web.

I casi d’uso principali sono le pagine web orientate per desktop o dispositivi tablet e le pagine progettate responsive che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questo metodo è la scelta migliore per le pagine web con un layout statico.

L&#39;incorporamento reattivo della progettazione presuppone che il visualizzatore debba essere ridimensionato in fase di esecuzione in risposta alla modifica delle dimensioni del relativo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

In modalità di incorporamento di progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`, lasciando libera la sua altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa funzionalità assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura sui lati. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout reattivi come Bootstrap e Foundation.

In caso contrario, se la pagina Web imposta sia la larghezza che l&#39;altezza per il contenitore del visualizzatore `DIV`, il visualizzatore occupa solo tale area e segue le dimensioni fornite dal layout della pagina Web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuare le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del DIV del contenitore.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l&#39;API del visualizzatore, assicurati di includere [!DNL eCatalogViewer.js]. Il file [!DNL eCatalogViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/eCatalogViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene fornito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo è simile al seguente:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/eCatalogViewer.js"></script>
```

>[!NOTE]
>
>Fare riferimento solo al file JavaScript `include` del visualizzatore principale nella pagina. Non fare riferimento ad altri file JavaScript nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente alla libreria `Utils.js` dell&#39;SDK di HTML5 caricata dal visualizzatore dal percorso di contesto `/s7viewers` (il cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o di librerie di visualizzatori di runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. L&#39;Adobe non mantiene sul server le versioni precedenti del visualizzatore secondario `includes`.
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

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica per il visualizzatore dichiarandolo per la classe CSS di primo livello `.s7ecatalogviewer` in unità assolute oppure utilizzando il modificatore `stagesize`.

   Puoi inserire il dimensionamento in CSS direttamente nella pagina HTML. Oppure, inserisci il dimensionamento in un file CSS visualizzatore personalizzato, che viene successivamente assegnato a un record di predefinito visualizzatore in Dynamic Media Classic, o passato esplicitamente utilizzando un comando di stile.

   Per ulteriori informazioni sullo stile del visualizzatore con CSS, vedere [Personalizzazione del visualizzatore eCatalog](../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-viewer-customizingviewer/c-html5-20-ecatalog-viewer-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0).

   Di seguito è riportato un esempio di definizione di una dimensione di visualizzatore statico nella pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   È possibile impostare il modificatore `stagesize` nel record del predefinito visualizzatore in Dynamic Media Classic. In alternativa, è possibile trasmetterlo esplicitamente con il codice di inizializzazione del visualizzatore con la raccolta `params` o come chiamata API come descritto nella sezione Riferimento comando, come segue:

   ```html {.line-numbers}
   eCatalogViewer.setParam("stagesize", 
   "640,480");
   ```

1. Inizializzazione del visualizzatore.

   Dopo aver completato i passaggi precedenti, si crea un&#39;istanza della classe `s7viewers.eCatalogViewer`, si passano tutte le informazioni di configurazione al relativo costruttore e si chiama il metodo `init()` su un&#39;istanza del visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto ha almeno il campo `containerId` che contiene il nome dell&#39;ID contenitore del visualizzatore e l&#39;oggetto JSON `params` nidificato con i parametri di configurazione supportati dal visualizzatore. In questo caso, l&#39;oggetto `params` deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento corpo `onload()`.

   Allo stesso tempo, l’elemento contenitore non deve ancora necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza del visualizzatore, di passaggio delle opzioni di configurazione minime necessarie al costruttore e di chiamata al metodo `init()`. L&#39;esempio presuppone che `eCatalogViewer` sia l&#39;istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; `https://s7d1.scene7.com/is/image/` è l&#39;URL di Image Server e `Viewers/Pluralist` è la risorsa:

   ```html {.line-numbers}
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script>
   ```

   Il codice seguente è un esempio completo di una pagina Web banale che incorpora il visualizzatore eCatalog con dimensioni fisse:

   ```html {.line-numbers}
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7ecatalogviewer { 
    width: 640px; 
    height: 480px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var eCatalogViewer = new s7viewers.eCatalogViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"Viewers/Pluralist", 
    "serverurl":"https://s7d1.scene7.com/is/image/" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporamento di progettazione reattiva con altezza illimitata**

Con l’incorporamento di un design reattivo, la pagina web in genere ha un layout flessibile che determina la dimensione di runtime del contenitore del visualizzatore `DIV`. Ai fini di questo esempio, si supponga che la pagina Web consenta al contenitore del visualizzatore `DIV` di occupare il 40% delle dimensioni della finestra del browser Web, senza limitazioni di altezza. Il codice HTML risultante per la pagina Web è simile al seguente:

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

L’aggiunta del visualizzatore a una pagina di questo tipo è simile all’incorporamento di dimensioni fisse, con l’unica differenza che non è necessario definire esplicitamente le dimensioni del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del DIV del contenitore.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell’incorporamento a dimensione fissa. Aggiungere il contenitore `DIV` al &quot; titolare&quot; esistente `DIV`. Il codice seguente è un esempio completo. Puoi vedere come cambiano le dimensioni del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La pagina di esempi seguente illustra altri casi d’uso reali di progetti reattivi con altezza illimitata incorporati:

[Demo Live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

**Dimensione flessibile con larghezza e altezza definite**

Nell’incorporamento di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina web è diverso. In altre parole, fornisce entrambe le dimensioni al &quot; titolare&quot; `DIV` e lo centra nella finestra del browser. La pagina Web imposta inoltre le dimensioni dell&#39;elemento `HTML` e dell&#39;elemento `BODY` al 100%:

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

I passaggi di incorporamento rimanenti sono identici all’incorporamento reattivo con altezza illimitata. L’esempio risultante è il seguente:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
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
var eCatalogViewer = new s7viewers.eCatalogViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Viewers/Pluralist", 
 "serverurl":"https://s7d1.scene7.com/is/image/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporamento tramite API basata su Set**

Invece di utilizzare l’inizializzazione basata su JSON è possibile utilizzare un’API basata su setter e un costruttore no-args. Con il costruttore API non accetta parametri e i parametri di configurazione sono specificati utilizzando i metodi API `setContainerId()`, `setParam()` e `setAsset()` con chiamate JavaScript separate.

L’esempio seguente mostra un’incorporazione a dimensione fissa con API basate su setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://s7d1.scene7.com/s7viewers/html5/js/eCatalogViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7ecatalogviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var eCatalogViewer = new s7viewers.eCatalogViewer(); 
eCatalogViewer.setContainerId("s7viewer"); 
eCatalogViewer.setParam("serverurl", "https://s7d1.scene7.com/is/image/"); 
eCatalogViewer.setAsset("Viewers/Pluralist"); 
eCatalogViewer.init(); 
</script> 
</body> 
</html>
```
