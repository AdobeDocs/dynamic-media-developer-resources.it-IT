---
description: Il visualizzatore per file multimediali diversi è un visualizzatore per contenuti multimediali. Supporta i set di file multimediali che contengono immagini, set di campioni, set 360 gradi, video e set video adattivi.
keywords: responsive
seo-description: Il visualizzatore per file multimediali diversi è un visualizzatore per contenuti multimediali. Supporta i set di file multimediali che contengono immagini, set di campioni, set 360 gradi, video e set video adattivi.
seo-title: Supporti multipli
solution: Experience Manager
title: Supporti multipli
topic: Dynamic media
uuid: b6028c54-7a3c-41eb-89f8-7b86bb0d0deb
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2681'
ht-degree: 0%

---


# Supporti multipli{#mixed-media}

Il visualizzatore per file multimediali diversi è un visualizzatore per contenuti multimediali. Supporta i set di file multimediali che contengono immagini, set di campioni, set 360 gradi, video e set video adattivi.

Una miniatura nella parte inferiore del visualizzatore rappresenta ciascun elemento del set di file multimediali, insieme all’indicatore del tipo di risorsa. Quando è selezionato un elemento set di campioni, viene visualizzata una riga secondaria di campioni per consentire la selezione della variazione di colore all’interno del set di campioni. Immagini e set di campioni supportano lo zoom in modalità continua o in linea; i set 360 gradi supportano sia lo zoom che la rotazione. I video e i set video adattivi supportano tutti i controlli di riproduzione di base, purché vengano visualizzati eventuali sottotitoli codificati facoltativi sopra al contenuto video. Un utente può passare allo schermo intero in qualsiasi momento facendo clic sul pulsante a schermo intero. Il visualizzatore dispone di un pulsante di chiusura opzionale. È progettato per funzionare su computer desktop e dispositivi mobili.

Il visualizzatore per file multimediali diversi utilizza la riproduzione di video in streaming HTML5 in formato HLS nella configurazione predefinita ogni volta che il sistema sottostante lo supporta. Sui sistemi che non supportano lo streaming HTML5, il visualizzatore torna alla distribuzione video progressiva HTML5.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Tipo di visualizzatore 505.

Vedere [Requisiti di sistema e prerequisiti](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## URL demo {#section-e1c3106f5b3e445d9b95be337c2f94e2}

[https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample](https://s7d9.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample)

## Utilizzo del visualizzatore per file multimediali diversi {#section-f21ac23d3f6449ad9765588d69584772}

Il visualizzatore di file multimediali diversi rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Potete usare il visualizzatore per file multimediali diversi in modalità a comparsa utilizzando la pagina HTML pronta per la produzione fornita con i visualizzatori IS. Oppure, potete utilizzare il visualizzatore in modalità incorporata, dove viene integrato in una pagina Web di destinazione tramite l&#39;API documentata.

La configurazione e l’associazione di interfacce al visualizzatore sono simili agli altri visualizzatori. L’associazione di interfacce viene realizzata tramite CSS personalizzato.

Consultate [Riferimento comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore di file multimediali diversi {#section-ab66eb6955aa4a8aa6d14a3b3acfed3f}

Il visualizzatore per file multimediali diversi supporta i gesti touch singola e multi-touch comuni in altre applicazioni mobili. Quando il visualizzatore non è in grado di elaborare il gesto di scorrimento di un utente, inoltra l&#39;evento al browser Web per eseguire uno scorrimento nativo della pagina. Questa funzionalità consente a un utente di navigare nella pagina anche se il visualizzatore occupa la maggior parte dell&#39;area dello schermo del dispositivo.

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
   <td colname="col1"> <p>Doppio tocco </p> </td> 
   <td colname="col2"> <p>In modalità <span class="codeph"> zoom continua </span>, lo zoom viene effettuato di un livello fino a raggiungere l'ingrandimento massimo; il doppio tocco successivo viene ripristinato allo stato iniziale. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Tocco e tenere premuto </p> </td> 
   <td colname="col2"> <p> In modalità <span class="codeph"> zoom in linea </span>, attiva l'immagine ingrandita. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Pizzico </p> </td> 
   <td colname="col2"> <p>In modalità zoom continuo, ingrandisce o ingrandisce l’immagine. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento o scorrimento orizzontale </p> </td> 
   <td colname="col2"> <p> Quando la risorsa corrente è un set 360 gradi e l’immagine è in stato di reimpostazione, viene ruotata nel set 360 gradi in orizzontale. </p> <p> Quando la risorsa corrente è un set 360 gradi o un’immagine e l’immagine viene ingrandita, l’immagine viene spostata in orizzontale. Se l’immagine viene spostata sul bordo della visualizzazione e lo scorrimento avviene ancora in quella direzione, il gesto esegue uno scorrimento nativo della pagina. </p> <p> Consente di scorrere l’elenco dei campioni nella barra dei campioni. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Scorrimento o scorrimento verticale </p> </td> 
   <td colname="col2"> <p> Se l’immagine è in stato di reimpostazione, cambia l’angolo di visualizzazione verticale se viene utilizzato un set 360 gradi multidimensionale. In un set 360 gradi monodimensionale, o quando un set 360 gradi multidimensionale si trova sull’ultimo o sul primo asse, in modo che lo scorrimento verticale non comporti la modifica dell’angolo di visualizzazione verticale, il gesto esegue lo scorrimento nativo della pagina. </p> <p> Quando la risorsa corrente è un set 360 gradi o un’immagine e l’immagine viene ingrandita, sposta l’immagine verticalmente. Se l’immagine viene spostata sul bordo della visualizzazione e lo scorrimento continua in quella direzione, il gesto esegue lo scorrimento nativo della pagina. </p> <p> Se il gesto viene eseguito all’interno dell’area dei campioni, viene eseguito uno scorrimento nativo della pagina. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il visualizzatore supporta inoltre l&#39;input touch e l&#39;input del mouse sui dispositivi Windows con touch screen e mouse. Questo supporto, tuttavia, è limitato solo ai browser Web Chrome, Internet Explorer 11 e Edge.

Questo visualizzatore è completamente accessibile tramite tastiera.

Vedere [Accessibilità e navigazione da tastiera](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore per file multimediali diversi {#section-6bb5d3c502544ad18a58eafe12a13435}

Diverse pagine Web hanno esigenze diverse per il comportamento del visualizzatore. A volte una pagina Web fornisce un collegamento che, quando viene fatto clic su di essa, apre il visualizzatore in una finestra browser separata. In altri casi, è necessario incorporare il visualizzatore direttamente nella pagina di hosting. In quest&#39;ultimo caso, la pagina Web potrebbe avere un layout di pagina statico oppure utilizzare un design reattivo che viene visualizzato in modo diverso su dispositivi diversi o per diverse dimensioni di finestra del browser. Per soddisfare queste esigenze, il visualizzatore supporta tre modalità di funzionamento principali: incorporazione a comparsa, dimensione fissa e incorporazione reattiva del design.

## Informazioni sulla modalità a comparsa {#section-77d5aa03b8b94566958a179b1a2cd474}

In modalità pop-up, il visualizzatore viene aperto in una finestra o in una scheda separata del browser Web. Richiede l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato, o se l&#39;orientamento di un dispositivo mobile viene modificato.

La modalità a comparsa è la più comune per i dispositivi mobili. La pagina Web carica il visualizzatore utilizzando la chiamata `window.open()` JavaScript, l&#39;elemento HTML configurato correttamente `A` o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML out-of-the-box per la modalità operativa a comparsa. In questo caso, si chiama [!DNL MixedMediaViewer.html] e si trova nella sottocartella [!DNL html5/] della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/MixedMediaViewer.html]

Potete ottenere la personalizzazione visiva applicando CSS personalizzato.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
<a href="http://s7d1.scene7.com/s7viewers/html5/MixedMediaViewer.html?asset=Scene7SharedAssets/Mixed_Media_Set_Sample" target="_blank">Open popup viewer</a>
```

## Informazioni sulle dimensioni fisse e sull&#39;incorporamento reattivo della progettazione {#section-ec86b100ba5943d0b16694268520bbde}

In modalità incorporata, il visualizzatore viene aggiunto alla pagina Web esistente, che potrebbe già presentare contenuti per clienti non correlati al visualizzatore. In genere, il visualizzatore occupa solo una parte del patrimonio immobiliare di una pagina Web.

I casi d’uso principali sono le pagine Web orientate per computer desktop o dispositivi tablet e le pagine di progettazione reattiva che adattano automaticamente il layout in base al tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica la dimensione dopo il caricamento iniziale. Questa è la scelta migliore per le pagine Web con layout statico.

L&#39;incorporazione reattiva della progettazione presuppone che il visualizzatore debba ridimensionare in fase di esecuzione in seguito alla modifica delle dimensioni del suo contenitore `DIV`. L’esempio più comune è l’aggiunta di un visualizzatore a una pagina Web con layout di pagina flessibile.

In modalità di incorporazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina Web ridimensiona il contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente l’altezza in base alle proporzioni della risorsa utilizzata. Questa funzione assicura che la risorsa si adatti perfettamente alla vista senza riempimenti laterali. Questo caso di utilizzo è il più comune per le pagine Web che utilizzano framework di layout reattivi come Bootstrap, Foundation e così via.

In caso contrario, se la pagina Web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore riempie solo tale area e ha le stesse dimensioni del layout della pagina Web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser Web.

## Incorporazione dimensione fissa {#section-17d162f76ffa4804b27928f51e7bea1d}

Per aggiungere il visualizzatore a una pagina Web, effettuate le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell&#39;intestazione HTML. Prima di poter utilizzare l&#39;API del visualizzatore, accertatevi di includere [!DNL MixedMediaViewer.js]. Il file [!DNL MixedMediaViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/html5/js/MixedMediaViewer.js]

Potete utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Scene7  e viene distribuito dallo stesso dominio. In caso contrario, specificate un percorso completo per uno  server Adobe Scene7 in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/s7viewers/html5/js/MixedMediaViewer.js"></script>
```

>[!NOTE]
>
>È consigliabile fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non dovete fare riferimento ad altri file JavaScript nel codice della pagina Web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fate riferimento direttamente alla libreria HTML5 SDK `Utils.js` caricata dal visualizzatore dal percorso contestuale `/s7viewers` (il cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o librerie di visualizzatori runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore.  Adobe non conserva sul server versioni precedenti del visualizzatore secondario `includes`.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi codice JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina, si interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione di prodotto.

1. Definizione del contenitore DIV.

   Aggiungete un elemento DIV vuoto alla pagina in cui desiderate visualizzare il visualizzatore. L&#39;ID dell&#39;elemento DIV deve essere definito perché l&#39;ID viene passato successivamente all&#39;API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il segnaposto DIV è un elemento posizionato, il che significa che la proprietà `position` CSS è impostata su `relative` o `absolute`.

   Assicurarsi che la funzione a schermo intero funzioni correttamente in Internet Explorer. Verificate che nel DOM non vi siano altri elementi con un ordine di sovrapposizione superiore a quello del DIV segnaposto.

   Esempio di un elemento DIV segnaposto definito:

   ```
   <div id="s7viewer" style="position:relative"></div> 
   ```

1. Impostazione delle dimensioni del visualizzatore

   Questo visualizzatore visualizza le miniature quando si utilizzano i set di più elementi. Sui sistemi desktop, le miniature vengono posizionate sotto la vista principale. Allo stesso tempo, il visualizzatore consente di scambiare la risorsa principale durante l&#39;esecuzione utilizzando l&#39;API `setAsset()`. In qualità di sviluppatore, potete controllare in che modo il visualizzatore gestisce l’area delle miniature in basso quando la nuova risorsa dispone di un solo elemento. È possibile mantenere intatte le dimensioni del visualizzatore esterno e lasciare che la vista principale ne aumenti l’altezza e occupi l’area delle miniature. In alternativa, potete mantenere statiche le dimensioni di visualizzazione principale e comprimere l’area del visualizzatore esterno, consentendo al contenuto della pagina Web di spostarsi verso l’alto e quindi utilizzare lo spazio disponibile sulla pagina gratuita che è rimasto dalle miniature.

   Per mantenere intatti i limiti del visualizzatore esterno, definite le dimensioni della classe CSS di livello principale `.s7mixedmediaviewer` in unità assolute. Il ridimensionamento in CSS può essere inserito direttamente nella pagina HTML o in un file CSS del visualizzatore personalizzato, che verrà successivamente assegnato a un record di predefinito per visualizzatori in Scene7 Publishing System, oppure trasmesso in modo esplicito tramite il comando stile.

   Consultate [Personalizzazione del visualizzatore di file multimediali diversi](../../c-html5-s7-aem-asset-viewers/c-html5-mixedmedia-viewer-about/c-html5-mixedmedia-viewer-customizingviewer/c-html5-mixedmedia-viewer-customizingviewer.md#concept-61b3410f187c4bf3af09ec813c649bf4) per ulteriori informazioni sullo stile del visualizzatore con i CSS.

   Di seguito è riportato un esempio di definizione delle dimensioni statiche del visualizzatore esterno in una pagina HTML:

   ```
   #s7viewer.s7mixedmediaviewer { 
    width: 640px; 
    height: 480px; 
   }
   ```

   Potete visualizzare il comportamento con un’area fissa del visualizzatore esterno sulla pagina di esempio seguente. Tenete presente che quando passate da un set all’altro, le dimensioni del visualizzatore esterno non cambiano:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-outer-area.html)

   Per rendere statiche le dimensioni di visualizzazione principali, definite le dimensioni del visualizzatore in unità assolute per il componente SDK interno `Container` utilizzando il selettore CSS `.s7mixedmediaviewer .s7container` o utilizzando il modificatore `stagesize`.

   Di seguito è riportato un esempio di definizione delle dimensioni del visualizzatore per il componente SDK interno `Container` in modo che l&#39;area di visualizzazione principale non cambi le dimensioni quando si passa da una risorsa all&#39;altra:

   ```
   #s7viewer.s7mixedmediaviewer .s7container { 
    width: 640px; 
    height: 480px; 
   }
   ```

   La pagina di esempio seguente mostra il comportamento del visualizzatore con una dimensione di visualizzazione principale fissa. Quando passate da un set all’altro, la vista principale rimane statica e il contenuto della pagina Web si sposta in verticale:

   [https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html](https://marketing.adobe.com/resources/help/en_US/s7/viewers_ref/samples/MixedMediaViewer-fixed-main-view.html)

   Potete impostare il modificatore `stagesize` nel record del predefinito per visualizzatori in Scene7 Publishing System, oppure passarlo esplicitamente con il codice di inizializzazione del visualizzatore con la raccolta `params` oppure come chiamata API come descritto nella sezione Riferimento comandi di questa guida, come segue:

   ```
   mixedMediaViewer.setParam("stagesize", "640,480");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi descritti qui sopra, potete creare un&#39;istanza della classe `s7viewers.MixedMediaViewer`, trasmettere tutte le informazioni di configurazione al relativo costruttore e chiamare il metodo `init()` su un&#39;istanza di visualizzatore. Le informazioni di configurazione vengono trasmesse al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere il campo `containerId` che contiene il nome dell&#39;ID contenitore del visualizzatore e l&#39;oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore. In questo caso, l&#39;oggetto `params` deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl`, l&#39;URL del server video passato come proprietà `videoserverurl` e la risorsa iniziale come parametro `asset`. L&#39;API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore del visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser ritardano la creazione del DOM fino alla fine della pagina Web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()`.

   Allo stesso tempo, l&#39;elemento contenitore non deve necessariamente far parte del layout della pagina Web. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del metodo `init()`. L&#39;esempio presuppone che `mixedMediaViewer` sia l&#39;istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; [!DNL http://s7d1.scene7.com/is/image/] è l&#39;URL del server immagini; [!DNL http://s7d1.scene7.com/is/content/] è l&#39;URL del server video; e [!DNL Scene7SharedAssets/Mixed_Media_Set_Sample] è la risorsa:

```
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

Il codice seguente è un esempio completo di una pagina Web di dimensioni ridotte che incorpora il visualizzatore di file multimediali diversi con dimensioni fisse:

```
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

Con l&#39;incorporazione reattiva della progettazione, la pagina Web dispone in genere di un layout flessibile che specifica le dimensioni runtime del contenitore del visualizzatore `DIV`. Nell&#39;esempio seguente, si supponga che la pagina Web consenta al contenitore del visualizzatore `DIV` di assumere il 40% delle dimensioni della finestra del browser Web, lasciando invariata l&#39;altezza. Il codice HTML della pagina Web sarà simile al seguente:

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

L’aggiunta del visualizzatore a tale pagina è simile alla procedura per l’incorporamento a dimensione fissa. L’unica differenza è che non è necessario definire in modo esplicito le dimensioni del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore DIV.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi indicati sopra sono uguali a quelli con l&#39;incorporamento a dimensione fissa. Aggiungete il DIV contenitore al DIV `"holder"` esistente. Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

```
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

La pagina degli esempi seguente illustra gli usi più reali dell’incorporamento reattivo di design con altezza illimitata:

[Live Demos](https://landing.adobe.com/en/na/dynamic-media/ctir-2755/live-demos.html)

<!-- KEEP (https://marketing.adobe.com/resources/help/en_US/s7/vlist/vlist.html) -->

## Incorporazione di dimensioni flessibili con larghezza e altezza definita {#section-0a329016f9414d199039776645c693de}

In caso di incorporamento di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina Web è diverso. Fornisce entrambe le dimensioni al DIV `"holder"` e lo centra nella finestra del browser. Inoltre, la pagina Web imposta la dimensione dell&#39;elemento `HTML` e `BODY` su 100%.

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

## Incorporazione tramite l&#39;API basata su Setter {#section-af26f0cc2e5140e8a9bfd0c6a841a6d1}

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L&#39;utilizzo di questo costruttore API non accetta parametri e i parametri di configurazione vengono specificati utilizzando i metodi API `setContainerId()`, `setParam()` e `setAsset()`, con chiamate JavaScript separate.

L&#39;esempio seguente illustra l&#39;utilizzo dell&#39;incorporamento a dimensione fissa con l&#39;API basata su setter:

```
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

