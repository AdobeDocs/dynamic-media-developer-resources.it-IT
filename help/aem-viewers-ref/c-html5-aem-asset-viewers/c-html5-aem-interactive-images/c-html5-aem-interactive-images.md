---
title: Immagine interattiva
description: Visualizzatore immagini interattivo è un visualizzatore che visualizza una singola immagine non ingrandibile con hotspot selezionabili. Lo scopo di questo visualizzatore è quello di implementare un’esperienza di "banner per acquisti". In altre parole, l'utente può selezionare un hotspot sull'immagine del banner e venire reindirizzato a una pagina Quickview o di dettaglio del prodotto sul sito Web. È progettato per funzionare su desktop e dispositivi mobili.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Images
role: Developer,User
exl-id: c7089ecd-6ff3-4fe9-9ee7-3b48c9201558
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '1720'
ht-degree: 0%

---

# Immagine interattiva{#interactive-image}

Visualizzatore immagini interattivo è un visualizzatore che visualizza una singola immagine non ingrandibile con hotspot selezionabili. Lo scopo di questo visualizzatore è quello di implementare un’esperienza di &quot;banner per acquisti&quot;. In altre parole, l&#39;utente può selezionare un hotspot sull&#39;immagine del banner e venire reindirizzato a una pagina Quickview o di dettaglio del prodotto sul sito Web. È progettato per funzionare su desktop e dispositivi mobili.

>[!NOTE]
>
>Le immagini che utilizzano IR (Image Rendering) o UGC (User-Generated Content) non sono supportate da questo visualizzatore.

Il tipo di visualizzatore è 508.

## URL demo {#section-c0ad383db6a444979dc7eeb1ec4cf54d}

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage.html)

## Requisiti di sistema {#section-b7270cc4290043399681dc504f043609}

Consulta [Requisiti di sistema](../../c-system-requirements-and-prerequisites.md#concept-9282e5b777de42cdaf72ef7ebd646842).

## Utilizzo del Visualizzatore immagini interattivo {#section-e6c68406ecdc4de781df182bbd8088b4}

Visualizzatore immagini interattivo rappresenta un file JavaScript principale e un set di file di supporto (un singolo file JavaScript da includere con tutti i componenti SDK del visualizzatore utilizzati da questo particolare visualizzatore, risorse e CSS) scaricati dal visualizzatore in fase di esecuzione.

Il Visualizzatore di immagini interattivo può essere utilizzato solo in modalità incorporata, dove è integrato nella pagina web di destinazione utilizzando l’API documentata.

La configurazione e lo skin sono simili a quelli degli altri visualizzatori descritti in questa Guida. Tutte le operazioni di skin vengono eseguite tramite CSS personalizzato.

Consulta [Riferimento comando comune a tutti i visualizzatori - Attributi di configurazione](../../r-html5-viewer-20-cmdref-configattrib/r-html5-viewer-20-cmdref-configattrib.md#concept-850e0f2c49b949deb7cfbfd330d329bd) e [Riferimento comando comune a tutti i visualizzatori - URL](../../c-html5-viewer-20-cmdref-url/c-html5-viewer-20-cmdref-url.md#concept-9b337f349b7b406b8c33c7ee96b3e226)

## Interazione con il visualizzatore di immagini interattivo {#section-642e66ca38cd4032992840ec6c0b0cd2}

L&#39;interazione supportata dal Visualizzatore immagini video è l&#39;attivazione di un hotspot sui sistemi desktop. Questa attivazione si verifica al clic e sui dispositivi touch con un solo tocco.

Il visualizzatore è completamente accessibile da tastiera.

Consulta [Accessibilità della tastiera e navigazione](../../c-keyboard-accessibility.md#topic-f5650e9493404e55a3627c8d1366b861).

## Incorporazione del visualizzatore di immagini interattivo {#section-6bb5d3c502544ad18a58eafe12a13435}

Il Visualizzatore di immagini interattivo è incorporato nella pagina di hosting. Tale pagina web può avere un layout statico, o può essere &quot;reattiva&quot; e visualizzata in modo diverso su dispositivi diversi o per diverse dimensioni della finestra del browser.

Per soddisfare queste esigenze, il visualizzatore supporta due modalità operative principali: l’incorporamento a dimensione fissa e l’incorporamento reattivo.

**Informazioni sulla modalità di incorporamento a dimensione fissa e sulla modalità di incorporamento a progettazione reattiva**

In modalità incorporata, il visualizzatore viene aggiunto alla pagina web esistente. È possibile che in questa pagina web siano già presenti alcuni contenuti dei clienti non correlati al visualizzatore. Il visualizzatore occupa normalmente solo una parte del patrimonio immobiliare di una pagina web.

I casi d’uso principali sono le pagine web orientate per desktop o dispositivi tablet e le pagine progettate responsive che regolano automaticamente il layout a seconda del tipo di dispositivo.

L’incorporamento a dimensione fissa viene utilizzato quando il visualizzatore non ne modifica le dimensioni dopo il caricamento iniziale. Questo metodo è la scelta migliore per le pagine web con un layout statico.

L’incorporamento reattivo della progettazione presuppone che il visualizzatore debba essere ridimensionato in fase di esecuzione in risposta alla modifica delle dimensioni del suo contenitore `DIV`. Il caso d’uso più comune è l’aggiunta di un visualizzatore a una pagina web che utilizza un layout di pagina flessibile.

In modalità di incorporamento di un design reattivo, il visualizzatore si comporta in modo diverso a seconda del modo in cui la pagina web ridimensiona il suo contenitore `DIV`. Se la pagina web imposta solo la larghezza del contenitore `DIV`, lasciando libera la sua altezza, lo spettatore sceglie automaticamente la sua altezza in base alle proporzioni della risorsa utilizzata. Questa funzionalità assicura che la risorsa si adatti perfettamente alla vista senza alcuna spaziatura sui lati. Questo caso d’uso è il più comune per le pagine web che utilizzano framework di layout di progettazione web responsive come Bootstrap e Foundation.

In caso contrario, se la pagina web imposta sia la larghezza che l’altezza per il contenitore del visualizzatore `DIV`, il visualizzatore riempie solo quell’area. Segue anche le dimensioni fornite dal layout della pagina web. Un buon esempio è l’incorporamento del visualizzatore in una sovrapposizione modale, in cui la sovrapposizione viene ridimensionata in base alle dimensioni della finestra del browser web.

**Incorporamento a dimensione fissa**

Per aggiungere il visualizzatore a una pagina Web, effettuare le seguenti operazioni:

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Impostazione delle dimensioni del visualizzatore.
1. Creazione e inizializzazione del visualizzatore.

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.

   Per creare un visualizzatore è necessario aggiungere un tag script nell’intestazione del HTML. Prima di poter utilizzare l’API del visualizzatore, assicurati di includere [!DNL InterativeImage.js]. Il [!DNL InteractiveImage.js] il file si trova sotto [!DNL html5/js/] sottocartella della distribuzione standard IS-Viewers:

[!DNL <s7viewers_root>/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js]

Puoi utilizzare un percorso relativo se il visualizzatore viene distribuito su uno dei server Adobe Dynamic Media Classic e viene fornito dallo stesso dominio. In caso contrario, si specifica un percorso completo per uno dei server Adobe Dynamic Media Classic in cui sono installati i visualizzatori IS.

Il percorso relativo è simile al seguente:

```html {.line-numbers}
<script language="javascript" type="text/javascript" src="/etc/dam/viewers/s7viewers/html5/js/InteractiveImage.js"></script>
```

>[!NOTE]
>
>Fai riferimento solo al visualizzatore principale JavaScript `include` sulla pagina. Non fare riferimento ad altri file JavaScript nel codice della pagina web che potrebbero essere scaricati dalla logica del visualizzatore in fase di esecuzione. In particolare, non fare riferimento direttamente all’SDK di HTML 5 `Utils.js` libreria caricata dal visualizzatore da `/s7viewers` percorso di contesto (il cosiddetto SDK consolidato) `include`). Il motivo è che l&#39;ubicazione di `Utils.js` o librerie di visualizzatori runtime simili sono completamente gestite dalla logica del visualizzatore e la posizione cambia tra le versioni del visualizzatore. L’Adobe non mantiene le versioni precedenti del visualizzatore secondario `includes` sul server.
>
>
>Di conseguenza, inserendo un riferimento diretto a qualsiasi JavaScript secondario `include` utilizzato dal visualizzatore sulla pagina interrompe la funzionalità del visualizzatore in futuro quando viene distribuita una nuova versione del prodotto.

1. Definizione del contenitore `DIV`.

   Aggiungi un elemento vuoto `DIV` nella pagina in cui si desidera visualizzare il visualizzatore. Il `DIV` deve avere il proprio ID definito perché questo ID viene passato successivamente all&#39;API del visualizzatore. La dimensione del DIV è specificata tramite CSS.

   Segnaposto `DIV` è un elemento posizionato, il che significa che `position` Proprietà CSS impostata su `relative` o `absolute`.

   Di seguito è riportato un esempio di segnaposto definito `DIV` elemento:

   ```html {.line-numbers}
   <div id="s7viewer" style="position:relative"></div>
   ```

1. Impostazione delle dimensioni del visualizzatore

   È possibile impostare la dimensione statica del visualizzatore dichiarandolo per `.s7interactiveimage` classe CSS di primo livello in unità assolute oppure utilizzando `stagesize` modificatore.

   Puoi inserire il dimensionamento in CSS direttamente nella pagina HTML. In alternativa, puoi inserire il dimensionamento in un file CSS visualizzatore personalizzato, che viene successivamente assegnato a un record di predefinito visualizzatore in Adobe Experience Manager Assets - On-demand, o trasmesso esplicitamente utilizzando `style` comando.

   Consulta [Video](../../c-html5-aem-asset-viewers/c-html5-aem-interactive-images/c-html5-aem-interactive-image-customizingviewer/c-html5-aem-interactive-image-customizingviewer.md#concept-73a8546acdb444a387c49969ceca57d0) per ulteriori informazioni sullo stile del visualizzatore con CSS.

   Di seguito è riportato un esempio di definizione di una dimensione di visualizzatore statico nella pagina HTML:

   ```html {.line-numbers}
   #s7viewer.s7interactiveimage { 
    width: 1174px; 
    height: 500px; 
   }
   ```

   Puoi trasmettere esplicitamente il `stagesize` modificatore con il codice di inizializzazione del visualizzatore `params` o come chiamata API come descritto nella sezione Riferimento comando, come segue:

   ```html {.line-numbers}
   interactiveImage.setParam("stagesize", "1174,500");
   ```

   Si consiglia un approccio basato su CSS, che viene utilizzato in questo esempio.

1. Creazione e inizializzazione del visualizzatore.

   Una volta completati i passaggi precedenti, puoi creare un’istanza di `s7viewers.InteractiveImage` classe, passa tutte le informazioni di configurazione al relativo costruttore e chiama `init()` su un&#39;istanza del visualizzatore. Le informazioni di configurazione vengono passate al costruttore come oggetto JSON. Questo oggetto deve avere almeno `containerId` campo contenente il nome dell’ID contenitore del visualizzatore e nidificato `params` Oggetto JSON con parametri di configurazione supportati dal visualizzatore. In questo caso, il `params` l&#39;oggetto deve avere almeno l&#39;URL Image Server passato come `serverUrl` e la risorsa iniziale come `asset` parametro. L’API di inizializzazione basata su JSON consente di creare e avviare il visualizzatore con una singola riga di codice.

   È importante aggiungere il contenitore del visualizzatore al DOM in modo che il codice del visualizzatore possa trovare l’elemento contenitore in base al relativo ID. Alcuni browser ritardano la creazione di DOM fino alla fine della pagina web. Per la massima compatibilità, chiama il `init()` metodo immediatamente prima della chiusura `BODY` o sul corpo `onload()` evento.

   Allo stesso tempo, l’elemento contenitore non deve ancora necessariamente far parte del layout della pagina web. Ad esempio, potrebbe essere nascosto utilizzando `display:none` stile assegnato. In questo caso, il visualizzatore ritarda il processo di inizializzazione fino al momento in cui la pagina web riporta l’elemento contenitore al layout. Quando si verifica questo evento, il caricamento del visualizzatore riprende automaticamente.

   Di seguito è riportato un esempio di creazione di un’istanza del visualizzatore, mediante il passaggio al costruttore delle opzioni di configurazione minime necessarie e la chiamata al `init()` metodo. L’esempio presuppone `interactiveImage` è l’istanza del visualizzatore; `s7viewer` è il nome del segnaposto `DIV`; `http://aodmarketingna.assetsadobe.com/is/image` è l’URL di Image Server e `/content/dam/mac/aodmarketingna/shoppable-banner/shoppable-banner.` è la risorsa:

   ```html {.line-numbers}
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

   Il codice che segue è un esempio completo di una pagina Web banale che incorpora il Visualizzatore immagini video con una dimensione fissa:

   ```html {.line-numbers}
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

**Design reattivo con altezza illimitata**

Con l’incorporamento di un design reattivo, la pagina web solitamente dispone di un layout flessibile che determina la dimensione di runtime del contenitore del visualizzatore `DIV`. Nell’esempio seguente, si supponga che la pagina web consenta il contenitore del visualizzatore `DIV` per occupare il 40% delle dimensioni della finestra del browser web. E la sua altezza viene lasciata libera. Il codice HTML della pagina Web sarà simile al seguente:

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

1. Aggiunta del file JavaScript del visualizzatore alla pagina web.
1. Definizione del contenitore `DIV`.
1. Creazione e inizializzazione del visualizzatore.

Tutti i passaggi precedenti sono gli stessi dell’incorporamento di dimensioni fisse. Aggiungi il contenitore `DIV` al esistente `"holder"` `DIV`. Il codice seguente è un esempio completo. Osserva come cambiano le dimensioni del visualizzatore quando il browser viene ridimensionato e come le proporzioni del visualizzatore corrispondono alla risorsa.

```html {.line-numbers}
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

La pagina di esempi seguente illustra usi più reali dell’incorporamento di design responsive con altezza illimitata:

[https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html](https://experienceleague.adobe.com/tools/dynamic-media-demo/shoppable-banner/InteractiveImage-responsive-unrestricted-height.html)

**Dimensione flessibile Incorporata con definizione di larghezza e altezza**

In presenza di un’incorporazione di dimensioni flessibili con larghezza e altezza definite, lo stile della pagina web è diverso. Fornisce entrambe le dimensioni al `"holder"` DIV e centralo nella finestra del browser. Inoltre, la pagina web imposta le dimensioni del `HTML` e `BODY` al 100%.

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

Il resto dei passaggi di incorporamento è identico ai passaggi utilizzati per l’incorporamento reattivo con altezza illimitata. L’esempio risultante è il seguente:

```html {.line-numbers}
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

**Incorporazione tramite API basata su set**

Invece di utilizzare l’inizializzazione basata su JSON, puoi utilizzare l’API basata su setter e il costruttore no-args. L’utilizzo di questo costruttore API non accetta parametri e i parametri di configurazione vengono specificati utilizzando `setContainerId()`, `setParam()`, e `setAsset()` Metodi API con chiamate JavaScript separate.

L’esempio seguente illustra l’utilizzo dell’incorporamento a dimensione fissa con l’API basata su setter:

```html {.line-numbers}
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
