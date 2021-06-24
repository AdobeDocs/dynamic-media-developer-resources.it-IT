---
description: Il visualizzatore Carosello è un carosello di immagini banner non zoomabili con punti attivi o aree geografiche selezionabili. Lo scopo di questo visualizzatore è quello di implementare un’esperienza "carosello acquistabile" in cui gli utenti possono selezionare un punto attivo o una regione sull’immagine del banner e venire reindirizzati a una pagina Quickview o dettagli prodotto sul sito web del cliente. È progettato per funzionare su desktop e dispositivi mobili.
solution: Experience Manager
title: Carosello
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Banner carosello
role: Developer,Business Practitioner
exl-id: d506dc6e-8929-4f7f-a205-1683e77681f1
source-git-commit: e6ff4ed80b22e10fc2bd3fac0f4e39bbf5148f8e
workflow-type: tm+mt
source-wordcount: '1902'
ht-degree: 0%

---

# Carosello{#carousel}

Il visualizzatore Carosello è un carosello di immagini banner non zoomabili con punti attivi o aree geografiche selezionabili. Lo scopo di questo visualizzatore è quello di implementare un’esperienza &quot;carosello acquistabile&quot; in cui gli utenti possono selezionare un punto attivo o una regione sull’immagine del banner e venire reindirizzati a una pagina Quickview o dettagli prodotto sul sito web del cliente. È progettato per funzionare su desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano il rendering delle immagini o il contenuto generato dall’utente (UGC) non sono supportate da questo visualizzatore.

Il tipo di visualizzatore è 511.

## URL demo {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewerDemo.html)

## Requisiti di sistema {#section-b7270cc4290043399681dc504f043609}

Vedere [Requisiti di sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilizzo del visualizzatore Carosello {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore Carosello rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Il visualizzatore Carosello può essere utilizzato sia in modalità pop-up utilizzando una pagina HTML pronta per la produzione fornita con i visualizzatori IS, o in modalità incorporata in cui è integrato nella pagina web di destinazione utilizzando un’API documentata.

La configurazione e lo skin sono simili a quelli degli altri visualizzatori descritti in questa Guida. Tutta la skin viene ottenuta tramite CSS personalizzati.

Consulta [Riferimento ai comandi comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento ai comandi comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore Carosello {#section-642e66ca38cd4032992840ec6c0b0cd2}

La navigazione all’interno del set carosello viene eseguita con un passaggio orizzontale sulla vista principale o con due pulsanti freccia disponibili sul dispositivo desktop. I puntini dell&#39;indicatore mostrano la posizione corrente all&#39;interno del set.

Il visualizzatore può eseguire il rendering di punti attivi o aree geografiche sopra l’immagine del banner per indicare l’area interattiva sul prodotto.

Quando si tocca o fai clic su un punto attivo o su una regione, viene attivata un’azione associata durante il momento dell’authoring. L’azione può essere reindirizzata a una pagina diversa del sito web oppure può restituire le informazioni sul prodotto alla logica della pagina web, che a sua volta può attivare una visualizzazione rapida con il contenuto del prodotto correlato.

Il visualizzatore è completamente accessibile da tastiera.

Consulta [Accesso facilitato alla tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore Carosello {#section-6bb5d3c502544ad18a58eafe12a13435}

**Informazioni sulla modalità a comparsa**

In modalità pop-up, il visualizzatore viene aperto in una finestra o scheda separata del browser Web. Prende l&#39;intera area della finestra del browser e si regola nel caso in cui il browser venga ridimensionato o se viene modificato l&#39;orientamento di un dispositivo mobile.

La modalità pop-up è la più comune per i dispositivi mobili. La pagina web carica il visualizzatore utilizzando `window.open()` una chiamata JavaScript, un elemento `A` HTML configurato correttamente o qualsiasi altro metodo appropriato.

Si consiglia di utilizzare una pagina HTML predefinita per la modalità operativa a comparsa. In questo caso, si chiama `CarouselViewer.html` e si trova all’interno della sottocartella `html5/` della distribuzione standard IS-Viewers:

`<s7viewers_root>/html5/CarouselViewer.html`

Puoi ottenere la personalizzazione visiva applicando CSS personalizzati.

Di seguito è riportato un esempio di codice HTML che apre il visualizzatore in una nuova finestra:

```
<a href="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/CarouselViewer.html?asset=/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner&serverurl=https://adobedemo62-h.assetsadobe.com/is/image" target="_blank">Open popup viewer</a>
```

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento della progettazione reattiva**

Nella modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente. Questa pagina web potrebbe avere già alcuni contenuti del cliente non correlati al visualizzatore. Il visualizzatore normalmente occupa solo una parte del patrimonio immobiliare di una pagina web.

I casi d’uso principali sono le pagine web orientate ai desktop o ai dispositivi tablet e le pagine responsive progettate che regolano automaticamente il layout in base al tipo di dispositivo.

L’incorporazione a dimensione fissa viene utilizzata quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questa è la scelta migliore per le pagine web con layout statico.

L’incorporazione di design reattivo presuppone che il visualizzatore debba ridimensionare in fase di runtime in risposta alla modifica delle dimensioni del contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

Nella modalità di incorporamento della progettazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il proprio contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando senza limitazioni l’altezza, il visualizzatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa funzionalità assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura laterale. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout di progettazione web reattivo come Bootstrap, Foundation e così via.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza del contenitore del visualizzatore `DIV`, il visualizzatore riempie solo quell’area. Segue anche le dimensioni fornite dal layout della pagina web. Un buon esempio è quello di incorporare il visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina web, effettua le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   La creazione di un visualizzatore richiede l’aggiunta di un tag script nell’intestazione HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL CarouselViewer.js]. Il file [!DNL CarouselViewer.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Dynamic Media Classic di Adobe e viene servito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Dynamic Media Classic di Adobe in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script>
```

>[!NOTE]
>
>Dovresti fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non devi fare riferimento a file JavaScript aggiuntivi nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente alla libreria HTML5 SDK `Utils.js` caricata dal visualizzatore dal percorso contestuale `/s7viewers` (cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o librerie di visualizzatori runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. Adobe non conserva le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, l’inserimento di un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore `DIV`.

   Aggiungi un elemento `DIV` vuoto alla pagina in cui desideri visualizzare il visualizzatore. L’ID dell’elemento `DIV` deve essere definito, perché viene passato successivamente all’API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il segnaposto `DIV` è un elemento posizionato, il che significa che la proprietà CSS `position` è impostata su `relative` o `absolute`.

   Di seguito è riportato un esempio di un elemento segnaposto definito `DIV`:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica del visualizzatore dichiarandola per la classe CSS di livello superiore `.s7carouselviewer` in unità assolute o utilizzando il modificatore `stagesize`.

   Puoi inserire le dimensioni in CSS direttamente nella pagina HTML o in un file CSS per visualizzatori personalizzati, che viene poi assegnato a un record predefinito per visualizzatori in AEM Assets - on-demand, o passato esplicitamente utilizzando il comando `style` .

   Per ulteriori informazioni sullo stile del visualizzatore con CSS, consulta [Personalizzazione del visualizzatore carosello](../../c-html5-aem-asset-viewers/c-html5-aem-carousel/c-html5-aem-carousel-customizingviewer/c-html5-aem-carousel-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) .

   Di seguito è riportato un esempio di definizione delle dimensioni di un visualizzatore statico nella pagina HTML:

   ```
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Puoi passare esplicitamente il modificatore `stagesize` con il codice di inizializzazione del visualizzatore con la raccolta `params` o come chiamata API come descritto nella sezione Riferimento comandi , come segue:

   ```
   carouselViewer.setParam("stagesize", "1174,500");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, crea un’istanza della classe `s7viewers.CarouselViewer`, passa tutte le informazioni di configurazione al relativo costruttore e chiama il metodo `init()` su un’istanza di visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere un campo `containerId` che contiene il nome dell’ID del contenitore del visualizzatore e un oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore. In questo caso, l’oggetto `params` deve avere almeno l’URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser rinviano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()` .

   Allo stesso tempo, l’elemento contenitore non deve necessariamente far parte del layout della pagina web per ora. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza di visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del metodo `init()` . L’esempio presuppone che `carouselViewer` sia l’istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; `https://adobedemo62-h.assetsadobe.com/is/image` è l&#39;URL di Image Server e `/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner` è la risorsa:

   ```
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script>
   ```

   Il codice seguente è un esempio completo di una pagina web banale che incorpora il visualizzatore Carosello con dimensioni fisse:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7carouselviewer { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var carouselViewer = new s7viewers.CarouselViewer({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
    "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html>
   ```

**Incorporazione di design reattivo con altezza illimitata**

Con l’incorporazione di design reattivo, la pagina web dispone normalmente di un layout flessibile che determina le dimensioni di runtime del contenitore del visualizzatore `DIV`. Nell’esempio seguente, si supponga che la pagina web consenta al contenitore del visualizzatore `DIV` di assumere il 40% delle dimensioni della finestra del browser Web. E la sua altezza è lasciata senza restrizioni. Il codice HTML della pagina web sarà simile al seguente:

```
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

L’aggiunta del visualizzatore a una pagina di questo tipo è simile alla procedura per l’incorporazione a dimensione fissa. L’unica differenza è che non è necessario definire esplicitamente la dimensione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell&#39;incorporazione con dimensione fissa. Aggiungi il contenitore `DIV` al `"holder"` `DIV` esistente. Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

La pagina degli esempi seguenti illustra gli utilizzi più reali dell’incorporazione di design reattivo a altezza illimitata:

[https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/viewers-ref/carousel/CarouselViewer-responsive-unrestricted-height.html)

**Dimensione flessibile Incorporamento con definizione di larghezza e altezza**

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

Gli altri passaggi di incorporamento sono identici ai passaggi utilizzati per l’incorporazione reattiva con altezza illimitata. L’esempio risultante è il seguente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
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
var carouselViewer = new s7viewers.CarouselViewer({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner", 
 "serverurl":"https://adobedemo62-h.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html>
```

**Incorporazione tramite API basate su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L’utilizzo di questo costruttore API non accetta alcun parametro e i parametri di configurazione vengono specificati utilizzando i metodi `setContainerId()`, `setParam()` e `setAsset()` API con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con l’API basata su setter:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="https://demos-pub.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/CarouselViewer.js"></script> 
<style type="text/css"> 
#s7viewer.s7carouselviewer { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var carouselViewer = new s7viewers.CarouselViewer(); 
carouselViewer.setContainerId("s7viewer"); 
carouselViewer.setParam("serverurl", "https://adobedemo62-h.assetsadobe.com/is/image"); 
carouselViewer.setAsset("/content/dam/dm-public-facing-live-demo-page/04_shoppable_carousel/05_shoppable_banner"); 
carouselViewer.init(); 
</script> 
</body> 
</html>
```
