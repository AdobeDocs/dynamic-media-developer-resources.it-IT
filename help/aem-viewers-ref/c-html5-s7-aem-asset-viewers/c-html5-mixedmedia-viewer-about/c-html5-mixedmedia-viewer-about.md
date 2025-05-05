---
title: File multimediali diversi
description: Visualizzatore di file multimediali diversi è un visualizzatore di file multimediali. Supporta i set di file multimediali che contengono immagini, set di campioni, set 360 gradi, video e set di video adattivi.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2581'
ht-degree: 0%

---

# File multimediali diversi{#mixed-media}

Visualizzatore di file multimediali diversi è un visualizzatore di file multimediali. Supporta i set di file multimediali che contengono immagini, set di campioni, set 360 gradi, video e set di video adattivi.

Una miniatura nella parte inferiore del visualizzatore rappresenta ogni elemento del set di file multimediali insieme al relativo indicatore del tipo di risorsa. Quando viene selezionato un elemento del set di campioni, viene visualizzata una riga secondaria di campioni che consente di selezionare la variazione di colore all&#39;interno del set di campioni. Le immagini e gli elementi del set di campioni supportano lo zoom in modalità continua o in linea; i set 360 gradi supportano sia lo zoom che la rotazione. I video e i set video adattivi supportano tutti i controlli di riproduzione di base, purché tutti i sottotitoli facoltativi vengano visualizzati sopra il contenuto video. L’utente può passare alla modalità a schermo intero in qualsiasi momento facendo clic sul pulsante. Il visualizzatore ha un pulsante di chiusura opzionale. È progettato per funzionare su desktop e dispositivi mobili.

Il visualizzatore di file multimediali diversi utilizza la riproduzione video in streaming HTML5 in formato HLS nella sua configurazione predefinita ogni volta che il sistema sottostante lo supporta. Sui sistemi che non supportano lo streaming HTML5, il visualizzatore torna alla distribuzione di video progressivi HTML5.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Visualizzatore di tipo 505.

Consulta [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Utilizzo del visualizzatore di file multimediali diversi {#section-f21ac23d3f6449ad9765588d69584772}

Il visualizzatore di file multimediali diversi rappresenta un file JavaScript principale e un set di file di supporto (un singolo JavaScript include con tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

È possibile utilizzare il visualizzatore di file multimediali diversi in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con i visualizzatori IS. In alternativa, puoi utilizzare il visualizzatore in modalità incorporata, dove viene integrato in una pagina web di destinazione utilizzando l’API documentata.

L’operazione di configurazione e interpolazione del visualizzatore è simile a quella di altri visualizzatori. Tutte le operazioni di skin vengono eseguite tramite CSS personalizzato.

Vedi [Riferimento al comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento al comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore di file multimediali diversi {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore di file multimediali diversi supporta i gesti single-touch e multi-touch comuni in altre applicazioni mobili. Quando il visualizzatore non è in grado di elaborare il gesto di scorrimento di un utente, inoltra l’evento al browser web per eseguire uno scorrimento nativo della pagina. Questa funzionalità consente a un utente di spostarsi all’interno della pagina anche se il visualizzatore occupa la maggior parte dell’area dello schermo del dispositivo.

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
   <td colname="col1"> <p>Doppio tocco </p> </td> 
   <td colname="col2"> <p>In modalità zoom <span class="codeph"> continuo </span>, ingrandisce di un livello fino al raggiungimento dell'ingrandimento massimo; il successivo movimento di doppio tocco ripristina lo stato iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tocco e tenere premuto </p> </td> 
   <td colname="col2"> <p> In modalità zoom </span> inline <span class="codeph"> attiva l'immagine ingrandita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pizzicare </p> </td> 
   <td colname="col2"> <p>In modalità zoom continuo, ingrandisce o riduce l'immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento orizzontale </p> </td> 
   <td colname="col2"> <p> Quando la risorsa corrente è un set 360 gradi e l’immagine è in stato di ripristino, ruota attraverso il set 360 gradi in orizzontale. </p> <p> Quando la risorsa corrente è un set 360 gradi o un’immagine e l’immagine è ingrandita, l’immagine viene spostata orizzontalmente. Se l'immagine viene spostata sul bordo della vista e lo scorrimento viene eseguito ancora in quella direzione, il movimento esegue uno scorrimento nativo della pagina. </p> <p> Scorre l'elenco dei campioni nella barra dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento verticale </p> </td> 
   <td colname="col2"> <p> Se l'immagine è reimpostata, l'angolo di visualizzazione verticale viene modificato nel caso in cui venga utilizzato un set 360 gradi multidimensionale. In un set 360 gradi unidimensionale o quando un set 360 gradi multidimensionale si trova sull'ultimo o sul primo asse, in modo che il passaggio verticale non provochi una modifica dell'angolo di visualizzazione verticale, il movimento esegue lo scorrimento nativo della pagina. </p> <p> Quando la risorsa corrente è un set 360 gradi o un’immagine e l’immagine è ingrandita, sposta l’immagine in verticale. Se l'immagine viene spostata sul bordo della vista e lo scorrimento viene eseguito ancora in quella direzione, il movimento esegue lo scorrimento nativo della pagina. </p> <p> Se il movimento viene eseguito all'interno dell'area dei campioni, esegue uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta inoltre l&#39;input tocco e mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Consulta [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione di visualizzatori di file multimediali diversi {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, se selezionato, apre il visualizzatore in una finestra del browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare una progettazione reattiva che viene visualizzata in modo diverso su dispositivi diversi o per dimensioni diverse della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità operative principali: popup, incorporamento di dimensioni fisse e incorporamento di progetti reattivi.

## Informazioni sulla modalità popup {#section-77d5aa03b8b94566958a179b1a2cd474}

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda del browser Web separata. Occupa l’intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o l’orientamento di un dispositivo mobile venga modificato.

La modalità pop-up è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando `window.open()` chiamata JavaScript, `A` elemento HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML preconfigurata per la modalità di funzionamento popup. In questo caso, si chiama [!DNL MixedMediaViewer.html] e si trova nella sottocartella [!DNL html5/] della distribuzione IS-Viewers standard:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Puoi ottenere una personalizzazione visiva applicando CSS personalizzata.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Informazioni sull’incorporamento di progetti a dimensione fissa e reattivi {#section-ec86b100ba5943d0b16694268520bbde}

In modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe già avere alcuni contenuti per i clienti non correlati al visualizzatore. Il visualizzatore occupa normalmente solo una parte del patrimonio immobiliare di una pagina web.

I casi d’uso principali sono le pagine web orientate per desktop o dispositivi tablet e le pagine di progettazione reattive che regolano automaticamente il layout a seconda del tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questa è la scelta migliore per le pagine web con un layout statico.

L&#39;incorporamento reattivo della progettazione presuppone che il visualizzatore debba essere ridimensionato in fase di esecuzione in risposta alla modifica delle dimensioni del relativo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

In modalità di incorporamento di progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`, lasciando libera la sua altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa funzionalità assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura sui lati. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout di progettazione reattivi come Bootstrap o Foundation.

In caso contrario, se la pagina Web imposta sia la larghezza che l&#39;altezza per il contenitore del visualizzatore `DIV`, il visualizzatore occupa solo tale area e segue le dimensioni fornite dal layout della pagina Web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

## Incorporazione a dimensione fissa {#section-17d162f76ffa4804b27928f51e7bea1d}

Per aggiungere il visualizzatore a una pagina Web, effettuare le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l&#39;API del visualizzatore, assicurati di includere [!DNL MixedMediaViewer.js]. Il file [!DNL MixedMediaViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene fornito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo è simile al seguente:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>Fare riferimento solo al file JavaScript `include` del visualizzatore principale nella pagina. Non fare riferimento ad altri file JavaScript nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente alla libreria `Utils.js` dell&#39;SDK di HTML5 caricata dal visualizzatore dal percorso di contesto `/s7viewers` (il cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o di librerie di visualizzatori di runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. L&#39;Adobe non mantiene sul server le versioni precedenti del visualizzatore secondario `includes`.
>
>
>Di conseguenza, il posizionamento di un riferimento diretto a qualsiasi JavaScript `include` secondario utilizzato dal visualizzatore nella pagina interrompe la funzionalità del visualizzatore in futuro, quando viene distribuita una nuova versione del prodotto.

1. Definizione del DIV del contenitore.

   Aggiungi un elemento DIV vuoto alla pagina in cui vuoi che venga visualizzato il visualizzatore. L’ID dell’elemento DIV deve essere definito perché questo ID viene passato successivamente all’API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il DIV segnaposto è un elemento posizionato, il che significa che la proprietà CSS `position` è impostata su `relative` o `absolute`.

   Verificare che la funzione a schermo intero funzioni correttamente in Internet Explorer. Verifica che nel DOM non siano presenti altri elementi con un ordine di sovrapposizione più elevato rispetto al DIV segnaposto.

   Di seguito è riportato un esempio di un elemento DIV segnaposto definito:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore

   Questo visualizzatore visualizza le miniature quando si lavora con set di più elementi. Sui sistemi desktop, le miniature sono posizionate sotto la vista principale. Allo stesso tempo, il visualizzatore consente lo scambio della risorsa principale durante il runtime utilizzando l&#39;API `setAsset()`. In qualità di sviluppatore, puoi controllare il modo in cui il visualizzatore gestisce l’area miniature nella parte inferiore quando la nuova risorsa ha un solo elemento. È possibile mantenere intatte le dimensioni del visualizzatore esterno e lasciare che la visualizzazione principale aumenti la sua altezza e occupi l’area delle miniature. In alternativa, è possibile mantenere statica la dimensione della visualizzazione principale e comprimere l&#39;area di visualizzazione esterna, consentendo lo spostamento verso l&#39;alto del contenuto della pagina Web. Quindi, utilizza la pagina immobiliare gratuita che è rimasta dalle miniature.

   Per mantenere intatti i limiti del visualizzatore esterno, definire la dimensione per la classe CSS di livello superiore `.s7mixedmediaviewer` in unità assolute. Il ridimensionamento in CSS può essere inserito direttamente nella pagina HTML o in un file CSS visualizzatore personalizzato e successivamente assegnato a un record predefinito visualizzatore in Dynamic Media Classic oppure passato esplicitamente utilizzando il comando style.

   Per ulteriori informazioni sullo stile del visualizzatore con CSS, vedere [Personalizzazione del visualizzatore di file multimediali diversi](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4).

   Di seguito è riportato un esempio di definizione delle dimensioni statiche del visualizzatore esterno in una pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puoi vedere il comportamento con un’area visualizzatore esterna fissa nella seguente pagina di esempio. Tieni presente che quando passi da un set all’altro, le dimensioni del visualizzatore esterno non cambiano:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html?lang=it](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html?lang=it)

   Per rendere statiche le dimensioni della visualizzazione principale, definisci le dimensioni del visualizzatore in unità assolute per il componente SDK `Container` interno utilizzando il selettore CSS `.s7mixedmediaviewer .s7container` o il modificatore `stagesize`.

   Di seguito è riportato un esempio di definizione delle dimensioni del visualizzatore per il componente SDK `Container` interno in modo che l&#39;area di visualizzazione principale non cambi le dimensioni quando si cambia la risorsa:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Nella pagina di esempio seguente viene illustrato il comportamento del visualizzatore con una dimensione di visualizzazione principale fissa. Quando passi da un set all’altro, la vista principale rimane statica e il contenuto della pagina web si sposta verticalmente:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html?lang=it](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html?lang=it)

   È possibile impostare il modificatore `stagesize` nel record del predefinito visualizzatore in Dynamic Media Classic oppure trasmetterlo in modo esplicito con il codice di inizializzazione del visualizzatore nella raccolta `params`. Oppure, come chiamata API come descritto nella sezione Riferimento comando di questa Guida, come nei seguenti casi:

   ```html {.line-numbers}
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   Si consiglia un approccio basato su CSS, che viene utilizzato in questo esempio.

1. Creazione e inizializzazione del visualizzatore.

   Dopo aver completato i passaggi precedenti, si crea un&#39;istanza della classe `s7viewers.MixedMediaViewer`, si passano tutte le informazioni di configurazione al relativo costruttore e si chiama il metodo `init()` su un&#39;istanza del visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto deve avere almeno il campo `containerId` che contiene il nome dell&#39;ID contenitore del visualizzatore e l&#39;oggetto JSON `params` nidificato con i parametri di configurazione supportati dal visualizzatore. In questo caso, l&#39;oggetto `params` deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl`, l&#39;URL del server video passato come proprietà `videoserverurl` e la risorsa iniziale come parametro `asset`. API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sul corpo dell&#39;evento `onload()`.

   Allo stesso tempo, l’elemento contenitore non deve ancora necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza del visualizzatore, di passaggio delle opzioni di configurazione minime necessarie al costruttore e di chiamata al metodo `init()`. L&#39;esempio presuppone che `mixedMediaViewer` sia l&#39;istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; [!DNL http://s7d1.scene7.com/is/image/] è l&#39;URL di Image Server; [!DNL http://s7d1.scene7.com/is/content/] è l&#39;URL del server video e [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] è la risorsa:

```html {.line-numbers}
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
<script type="text/javascript"> 
mixedMediaViewer.init(); 
</script>
```

Il codice che segue è un esempio completo di una pagina web banale che incorpora il visualizzatore di file multimediali diversi con una dimensione fissa:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporamento reattivo con altezza illimitata {#section-056cb574713c4d07be6d07cf3c598839}

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La pagina di esempi seguente illustra usi più reali dell’incorporamento di design responsive con altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Percorso demo alternativo](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html?lang=it)

## Dimensione flessibile che incorpora con larghezza e altezza definite {#section-0a329016f9414d199039776645c693de}

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
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
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
var mixedMediaViewer = new s7viewers.MixedMediaViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"Scene7SharedAssets/Mixed_Media_Set_Sample", 
 "serverurl":"http://s7d1.scene7.com/is/image/", 
 "videoserverurl":"http://s7d1.scene7.com/is/content/" 
} 
}).init(); 
</script> 
</body> 
</html>
```

## Incorporazione tramite API basata su Set {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Invece di utilizzare l’inizializzazione basata su JSON, puoi utilizzare l’API basata su setter e il costruttore no-args. L&#39;utilizzo di questo costruttore API non accetta parametri e i parametri di configurazione sono specificati utilizzando i metodi API `setContainerId()`, `setParam()` e `setAsset()`, con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con API basate su setter:

```html {.line-numbers}
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://s7d1.scene7.com/s7viewers/html5/js/MixedMediaViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7mixedmediaviewer { 
 width: 640px; 
 height: 480px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var mixedMediaViewer = new s7viewers.MixedMediaViewer(); 
mixedMediaViewer.setContainerId("s7viewer"); 
mixedMediaViewer.setParam("serverurl", "http://s7d1.scene7.com/is/image/"); 
mixedMediaViewer.setAsset("Scene7SharedAssets/Mixed_Media_Set_Sample"); 
mixedMediaViewer.init(); 
</script> 
</body> 
</html>
```
