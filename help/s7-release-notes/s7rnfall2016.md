---
description: Note aggiornate sulla versione di Adobe Scene7 - Autunno 2016 - parte della soluzione di Adobe Experience Manager  nel Adobe Marketing Cloud .
seo-description: Note aggiornate sulla versione di Adobe Scene7 - Autunno 2016 - parte della soluzione di Adobe Experience Manager  nel Adobe Marketing Cloud .
seo-title: Rilascio di Scene7 - Autunno 2016
solution: Experience Manager
title: Rilascio di Scene7 - Autunno 2016
topic: Dynamic media
uuid: 3fddda65-0c6e-48ec-bd60-7e0ca59421a8
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2263'
ht-degree: 0%

---


# Rilascio di Scene7 - Autunno 2016{#scene-fall-release}

Note aggiornate sulla versione di Adobe Scene7 - Autunno 2016 - parte della soluzione di Adobe Experience Manager  nel Adobe Marketing Cloud .

## Rilascio di Scene7 - Autunno 2016 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Le ultime note sulla versione relative alla versione di [!DNL Adobe Scene7] autunno 2016 fanno parte della [!DNL Adobe Experience Manager] soluzione [!DNL Adobe Marketing Cloud].

* [Generali](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7 Publishing System](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visualizzatori (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visualizzatori (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visualizzatori (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [Scene7 HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Scene7 Image Serving 6.3.2 e Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Generali {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe è entusiasta di annunciare la disponibilità della distribuzione di contenuti HTTP/2 con il vantaggio complessivo di prestazioni migliorate.

Consultate [HTTP2 Delivery of Content FAQ](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/scene7/http2faq.html)(Distribuzione HTTP2 di contenuti).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Per la documentazione completa, vedete [https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html)

**Nuove funzioni, miglioramenti e correzioni di bug**

* Funzione di remix video rimossa dall’interfaccia [!DNL Adobe Scene7 Publishing System] utente.
* È stata aggiunta l’autenticazione a tutti i servlet di Scene7 laddove necessario e possibile.
* Correzione di bug relativi alla vista Elenco nel cestino.
* È stata rimossa la funzione **Crea utente SPSAdmin** da Gestione utente a causa di problemi di sicurezza.
* WebAdmin FTP ora supporta l&#39;autenticazione OKTA.
* È stata rimossa la funzione della password predefinita creata per i nuovi utenti di Media Portal.
* Correzione di bug relativa alla password temporanea generata al momento dell&#39;aggiunta di un nuovo utente. La password non soddisfa i requisiti di password necessari.
* Sono stati risolti i problemi relativi al disco radice WebAdmin.
* Correzione di bug che coinvolge la disattivazione di un utente che non si riflette immediatamente nell&#39;interfaccia utente.
* Correzione di bug che comporta l&#39;eliminazione di un utente che non consentiva di ricreare l&#39;utente in un secondo momento.
* Correzione di bug relativa al messaggio e-mail di benvenuto inviato ai nuovi utenti di Scene7 che non includevano l’autenticazione per controllare determinate impostazioni.
* Correzione di bug che causava il mancato recupero di un elenco di cartelle FTP se il nome di una cartella conteneva caratteri speciali.
* Configurare i fornitori di servizi OKTA per gli ambienti Scene7.
* È stato aggiunto il supporto per l’ID organizzazione Marketing Cloud per il visualizzatore  Analytics.
* Implementato il consumer SAML di Scene7.

## Visualizzatori (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Per la documentazione completa, consultate la Guida di riferimento [ai visualizzatori](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Correzioni di bug per Image Server 5.5.3**

* Compatibilità con le librerie RequireJS e DOJO.

   Memorizzazione nella cache SDK consolidata durante la distribuzione del visualizzatore.

## Visualizzatori (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Per la documentazione completa, consultate la Guida di riferimento [ai visualizzatori](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Correzioni di bug per Image Server 5.5.2**

* Impossibile riprodurre il video in Internet Explorer 11 in Windows 7.
* `initialframe` non influiva sulla modalità verticale sui dispositivi mobili per l’eCatalog HTML5.

## Visualizzatori (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Per la documentazione completa, consultate la Guida di riferimento [ai visualizzatori](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html).

**Nuove funzioni, miglioramenti e correzioni di bug per Image Server 5.5.1**

* Visualizzatore HTML5 per eCatalog con funzione di ricerca.
* È stata aggiunta la riproduzione video in streaming HLS come metodo di distribuzione video predefinito per la maggior parte dei sistemi desktop. Lo streaming video HDS basato su Flash è ancora disponibile come opzione di riproduzione alternativa.
* È stato aggiunto il supporto per i dispositivi con input sia del mouse che touch con il browser Chrome.
* È stato aggiunto il supporto per l’ID organizzazione Marketing Cloud all’integrazione  Analytics.
* Aggiorna la libreria JavaScript AppMeasurement alla versione 1.6.1.
* È stato aggiunto il supporto per l’orientamento da destra a sinistra nel visualizzatore eCatalog.
* Problema risolto relativo alla `tip=0,-1,0` causa di un errore fuori intervallo.

**Note sulla compatibilità**

* Blackberry

   * Incompatibilità con i set AVS precedenti. I client potrebbero dover caricare nuovamente i set AVS per consentire la riproduzione.

* Generali

   * Il ridimensionamento lato browser potrebbe rendere sfocata l&#39;interfaccia utente e le immagini durante lo zoom dell&#39;utente nella pagina. La formattazione dell&#39;interfaccia utente potrebbe anche non essere visualizzata correttamente a seconda dello zoom. Questo passerà allo schermo intero.
   * A causa della limitazione delle dimensioni sui dispositivi mobili, il visualizzatore di file multimediali diversi utilizza il gesto di scorrimento per scambiare i fotogrammi in set di immagini incorporati invece di toccare il componente Campioni incorporato. Il componente è presente come indicatore visivo.
   * Nei browser Internet Explorer e in alcuni dispositivi touch, la modalità a schermo intero non occupa l&#39;intero schermo del dispositivo. ma ridimensiona l&#39;applicazione alle dimensioni della finestra del browser.
   * Il pulsante Chiudi non funziona su iOS 8.0 e 8.1 ma non si verifica più in iOS 8.2

* Galaxy SIII

   * Perdita di memoria visibile con i visualizzatori HTML5 per zoom e eCatalog. La navigazione ripetuta attraverso i frame potrebbe causare l&#39;arresto anomalo del browser.
   * Toccando due volte il visualizzatore è possibile che l’intera pagina venga ingrandita invece che solo il visualizzatore con il ridimensionamento laterale del browser abilitato.

* Galaxy S4

   * Dispositivo rilevato come tablet in modalità verticale con schermo intero selezionato nelle impostazioni del browser.

* Galassia Nexus

   * Toccando due volte il visualizzatore è possibile che l’intera pagina venga ingrandita invece che solo il visualizzatore con il ridimensionamento laterale del browser abilitato.

* Galaxy Nexus 10 e Galaxy Tablet

   * eCatalog che mostra pagine affiancate non corrette con orientamenti orizzontali e verticali.

* Dispositivi mobili HTC

   * I nostri risultati mostrano che l’impossibilità di disattivare lo zoom con le dita nativo è una &quot;caratteristica&quot; del wrapper dell’interfaccia HTC (SENSO HTC). Questo può causare lo zoom di un’intera pagina quando si utilizza il gesto di zoom con le dita sul visualizzatore. Suggerisci di utilizzare il doppio tocco.
   * Le icone delle mappe immagine potrebbero sovrapporsi se le mappe immagine sono piccole e si chiudono insieme.

* Video HTML5

   * Internet Explorer 9: le immagini poster personalizzate non vengono visualizzate.
   * `IntialBitRate` il modificatore è supportato solo con riproduzione software HLS e Flash HDS. Non funziona quando la riproduzione utilizza il lettore nativo.
   * Al momento non è supportata la riproduzione progressiva OGG e WebM.
   * Il ridimensionamento del browser può causare la visualizzazione errata del lettore video (include le impostazioni del pannello di controllo del sistema operativo Windows)
   * La ricerca di video con streaming HLS su Safari potrebbe non essere coerente.

* Internet Explorer

   * Al momento la modalità Quirks non è supportata.
   * Al momento la modalità di compatibilità non è supportata.
   * Al momento Internet Explorer su dispositivo mobile non è supportato.

* iOS

   * Gli eCatalog di grandi dimensioni possono causare l’arresto anomalo del browser sull’iPad 2.
   * I telefoni iPhone 6+ vengono rilevati come tablet dai visualizzatori.

* Safari

   * Safari 6.1 o successivo: Le impostazioni dei plug-in Internet potrebbero impedire la riproduzione di video Flash.
   * Il video &quot;search&quot; che utilizza lo streaming HLS su Safari potrebbe non essere coerente.
   * Impossibile cercare di terminare il video in Safari 6 utilizzando lo streaming HLS.

**Problemi noti e restrizioni**

* I modificatori Image Serving da non `iscommands` vengono aggiunti alla `req=set` richiesta per impostazione predefinita. I modificatori che influiscono solo sulla visualizzazione delle immagini funzionano correttamente. I modificatori che influiscono sulle dimensioni devono essere utilizzati in una risorsa complessa. Ad esempio:

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [IE9 a comparsa] a volte rimane sullo schermo dopo lo spegnimento del mouse.
* Il ridimensionamento del browser determina un ridimensionamento errato.
* iPad 2: Una grande risorsa eCatalog si blocca in Safari su iOS.
* Tutti i visualizzatori

   * Filigrane, offuscamento e blocco non sono supportati.
   * I predefiniti per immagini non sono supportati.
   * Al momento, l’aggiunta o la rimozione del visualizzatore dal DOM tramite `display:none` CSS o lo scollegamento dinamico dal nodo principale non è supportata.

* HTML5 Tutti i visualizzatori

   * Se si incorpora un visualizzatore in una tabella, il ridimensionamento o il posizionamento del visualizzatore potrebbero non essere corretti in modalità schermo intero non nativa. Consiglia di utilizzare i div.
   * I parametri con nomi di istanza espliciti nel codice richiedono che i nomi di istanza nell’URL vengano sovrascritti (ad esempio, `zoomView.iconfeffect=0`).
   * Al momento il ritaglio del comando Image Server non è supportato.
   * Il pulsante Chiudi funziona solo se il visualizzatore è aperto nella finestra secondaria.
   * Il `iscommands` modificatore non supporta i modificatori Image Server che agiscono sulle dimensioni dell’immagine.

* HTML5 eCatalog

   * Se si passa a un&#39;altra pagina HTML e si torna talvolta, il visualizzatore viene reimpostato sulla prima pagina.
   * Il layout della pagina talvolta non viene visualizzato correttamente dopo la rotazione del dispositivo iOS. Lo zoom nella pagina corregge il layout.
   * I collegamenti interni collegano solo alla pagina più a sinistra tra quelle affiancate. Interessa i dispositivi mobili in modalità verticale.
   * I collegamenti InitalFrame collegano solo alla pagina più a sinistra tra quelle affiancate. Interessa i dispositivi mobili in modalità verticale.
   * A causa di limitazioni del browser, la funzione di stampa non è disponibile in IE9.

* HTML5 MixedMedia

   * Al momento la riproduzione della colonna sonora non è supportata.

* HTML5 Social

   * Per eseguire correttamente il rendering delle miniature nell’e-mail in uscita, il `serverurl` modificatore deve avere un URL assoluto.

* Video HTML5

   * L&#39;immagine poster potrebbe incontrare un errore &quot;dimensione massima&quot;. Potrebbe essere necessario aumentare l’impostazione dei limiti per la pubblicazione da parte di Image Server.
   * I sottotitoli video richiedono un ruleset aziendale se l’hosting della pagina HTML è gestito da un server esterno (non da un server Scene7). Per assistenza, contattate il supporto Adobe.
   *  tracciamento Analytics potrebbe riportare una percentuale di riproduzione non corretta a causa del buffering
   * Sui dispositivi Android e iPad potrebbe venire visualizzato un fotogramma nero invece dell’immagine poster.
   * Un fotogramma nero potrebbe lampeggiare sullo schermo durante il caricamento del visualizzatore su dispositivi iPad o Android.
   * I bordi neri sono visualizzati sul lato del componente VideoPlayer quando lo sfondo è impostato su bianco/trasparente sui dispositivi iPad.
   * L’ultimo fotogramma del video potrebbe essere distorto sull’iPad con iOS 7.
   * Il macroblocco occasionale può verificarsi durante la ricerca video in modalità di streaming HLS nei browser Chrome, Firefox e Internet Explorer.
   * L&#39;immagine poster potrebbe non essere visualizzata nel browser Microsoft Edge per la prima volta dal visitatore.
   * L&#39;immagine poster potrebbe nascondersi dopo il caricamento del video in Internet Explorer 9 quando si utilizza la riproduzione progressiva.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

La Guida utente si trova nella cartella Adobe HTML5 Viewer SDK dell’installazione client. La documentazione relativa alle API dei componenti si trova nella sottocartella docs dell&#39;installazione client.

**Correzioni di bug per la versione 3.0.2**

* VideoPlayer - Impossibile riprodurre il video in Internet Explorer 11 in Windows 7
* TableOfContents - `initialframe` non ha influito sulla modalità verticale sui dispositivi mobili per il visualizzatore HTML5 per eCatalog.

**Nuove funzioni, miglioramenti e correzioni di bug per la versione 3.0.1**

* Generali

   * È stata aggiunta la riproduzione video in streaming HLS come metodo di distribuzione video predefinito per la maggior parte dei sistemi desktop. Lo streaming video HDS basato su Flash è ancora disponibile come opzione di riproduzione alternativa.
   * Sono stati aggiunti i componenti SearchManager, SearchPanel, SearchEffect e SearchButton per supportare la nuova funzione di ricerca nei visualizzatori eCatalog.
   * È stato aggiunto il supporto per i dispositivi con input touch e mouse in esecuzione sul browser Chrome.
   * È stato modificato il rilevamento della versione Android per supportare versioni future del sistema operativo
   * È stato aggiunto il supporto per l’orientamento da destra a sinistra nei componenti SDK per eCatalog specifici.

* ControlBar

   * È stato aggiunto lo scorrimento facoltativo per il contenuto ControlBar nel caso in cui non rientri nella larghezza disponibile.

* FlyoutzoomView

   * Problema risolto relativo alla `tip=0,-1,0` causa di un errore fuori intervallo.

**Note sulla compatibilità**

* Android 4.x

   * Per disattivare il predefinito, evidenziate in blu la seguente regola CSS da aggiungere al componente:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * La riproduzione video potrebbe cessare quando si modificano i flussi di bitrate nei set AVS.

* Effetto cromatura

   * Eventuali chiamate API che forzano la ricostruzione del componente potrebbero essere ignorate a causa del caching interno di Chrome.

* Galaxy SIII

   * A volte il visualizzatore non viene caricato a schermo intero.
   * Pageview è affetta da una perdita di memoria sul dispositivo in questa fase.
   * Toccate due volte per ingrandire il visualizzatore e la pagina quando è attivo il ridimensionamento sul lato del browser.

* Galassia Nexus

   * Visualizzazione di artefatti su alcuni componenti di visualizzazione.
   * Toccate due volte per ingrandire il visualizzatore e la pagina quando è attivo il ridimensionamento sul lato del browser.

* iPad 3

   * L’iPad 3 ha una risoluzione nativa di 2048x1536. Ciò può causare problemi di visualizzazione se il limite di dimensioni dell’immagine della società per la pubblicazione IS è inferiore a quello impostato.

* iPhone4

   * Icona Riproduci effetto sostituita dall’icona di riproduzione dopo la pagina di scorrimento.

* Internet Explorer

   * In IE 10 e nelle versioni precedenti la modalità a schermo intero non occupa l&#39;intero schermo, ma ridimensiona l&#39;applicazione alle dimensioni della finestra del browser.
   * La modalità di rendering dei collegamenti non è supportata.
   * Al momento Internet Explorer su dispositivo mobile non è supportato.
   * Util.js potrebbe non riuscire a caricarsi se incluso in modo asincrono.
   * I blocchi di icone IconEffect fanno clic su eventi sui componenti Visualizzazione 360 gradi e Visualizzazione zoom.

* Lettori video per dispositivi nativi

   * I componenti dell’interfaccia utente di livello su VideoPlayer non sono supportati quando VideoPlayer viene utilizzato per chiamare il lettore nativo del dispositivo.
   * La riproduzione video in modalità nativa non è coerente con Safari 6.
   * La riproduzione nativa sostituisce l&#39;icona di riproduzione con l&#39;icona di riproduzione dopo la pagina di scorrimento.

* Dispositivi touch

   * La modalità a schermo intero non occupa l&#39;intero schermo del dispositivo, ma ridimensiona l&#39;applicazione alle dimensioni della finestra del browser.
   * I cursori personalizzati non funzionano sui dispositivi touch.
   * Al momento, il ridimensionamento delle pagine sui dispositivi touch non è supportato. Per incorporare i visualizzatori HTML5 è necessario un tag meta viewport con le impostazioni appropriate.

* Xoom

   * Toccate due volte per ingrandire il visualizzatore e la pagina quando è attivo il ridimensionamento sul lato del browser.

**Problemi noti e restrizioni**

* Tutti i componenti

   * Nelle versioni 2.7.2 e precedenti, alcuni componenti venivano aggiunti al DOM tramite `insertBefore()` API. Di conseguenza, tali componenti si posizionavano nella parte inferiore dell’ordine di sovrapposizione, indipendentemente dal momento in cui viene creata l’istanza del componente rispetto ad altri componenti. Con la versione 2.8.1, tutti i componenti utilizzano ora l’ `appendChild()` API, il che significa che l’ordine di sovrapposizione dei componenti corrisponderebbe all’ordine di creazione dell’istanza.

   * L&#39;utilizzo del `iscommand` modificatore per impostare il formato del canale alfa dell&#39;immagine non è supportato. Utilizzate invece `FMT` il parametro component.
   * Al momento la proprietà di trasformazione CSS non è supportata.

* Dispositivi touch

   * Il gesto di avvicinamento delle dita sui dispositivi touch non genera un evento di zoom

* Contenitore

   * Bordo, spaziatura e margini del contenitore non sono supportati. Adobe consiglia di aggiungere elementi di stile al DIV principale.
   * È necessario impostare esplicitamente la dimensione del contenitore, altrimenti i componenti potrebbero essere ridimensionati correttamente.

* Stampa, componente

   * A causa di limitazioni del browser, in Internet Explorer 9 il componente per la stampa potrebbe non essere in grado di ridimensionare correttamente il contenuto sul foglio.

* IconEffect, componente

   * IconEffect genera un errore di script in Internet Explorer se `autohide` è disabilitato (impostato su `0`).

* Componente ImageMapEffect

   * Ritardo con l’icona di riposizionamento durante il panning dell’immagine sul componente di visualizzazione.

* Componente MediaSet

   * Le risorse in linea richiedono la stessa codifica utilizzata per l’URL.

* NavigationView, componente

   * Attualmente il componente non supporta il ridimensionamento.

* PageScrubber, componente

   * Su iPhone 5, quando la bolla PageScrubber è impostata su testo, vengono visualizzati artefatti quando si scorre il pulsante lungo la traccia. L&#39;utilizzo `-webkit-background-clip: content;` nello stile aggira l&#39;argomento.

* SpinView, componente

   * A volte la visualizzazione 360 gradi sembra bloccarsi dopo il gesto di scorrimento e ruotare il dispositivo mentre l’immagine è in rotazione.

* Campioni, componente

   * Quando si seleziona un campione con un limite inferiore, vengono visualizzate 2 evidenziazioni.
   * Scorrimento automatico con `selectSwatch()` metodo non funzionante correttamente.

* VideoPlayer

   * Frame video non aggiornato se la ricerca è impostata su 100% con il fallback impostato su auto.
   * Il blocco occasionale delle macro può verificarsi durante la ricerca video in modalità di streaming HLS nei browser Chrome, Firefox e Internet Explorer.
   * L&#39;immagine poster potrebbe non essere visualizzata nel browser Microsoft Edge per la prima volta dal visitatore.
   * L&#39;immagine poster potrebbe nascondersi dopo il caricamento del video in Internet Explorer 9 quando si utilizza la riproduzione progressiva.

## Scene7 Image Serving 6.3.2 and Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utility IC: il flag non è più supportato `downsample2x2` . Questo flag era un downsampling 2x2 di scarsa qualità che non è più utilizzato da IPS.
* Intestazione CORS - Attualmente, l&#39;intestazione CORS è configurata per `/is/content/` le richieste.

