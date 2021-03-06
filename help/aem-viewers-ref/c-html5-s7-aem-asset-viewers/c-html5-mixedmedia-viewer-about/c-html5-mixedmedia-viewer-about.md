---
title: Supporti multipli
description: Il visualizzatore di file multimediali diversi è un visualizzatore di contenuti multimediali diversi. Supporta i set di file multimediali che contengono immagini, set di campioni, set 360 gradi, video e set di video adattivi.
keywords: reattivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: 65a54308-f9db-4458-a9c3-ccb1433af43c
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '2645'
ht-degree: 0%

---

# Supporti multipli{#mixed-media}

Il visualizzatore di file multimediali diversi è un visualizzatore di contenuti multimediali diversi. Supporta i set di file multimediali che contengono immagini, set di campioni, set 360 gradi, video e set di video adattivi.

Una miniatura nella parte inferiore del visualizzatore rappresenta ogni elemento del set di file multimediali, insieme al relativo indicatore del tipo di risorsa. Quando viene selezionato un elemento set di campioni, viene visualizzata una riga secondaria di campioni per consentire la selezione della variazione di colore all’interno del set di campioni. Le immagini e gli elementi set di campioni supportano lo zoom in modalità continua o in linea; i set 360 gradi supportano sia lo zoom che la rotazione. I video e i set di video adattivi supportano tutti i controlli di riproduzione di base, purché sul contenuto video siano visualizzati eventuali sottotitoli codificati opzionali. Un utente può passare in qualsiasi momento alla modalità a schermo intero facendo clic sul pulsante a schermo intero. Il visualizzatore dispone di un pulsante di chiusura opzionale. È progettato per funzionare su desktop e dispositivi mobili.

Il visualizzatore di file multimediali diversi utilizza la riproduzione video in streaming HTML5 in formato HLS nella configurazione predefinita ogni volta che il sistema sottostante lo supporta. Nei sistemi che non supportano lo streaming HTML5, il visualizzatore torna alla distribuzione progressiva dei video HTML5.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Tipo di visualizzatore 505.

Vedi [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Utilizzo del visualizzatore di file multimediali diversi {#section-f21ac23d3f6449ad9765588d69584772}

Il visualizzatore di file multimediali diversi rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

È possibile utilizzare il visualizzatore di file multimediali diversi in modalità pop-up utilizzando la pagina HTML pronta per la produzione fornita con IS-Viewers. In alternativa, puoi utilizzare il visualizzatore in modalità incorporata, dove viene integrato in una pagina web di destinazione utilizzando l’API documentata.

L’attività di configurazione e skin del visualizzatore è simile a quella di altri visualizzatori. Tutta la skin viene ottenuta tramite CSS personalizzati.

Vedi [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con i visualizzatori di file multimediali diversi {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore di file multimediali diversi supporta gesti touch e touch singoli comuni ad altre applicazioni mobili. Quando il visualizzatore non è in grado di elaborare il gesto di scorrimento rapido di un utente, inoltra l’evento al browser web per eseguire un scorrimento nativo della pagina. Questa funzionalità consente a un utente di navigare nella pagina anche se il visualizzatore occupa la maggior parte dell’area dello schermo del dispositivo.

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
   <td colname="col1"> <p>Doppio tocco </p> </td> 
   <td colname="col2"> <p>All'interno <span class="codeph"> continuo </span> in modalità zoom, esegue lo zoom di un livello fino a raggiungere l’ingrandimento massimo; il doppio tocco successivo viene reimpostato sullo stato iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tocco e tenere premuto </p> </td> 
   <td colname="col2"> <p> All'interno <span class="codeph"> inline </span> modalità zoom, attiva l’immagine ingrandita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pizzico </p> </td> 
   <td colname="col2"> <p>In modalità zoom continuo, ingrandisce o riduce l’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento orizzontale o rapido </p> </td> 
   <td colname="col2"> <p> Quando la risorsa corrente è un set 360 gradi e l’immagine è in uno stato di ripristino, ruota in orizzontale attraverso il set 360 gradi. </p> <p> Quando la risorsa corrente è un set 360 gradi o un’immagine e l’immagine viene ingrandita, l’immagine viene spostata in orizzontale. Se l’immagine viene spostata sul bordo della visualizzazione e lo scorrimento viene ancora eseguito in quella direzione, il movimento esegue uno scorrimento nativo della pagina. </p> <p> Scorre l’elenco dei campioni nella barra dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento o scorrimento verticale </p> </td> 
   <td colname="col2"> <p> Se lo stato dell’immagine è reimpostato, cambia l’angolo di visualizzazione verticale nel caso in cui venga utilizzato un set 360 gradi multidimensionale. In un set 360 gradi monodimensionale o quando un set 360 gradi multidimensionale si trova sull’ultimo o sul primo asse, in modo che lo scorrimento verticale non comporti una modifica dell’angolo di visualizzazione verticale, il movimento esegue lo scorrimento nativo della pagina. </p> <p> Quando la risorsa corrente è un set 360 gradi o un'immagine e l'immagine viene ingrandita, sposta l'immagine verticalmente. Se l’immagine viene spostata sul bordo della visualizzazione e lo scorrimento viene ancora eseguito in quella direzione, il movimento esegue lo scorrimento nativo della pagina. </p> <p> Se il movimento viene eseguito all’interno dell’area dei campioni, viene eseguito uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta anche l’input touch e il mouse su dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile da tastiera.

Vedi [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione di un visualizzatore di file multimediali diversi {#section-6bb5d3c502544ad18a58eafe12a13435}

Pagine web diverse hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina web fornisce un collegamento che, se selezionato, apre il visualizzatore in una finestra separata del browser. In altri casi, è necessario incorporare il diritto del visualizzatore nella pagina di hosting. In quest’ultimo caso, la pagina web può avere un layout di pagina statico o utilizzare un design reattivo che viene visualizzato in modo diverso su diversi dispositivi o per diverse dimensioni della finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: incorporazione a dimensione fissa e design reattivo.

## Informazioni sulla modalità a comparsa {#section-77d5aa03b8b94566958a179b1a2cd474}

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda separata del browser Web. Prende l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o se viene modificato l&#39;orientamento di un dispositivo mobile.

La modalità pop-up è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` Chiamata JavaScript configurata correttamente `A` Elemento HTML o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML predefinita per la modalità operativa a comparsa. In questo caso, si chiama [!DNL MixedMediaViewer.html] e si trova all&#39;interno del [!DNL html5/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Puoi ottenere la personalizzazione visiva applicando CSS personalizzati.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```html {.line-numbers}
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Informazioni sull’incorporazione di dimensioni fisse e design reattivo {#section-ec86b100ba5943d0b16694268520bbde}

Nella modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente, che potrebbe avere già alcuni contenuti del cliente non correlati al visualizzatore. Il visualizzatore normalmente occupa solo una parte del patrimonio immobiliare di una pagina web.

I casi d’uso principali sono le pagine web orientate ai desktop o ai dispositivi tablet, nonché le pagine di progettazione reattiva che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporazione a dimensione fissa viene utilizzata quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questa azione è la scelta migliore per le pagine web con layout statico.

L’incorporazione di design reattivo presuppone che il visualizzatore debba ridimensionare in fase di runtime in risposta alla modifica delle dimensioni del suo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

Nella modalità di incorporamento della progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa funzionalità assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura laterale. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout di progettazione reattiva come Bootstrap o Foundation.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza del contenitore del visualizzatore `DIV`, il visualizzatore riempie solo quell’area e ha le stesse dimensioni del layout della pagina web. Un buon esempio è quello di incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

## Incorporazione a dimensione fissa {#section-17d162f76ffa4804b27928f51e7bea1d}

Per aggiungere il visualizzatore a una pagina web, effettua le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione di HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL MixedMediaViewer.js]. La [!DNL MixedMediaViewer.js] si trova sotto [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene servito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
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

   Assicurati che la funzione a schermo intero funzioni correttamente in Internet Explorer. Controlla che non ci siano altri elementi nel DOM con un ordine di impilamento più alto del tuo segnaposto DIV.

   Di seguito è riportato un esempio di elemento DIV segnaposto definito:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore

   Questo visualizzatore visualizza le miniature quando si lavora con set di più elementi. Nei sistemi desktop, le miniature vengono posizionate sotto la vista principale. Allo stesso tempo, il visualizzatore consente lo scambio della risorsa principale durante il runtime utilizzando `setAsset()` API. In qualità di sviluppatore, puoi controllare come il visualizzatore gestisce l’area delle miniature in basso, quando la nuova risorsa ha un solo elemento. È possibile mantenere intatta la dimensione del visualizzatore esterno e lasciare che la vista principale aumenti la sua altezza e occupare l&#39;area delle miniature. Oppure, puoi mantenere statiche le dimensioni della visualizzazione principale e comprimere l’area del visualizzatore esterno, lasciando che il contenuto della pagina web si muova verso l’alto. Quindi, utilizza la proprietà immobiliare della pagina libera che è lasciata dalle miniature.

   Per mantenere intatti i limiti del visualizzatore esterno, definisci le dimensioni per `.s7mixedmediaviewer` classe CSS di primo livello in unità assolute. Le dimensioni in CSS possono essere posizionate direttamente sulla pagina HTML o in un file CSS per visualizzatori personalizzati e successivamente assegnate a un record predefinito per visualizzatori in Dynamic Media Classic oppure trasmesse in modo esplicito utilizzando il comando stile.

   Vedi [Personalizzazione del visualizzatore di file multimediali diversi](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione delle dimensioni statiche del visualizzatore esterno in una pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Puoi vedere il comportamento con un’area di visualizzazione esterna fissa nella pagina di esempio seguente. Quando si passa da un set all’altro, le dimensioni del visualizzatore esterno non cambiano:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-outer-area.html)

   Per rendere statiche le dimensioni della visualizzazione principale, definisci le dimensioni del visualizzatore in unità assolute per l&#39;interno `Container` Componente SDK che utilizza `.s7mixedmediaviewer .s7container` Selettore CSS, o utilizzando `stagesize` modificatore.

   Di seguito è riportato un esempio di definizione della dimensione del visualizzatore per l’interno `Container` Componente SDK in modo che l’area di visualizzazione principale non cambi le sue dimensioni quando si cambia risorsa:

   ```html {.line-numbers}
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La pagina di esempio seguente mostra il comportamento del visualizzatore con una dimensione di visualizzazione principale fissa. Quando si passa da un set all’altro, la visualizzazione principale rimane statica e il contenuto della pagina web si sposta in verticale:

   [https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/mixedmedia/MixedMediaViewer-fixed-main-view.html)

   È possibile impostare `stagesize` modificatore nel record predefinito visualizzatore in Dynamic Media Classic, oppure trasmettilo esplicitamente con il codice di inizializzazione del visualizzatore con `params` raccolta. Oppure, come chiamata API come descritto nella sezione Riferimento comando di questa Guida, come segue:

   ```html {.line-numbers}
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza di `s7viewers.MixedMediaViewer` , passare tutte le informazioni di configurazione al relativo costruttore e chiamare `init()` su un’istanza di visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere `containerId` campo che contiene il nome dell’ID contenitore visualizzatore e nidificato `params` Oggetto JSON con parametri di configurazione supportati dal visualizzatore. In questo caso, il `params` L&#39;oggetto deve avere almeno l&#39;URL Image Server passato come `serverUrl` , l&#39;URL del server video viene passato come `videoserverurl` e la risorsa iniziale come `asset` parametro . L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il `init()` metodo immediatamente prima della chiusura `BODY` o sul corpo `onload()` evento.

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. Quando si verifica questa azione, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del `init()` metodo . L&#39;esempio presuppone `mixedMediaViewer` è l’istanza visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; [!DNL http://s7d1.scene7.com/is/image/] è l’URL di Image Server; [!DNL http://s7d1.scene7.com/is/content/] è l’URL del server video; e [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] è la risorsa:

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

Il codice seguente è un esempio completo di una pagina web semplice che incorpora il visualizzatore di file multimediali diversi con dimensioni fisse:

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

## Incorporazione reattiva con altezza illimitata {#section-056cb574713c4d07be6d07cf3c598839}

Con l’incorporazione di design reattivo, la pagina web dispone normalmente di un layout flessibile che determina le dimensioni di runtime del contenitore del visualizzatore `DIV`. Nell’esempio seguente, si supponga che la pagina web consenta il contenitore del visualizzatore `DIV` per prendere il 40% delle dimensioni della finestra del browser web, lasciando la sua altezza senza restrizioni. Il codice HTML della pagina web sarà simile al seguente:

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

L’aggiunta del visualizzatore a una pagina di questo tipo è simile alla procedura per l’incorporazione a dimensione fissa. L’unica differenza è che non è necessario definire esplicitamente la dimensione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell&#39;incorporazione con dimensione fissa. Aggiungi il DIV del contenitore all’esistente `"holder"` DIV Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

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

La pagina degli esempi seguenti illustra gli utilizzi più reali dell’incorporazione di design reattivo a altezza illimitata:

[Demo live](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

[Posizione demo alternativa](https://experienceleague.adobe.com/tools/dynamic-media-demo/vlist/vlist.html)

## Incorporazione di dimensioni flessibili con larghezza e altezza definite {#section-0a329016f9414d199039776645c693de}

Se è definito un tipo di incorporamento a dimensioni flessibili con larghezza e altezza, lo stile della pagina web è diverso. Fornisce entrambe le dimensioni al `"holder"` DIV e lo centra nella finestra del browser. Inoltre, la pagina web imposta le dimensioni del `HTML` e `BODY` al 100%.

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

Gli altri passaggi di incorporamento sono identici ai passaggi utilizzati per incorporare design reattivo con altezza illimitata. L’esempio risultante è il seguente:

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

## Incorporazione tramite API basate su Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L’utilizzo di questo costruttore API non richiede alcun parametro e i parametri di configurazione specificati utilizzano `setContainerId()`, `setParam()`e `setAsset()` Metodi API, con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con l’API basata su setter:

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
