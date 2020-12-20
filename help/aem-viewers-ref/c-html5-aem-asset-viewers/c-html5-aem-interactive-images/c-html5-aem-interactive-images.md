---
description: Interactive Image Viewer è un visualizzatore che visualizza una singola immagine non zoomabile con punti attivi cliccabili. Lo scopo di questo visualizzatore è quello di implementare un'esperienza "banner acquistabile". In altre parole, l'utente può selezionare un punto di attivazione sull'immagine del banner e passare a una pagina di visualizzazione rapida o di dettaglio del prodotto sul sito Web. È progettato per funzionare su computer desktop e dispositivi mobili.
seo-description: Interactive Image Viewer è un visualizzatore che visualizza una singola immagine non zoomabile con punti attivi cliccabili. Lo scopo di questo visualizzatore è quello di implementare un'esperienza "banner acquistabile". In altre parole, l'utente può selezionare un punto di attivazione sull'immagine del banner e passare a una pagina di visualizzazione rapida o di dettaglio del prodotto sul sito Web. È progettato per funzionare su computer desktop e dispositivi mobili.
seo-title: Immagine interattiva
solution: Experience Manager
title: Immagine interattiva
topic: Dynamic media
uuid: 18b7a0c3-c047-4ce1-8920-1d8ebc1ab60e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---


# Immagine interattiva{#interactive-image}

Interactive Image Viewer è un visualizzatore che visualizza una singola immagine non zoomabile con punti attivi cliccabili. Lo scopo di questo visualizzatore è quello di implementare un&#39;esperienza &quot;banner acquistabile&quot;. In altre parole, l&#39;utente può selezionare un punto di attivazione sull&#39;immagine del banner e passare a una pagina di visualizzazione rapida o di dettaglio del prodotto sul sito Web. È progettato per funzionare su computer desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Il tipo di visualizzatore è 508.

## URL demo {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage.html)

## Requisiti di sistema {#section-b7270cc4290043399681dc504f043609}

Vedere [Requisiti di sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilizzo del visualizzatore immagini interattivo {#section-e6c68406ecdc4de781df182bbd8088b4}

Il visualizzatore immagini interattivo rappresenta un file JavaScript principale e un set di file helper (un singolo JavaScript include tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Il visualizzatore immagini interattivo può essere utilizzato solo in modalità incorporata, dove viene integrato nella pagina Web di destinazione tramite l’API documentata.

La configurazione e l’interfaccia sono simili a quelle degli altri visualizzatori descritti in questa guida. L’associazione di interfacce viene realizzata tramite CSS personalizzato.

Consultate [Riferimento comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore immagini interattivo {#section-642e66ca38cd4032992840ec6c0b0cd2}

L’interazione supportata dal visualizzatore di immagini video è l’attivazione dei punti di attivazione sui sistemi desktop. Questa attivazione si verifica su dispositivi touch con un solo tocco.

Il visualizzatore è completamente accessibile tramite tastiera.

Vedere [Accessibilità e navigazione da tastiera](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore immagini interattivo {#section-6bb5d3c502544ad18a58eafe12a13435}

Interactive Image Viewer è progettato per essere incorporato nella pagina host. Una pagina Web di questo tipo può avere un layout statico, oppure essere &quot;reattiva&quot; e visualizzata in modo diverso su dispositivi diversi o per diverse dimensioni di finestra del browser.

Per soddisfare queste esigenze, il visualizzatore supporta due modalità di funzionamento principali: incorporazione a dimensione fissa e incorporazione reattiva.

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina Web esistente. Questa pagina Web potrebbe già avere del contenuto cliente non correlato al visualizzatore. In genere, il visualizzatore occupa solo una parte del patrimonio immobiliare di una pagina Web.

I casi d’uso principali sono le pagine Web orientate per computer desktop o dispositivi tablet e le pagine reattive progettate per regolare automaticamente il layout in base al tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica la dimensione dopo il caricamento iniziale. Questa è la scelta migliore per le pagine Web con layout statico.

L&#39;incorporazione reattiva della progettazione presuppone che il visualizzatore debba ridimensionare in fase di esecuzione in seguito alla modifica delle dimensioni del suo contenitore `DIV`. L’esempio più comune è l’aggiunta di un visualizzatore a una pagina Web con layout di pagina flessibile.

In modalità di incorporazione reattiva, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina Web ridimensiona il contenitore `DIV`. Se la pagina Web imposta solo la larghezza del contenitore `DIV`, lasciando senza restrizioni l’altezza, il visualizzatore sceglie automaticamente l’altezza in base alle proporzioni della risorsa utilizzata. Questa funzione assicura che la risorsa si adatti perfettamente alla vista senza riempimenti laterali. Questo caso di utilizzo è il più comune per le pagine Web che utilizzano framework di layout reattivi per la progettazione Web come Bootstrap, Foundation e così via.

In caso contrario, se la pagina Web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore riempie solo tale area. Segue anche la dimensione fornita dal layout della pagina Web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser Web.

**Incorporazione a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuate le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina Web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell&#39;intestazione HTML. Prima di poter utilizzare l&#39;API del visualizzatore, accertatevi di includere [!DNL InterativeImage.js]. Il file [!DNL InteractiveImage.js] si trova nella sottocartella [!DNL html5/js/] della distribuzione standard dei visualizzatori IS:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Potete utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Dynamic Media Classic  Adobe e viene distribuito dallo stesso dominio. In caso contrario, specificate un percorso completo per uno dei server Dynamic Media Classic  Adobe in cui sono installati i visualizzatori IS.

Il percorso relativo si presenta come segue:

```
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>È consigliabile fare riferimento solo al file JavaScript del visualizzatore principale `include` nella pagina. Non dovete fare riferimento ad altri file JavaScript nel codice della pagina Web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fate riferimento direttamente alla libreria HTML5 SDK `Utils.js` caricata dal visualizzatore dal percorso contestuale `/s7viewers` (il cosiddetto SDK consolidato `include`). Il motivo è che la posizione di `Utils.js` o librerie di visualizzatori runtime simili è completamente gestita dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore.  Adobe non conserva sul server versioni precedenti del visualizzatore secondario `includes`.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi codice JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina, si interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione di prodotto.

1. Definizione del contenitore `DIV`.

   Aggiungete un elemento `DIV` vuoto alla pagina in cui desiderate visualizzare il visualizzatore. L&#39;ID dell&#39;elemento `DIV` deve essere definito perché l&#39;ID viene passato successivamente all&#39;API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Il segnaposto `DIV` è un elemento posizionato, il che significa che la proprietà `position` CSS è impostata su `relative` o `absolute`.

   Di seguito è riportato un esempio di un elemento segnaposto definito `DIV`:

   ```
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   Potete impostare le dimensioni statiche per il visualizzatore dichiarandolo per la classe CSS di livello principale `.s7interactiveimage` in unità assolute oppure utilizzando il modificatore `stagesize`.

   Potete inserire le dimensioni in CSS direttamente nella pagina HTML o in un file CSS del visualizzatore personalizzato, che verrà quindi assegnato a un record di predefinito per visualizzatori in  AEM Assets - su richiesta, o trasmesso esplicitamente tramite il comando `style`.

   Per ulteriori informazioni sullo stile del visualizzatore con i CSS, consultate [Video](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0).

   Di seguito è riportato un esempio di definizione di una dimensione visualizzatore statica nella pagina HTML:

   ```
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Potete trasmettere esplicitamente il modificatore `stagesize` con il codice di inizializzazione del visualizzatore con la raccolta `params` o come chiamata API come descritto nella sezione Riferimento comando, come segue:

   ```
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   In questo esempio viene consigliato un approccio basato su CSS.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi descritti qui sopra, potete creare un&#39;istanza della classe `s7viewers.InteractiveImage`, trasmettere tutte le informazioni di configurazione al relativo costruttore e chiamare il metodo `init()` su un&#39;istanza di visualizzatore. Le informazioni di configurazione vengono trasmesse al costruttore come oggetto JSON. Come minimo, questo oggetto deve avere un campo `containerId` contenente il nome dell&#39;ID contenitore del visualizzatore e un oggetto JSON nidificato `params` con i parametri di configurazione supportati dal visualizzatore. In questo caso, l&#39;oggetto `params` deve avere almeno l&#39;URL Image Server passato come proprietà `serverUrl` e la risorsa iniziale come parametro `asset`. L&#39;API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una sola riga di codice.

   È importante che il contenitore del visualizzatore venga aggiunto al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al suo ID. Alcuni browser ritardano la creazione del DOM fino alla fine della pagina Web. Per garantire la massima compatibilità, chiamare il metodo `init()` immediatamente prima del tag di chiusura `BODY` o sull&#39;evento body `onload()`.

   Allo stesso tempo, l&#39;elemento contenitore non deve necessariamente far parte del layout della pagina Web. Ad esempio, potrebbe essere nascosto utilizzando lo stile `display:none` assegnatogli. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina Web riporta l&#39;elemento contenitore al layout. In questo caso, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un&#39;istanza visualizzatore, passaggio delle opzioni di configurazione minime necessarie al costruttore e chiamata del metodo `init()`. L&#39;esempio presuppone che `interactiveImage` sia l&#39;istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` è l&#39;URL del server immagini e `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` è la risorsa:

   ```
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage ({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   ```

   Il codice seguente è un esempio completo di una pagina Web banale che incorpora il visualizzatore di immagini video con una dimensione fissa:

   ```
   <!DOCTYPE html> 
   <html> 
   <head> 
   <script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
   <style type="text/css"> 
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   } 
   </style> 
   </head> 
   <body> 
   <div id="s7viewer" style="position:relative"></div> 
   <script type="text/javascript"> 
   var interactiveImage = new s7viewers.InteractiveImage({ 
    "containerId":"s7viewer", 
   "params":{ 
    "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
    "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
   } 
   }).init(); 
   </script> 
   </body> 
   </html> 
   ```

**Incorporazione responsive con altezza illimitata**

Con l&#39;incorporazione reattiva della progettazione, la pagina Web dispone in genere di un layout flessibile che specifica le dimensioni runtime del contenitore del visualizzatore `DIV`. Ad esempio, si supponga che la pagina Web consenta al contenitore del visualizzatore `DIV` di occupare il 40% della dimensione della finestra del browser Web. E la sua altezza è lasciata illimitata. Il codice HTML della pagina Web sarà simile al seguente:

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
1. Definizione del contenitore `DIV`.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi indicati sopra sono uguali a quelli con l&#39;incorporamento a dimensione fissa. Aggiungete il contenitore `DIV` alla `"holder"` `DIV` esistente. Il codice seguente è un esempio completo. Le dimensioni del visualizzatore cambiano quando il browser viene ridimensionato e le proporzioni del visualizzatore corrispondono alla risorsa.

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

La pagina degli esempi seguente illustra gli usi più reali dell’incorporamento reattivo di design con altezza illimitata:

[https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html](https://marketing.adobe.com/resources/help/en_US/dm/shoppable-banner/samples/InteractiveImage-responsive-unrestricted-height.html)

**Dimensioni flessibili Incorporamento con larghezza e altezza definite**

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

Gli altri passaggi di incorporamento sono identici ai passaggi utilizzati per l&#39;incorporamento reattivo con altezza illimitata. L’esempio risultante è il seguente:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
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
var interactiveImage = new s7viewers.InteractiveImage({ 
 "containerId":"s7viewer", 
"params":{ 
 "asset":"/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg", 
 "serverurl":"http://aodmarketingna.assetsadobe.com/is/image" 
} 
}).init(); 
</script> 
</body> 
</html> 
```

**Incorporazione tramite l&#39;API basata su Setter**

Invece di utilizzare l&#39;inizializzazione basata su JSON, è possibile utilizzare l&#39;API basata su setter e il costruttore no-args. L&#39;utilizzo di questo costruttore di API non accetta parametri e i parametri di configurazione vengono specificati utilizzando i metodi `setContainerId()`, `setParam()` e `setAsset()` API con chiamate JavaScript separate.

L&#39;esempio seguente illustra l&#39;utilizzo dell&#39;incorporamento a dimensione fissa con l&#39;API basata su setter:

```
<!DOCTYPE html> 
<html> 
<head> 
<script type="text/javascript" src="http://aodmarketingna.assetsadobe.com/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script> 
<style type="text/css"> 
#s7viewer.s7interactiveimage { 
 width: 1174px; 
 height: 500px; 
} 
</style> 
</head> 
<body> 
<div id="s7viewer" style="position:relative"></div> 
<script type="text/javascript"> 
var interactiveImage = new s7viewers.InteractiveImage(); 
interactiveImage.setContainerId("s7viewer"); 
interactiveImage.setParam("serverurl", "http://aodmarketingna.assetsadobe.com/is/image"); 
interactiveImage.setAsset("/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.jpg"); 
interactiveImage.init(); 
</script> 
</body> 
</html> 
```

