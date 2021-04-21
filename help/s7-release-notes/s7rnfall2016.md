---
description: '"Note aggiornate sulla versione di Adobe Scene7 - Autunno 2016, parte della soluzione Adobe Experience Manager di Adobe Marketing Cloud."'
solution: Experience Manager
title: Rilascio di Scene7 - Autunno 2016
feature: Dynamic Media Classic
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '2238'
ht-degree: 0%

---


# Rilascio di Scene7 - Autunno 2016{#scene-fall-release}

Note aggiornate sulla versione di Adobe Scene7 - Autunno 2016 - parte della soluzione Adobe Experience Manager in Adobe Marketing Cloud.

## Rilascio di Scene7 - Autunno 2016 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Note aggiornate sulla versione per [!DNL Adobe Scene7] Autunno 2016 nella sezione della soluzione [!DNL Adobe Experience Manager] in [!DNL Adobe Marketing Cloud].

* [Generali](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visualizzatori (Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visualizzatori (Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visualizzatori (Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [SDK visualizzatore HTML5 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 e Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Generali {#section-52afeb72ecb34c1585ea67a5051825a2}

L’Adobe è entusiasta di annunciare la disponibilità della distribuzione di contenuti HTTP/2 con il vantaggio complessivo di migliorare le prestazioni.

Consulta [Domande frequenti sulla distribuzione dei contenuti HTTP2](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Per la documentazione completa, consulta [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**Nuove funzioni, miglioramenti e correzioni di bug**

* Funzione di recupero video rimossa dall&#39;interfaccia utente [!DNL Adobe Scene7 Publishing System].
* È stata aggiunta l’autenticazione a tutti i servlet Scene7, se necessario e possibile.
* Correzione di bug che coinvolgono la visualizzazione elenco nel cestino.
* La funzionalità utente **Crea Dynamic Media Classic (Scene7) Admin** è stata rimossa da Gestione utente per motivi di sicurezza.
* WebAdmin FTP ora supporta l’autenticazione OKTA.
* È stata rimossa la funzione della password predefinita creata per i nuovi utenti di Media Portal.
* Correzione di bug relativi alla password temporanea generata all&#39;aggiunta di un nuovo utente. La password non soddisfa i requisiti necessari.
* Sono stati risolti i problemi relativi al disco radice WebAdmin pieno.
* Correzione di bug che comportano la disattivazione di un utente che non si riflette immediatamente nell&#39;interfaccia utente.
* Correzione di bug che comporta l’eliminazione di un utente che non consentiva di ricreare l’utente in un secondo momento.
* Correzione di bug relativi all&#39;e-mail di benvenuto inviata ai nuovi utenti Scene7 che non includevano l&#39;autenticazione per controllare alcune impostazioni.
* Correzione di bug che causava il mancato recupero di un elenco di cartelle FTP se il nome di una cartella conteneva caratteri speciali.
* Configura i provider di servizi OKTA per gli ambienti Scene7.
* È stato aggiunto il supporto per ID organizzazione Marketing Cloud per Viewer Analytics.
* Implementazione del consumer Scene7 SAML.

## Visualizzatori (Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Per la documentazione completa, consulta [Guida di riferimento visualizzatori](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Correzioni di bug per Image Serving 5.5.3**

* Compatibilità con le librerie RequireJS e DOJO.

   Memorizzazione nella cache JS dell’SDK consolidata durante la distribuzione del visualizzatore.

## Visualizzatori (Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Per la documentazione completa, consulta [Guida di riferimento visualizzatori](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Correzioni di bug per Image Serving 5.5.2**

* Impossibile riprodurre il video in Internet Explorer 11 su Windows 7.
* `initialframe` non influiva sulla modalità verticale sui dispositivi mobili per l&#39;eCatalog HTML5.

## Visualizzatori (Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Per la documentazione completa, consulta [Guida di riferimento visualizzatori](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html).

**Nuove funzioni, correzioni e miglioramenti implementati in Image Serving 5.5.1**

* Visualizzatore HTML5 per eCatalog con funzione di ricerca.
* È stata aggiunta la riproduzione video in streaming HLS come metodo di distribuzione video predefinito per la maggior parte dei sistemi desktop. Lo streaming video HDS basato su Flash è ancora disponibile come opzione di riproduzione alternativa.
* È stato aggiunto il supporto per i dispositivi con input sia del mouse che touch tramite il browser Chrome.
* È stato aggiunto il supporto per ID organizzazione Marketing Cloud all’integrazione di Analytics.
* Aggiorna la libreria JavaScript AppMeasurement alla versione 1.6.1.
* È stato aggiunto il supporto per l’orientamento da destra a sinistra nel visualizzatore eCatalog.
* È stato risolto un problema a causa del quale `tip=0,-1,0` causava un errore fuori intervallo.

**Note sulla compatibilità**

* Blackberry

   * Incompatibilità con set AVS precedenti. I clienti potrebbero dover ricaricare i set AVS per consentire la riproduzione.

* Generali

   * Il ridimensionamento lato browser può rendere sfocata l’interfaccia utente e le immagini quando l’utente ingrandisce la pagina. La formattazione dell’interfaccia utente potrebbe anche non essere visualizzata correttamente a seconda dello zoom. Questo passerà allo schermo intero.
   * A causa della limitazione delle dimensioni sui dispositivi mobili, il visualizzatore di file multimediali diversi utilizza il movimento delle diapositive per scambiare i fotogrammi in set di immagini incorporati invece di toccare il componente campioni incorporati. Il componente è presente come indicatore visivo.
   * Nei browser Internet Explorer e in alcuni dispositivi touch, la modalità a schermo intero non occupa l’intero schermo del dispositivo. ma ridimensiona l&#39;applicazione alle dimensioni della finestra del browser.
   * Il pulsante Chiudi non funziona iOS 8.0 e 8.1 ma non si verifica più in iOS 8.2

* Galassia SIII

   * Perdita di memoria visibile con i visualizzatori HTML5 per zoom e eCatalog. La navigazione ripetuta attraverso i frame può causare l&#39;arresto anomalo del browser.
   * Il doppio tocco sul visualizzatore può causare lo zoom di tutta la pagina invece del solo visualizzatore con ridimensionamento lato browser abilitato.

* Galaxy S4

   * Dispositivo rilevato come tablet in modalità verticale con schermo intero selezionato nelle impostazioni del browser.

* Nexus galassico

   * Il doppio tocco sul visualizzatore può causare lo zoom di tutta la pagina invece del solo visualizzatore con ridimensionamento lato browser abilitato.

* Galaxy Nexus 10 e Galaxy Tablet

   * eCatalog mostra pagine con orientamenti per verticale e orizzontale non corretti.

* Dispositivi mobili HTC

   * I nostri risultati sui dispositivi mobili HTC mostrano che l’impossibilità di disabilitare lo zoom nativo con le dita è una &quot;funzione&quot; del wrapper HTC UI (HTC Sense). Questo può causare lo zoom di tutta la pagina quando si utilizza il gesto &quot;pizzico per lo zoom&quot; sul visualizzatore. Suggerisci invece di usare il doppio tocco.
   * Le icone delle mappe immagine possono sovrapporsi se le mappe immagine sono piccole e vicine tra loro.

* Video HTML5

   * Internet Explorer 9: le immagini poster personalizzate non vengono visualizzate.
   * `IntialBitRate` Il modificatore è supportato solo con riproduzione software HLS e Flash HDS. Non funziona quando la riproduzione utilizza il lettore nativo.
   * Riproduzione progressiva OGG e WebM non supportata al momento.
   * Il ridimensionamento del browser può causare la visualizzazione del lettore video con dimensioni errate (incluse le impostazioni di visualizzazione del pannello di controllo del sistema operativo Windows)
   * La ricerca video che utilizza lo streaming HLS su Safari potrebbe non essere coerente.

* Internet Explorer

   * La modalità Quirks al momento non è supportata.
   * Al momento la modalità di compatibilità non è supportata.
   * Al momento Internet Explorer su dispositivi mobili non è supportato.

* iOS

   * Gli eCatalog di grandi dimensioni possono causare l’arresto anomalo del browser sull’iPad 2.
   * I telefoni iPhone 6+ sono rilevati come tablet dai visualizzatori.

* Safari

   * Safari 6.1 o successivo: Le impostazioni dei plug-in Internet possono impedire la riproduzione di video Flash.
   * Il video &quot;cerca&quot; utilizzando lo streaming HLS su Safari potrebbe non essere coerente.
   * Impossibile cercare di terminare il video su Safari 6 utilizzando lo streaming HLS.

**Problemi noti e restrizioni**

* I modificatori Image Server di `iscommands` non vengono aggiunti alla richiesta `req=set` per progettazione. I modificatori che influiscono solo sulla visualizzazione delle immagini funzionano bene. I modificatori che influiscono sulle dimensioni devono essere utilizzati in una risorsa complessa. Ad esempio:

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [] A volte FlyoutIE9 rimane sullo schermo dopo lo spegnimento del mouse.
* Il ridimensionamento del browser causa un ridimensionamento errato.
* iPad 2: Una grande risorsa eCatalog si blocca in Safari su iOS.
* Tutti i visualizzatori

   * Filigrane, offuscamento e blocco non supportati.
   * I predefiniti immagine non sono supportati.
   * Al momento l’aggiunta o la rimozione del visualizzatore dal DOM tramite `display:none` CSS o tramite lo scollegamento dinamico dal nodo principale non è supportato.

* HTML5 Tutti i visualizzatori

   * Se si incorpora un visualizzatore nella tabella, le dimensioni o il posizionamento del visualizzatore potrebbero non essere corretti in modalità a schermo intero non nativa. Suggerisci invece di utilizzare DIV.
   * I parametri con nomi di istanza espliciti nel codice richiedono anche la sovrascrittura dei nomi di istanza nell’URL (ad esempio, `zoomView.iconfeffect=0`).
   * Il comando Ritaglio di Image Server non è al momento supportato.
   * Il pulsante Chiudi funziona solo se il visualizzatore è aperto nella finestra secondaria.
   * Il modificatore `iscommands` non supporta i modificatori Image Server che influiscono sulle dimensioni dell’immagine.

* eCatalog HTML5

   * Se si passa a un’altra pagina HTML e si torna occasionalmente, il visualizzatore viene reimpostato sulla prima pagina.
   * Il layout di pagina talvolta non viene visualizzato correttamente dopo la rotazione del dispositivo iOS. Lo zoom nella pagina corregge il layout.
   * I collegamenti interni collegano solo alla pagina più a sinistra tra quelle affiancate. Influisce sui dispositivi mobili in modalità verticale.
   * I collegamenti InitalFrame collegano solo alla pagina più a sinistra tra quelle affiancate. Influisce sui dispositivi mobili in modalità verticale.
   * A causa di limitazioni del browser, la funzione di stampa non è disponibile in IE9.

* File multimediali diversi HTML5

   * La riproduzione della colonna sonora non è attualmente supportata.

* HTML5 Social

   * Per eseguire correttamente il rendering delle miniature nelle e-mail in uscita, il modificatore `serverurl` deve disporre di un URL assoluto.

* Video HTML5

   * L&#39;immagine poster potrebbe incontrare l&#39;errore &quot;Dimensione massima&quot;. Potrebbe essere necessario aumentare l&#39;impostazione dei limiti per Image Serving Publish.
   * I sottotitoli video richiedono un set di regole aziendali se l’hosting della pagina HTML viene gestito da un server esterno (non da un server Scene7). Per assistenza, contatta il supporto Adobe.
   * Il tracciamento di Analytics potrebbe riportare una percentuale di riproduzione errata a causa del buffering
   * Su dispositivi Android o iPad può essere visualizzato un fotogramma nero invece del poster.
   * Su dispositivi Android o iPad, il fotogramma nero può lampeggiare sullo schermo durante il caricamento del visualizzatore.
   * I bordi neri vengono visualizzati sul lato del componente VideoPlayer quando lo sfondo è impostato su bianco/trasparente sui dispositivi iPad.
   * Su iPad con iOS 7, l’ultimo fotogramma di un video potrebbe essere distorto.
   * Il macroblocco occasionale può verificarsi durante la ricerca video in modalità streaming HLS nei browser Chrome, Firefox e Internet Explorer.
      * L&#39;immagine miniatura potrebbe non essere visualizzata nel browser Microsoft Edge per la prima volta.
      * L&#39;immagine poster può nascondersi dopo il caricamento del video in Internet Explorer 9 quando si utilizza la riproduzione progressiva.

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

La Guida utente si trova nella cartella Adobe HTML5 Viewer SDK dell’installazione client. La documentazione API del componente si trova nella sottocartella docs dell’installazione client.

**Correzioni di bug per la versione 3.0.2**

* VideoPlayer - Impossibile riprodurre il video in Internet Explorer 11 su Windows 7
* TableOfContents - `initialframe` non influisce sulla modalità verticale sui dispositivi mobili per il visualizzatore HTML5 per eCatalog.

**Nuove funzioni, miglioramenti e correzioni di bug per la versione 3.0.1**

* Generali

   * È stata aggiunta la riproduzione video in streaming HLS come metodo di distribuzione video predefinito per la maggior parte dei sistemi desktop. Lo streaming video HDS basato su Flash è ancora disponibile come opzione di riproduzione alternativa.
   * Sono stati aggiunti i componenti SearchManager, SearchPanel, SearchEffect e SearchButton per supportare la nuova funzione Search nei visualizzatori di eCatalog.
   * È stato aggiunto il supporto per i dispositivi con input touch e mouse in esecuzione sul browser Chrome.
   * Rilevamento versione Android ripristinato per supportare versioni future del sistema operativo
   * È stato aggiunto il supporto dell’orientamento da destra a sinistra nei componenti SDK per eCatalog specifici.

* ControlBar

   * È stato aggiunto lo scorrimento facoltativo per il contenuto di ControlBar nel caso in cui non rientri nella larghezza disponibile.

* Visualizzazione zoom a comparsa

   * È stato corretto un caso in cui `tip=0,-1,0` causava un errore fuori intervallo.

**Note sulla compatibilità**

* Android 4.x

   * Per disattivare l’impostazione predefinita, è necessario aggiungere la seguente regola CSS per il componente:

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * La riproduzione video potrebbe cessare quando si modificano i flussi di bit rate nei set AVS.

* Chrome

   * Eventuali chiamate API che forzano la ricostruzione dei componenti possono essere ignorate a causa della memorizzazione nella cache interna di Chrome.

* Galassia SIII

   * A volte il visualizzatore non viene caricato a schermo intero.
   * Pageview soffre di una perdita di memoria sul dispositivo in questo momento.
   * Tocca due volte per ingrandire il visualizzatore e la pagina quando è attivo il ridimensionamento lato browser.

* Nexus galassico

   * Artefatti visualizzati su alcuni componenti di visualizzazione.
   * Tocca due volte per ingrandire il visualizzatore e la pagina quando è attivo il ridimensionamento lato browser.

* iPad 3

   * L&#39;iPad 3 ha una risoluzione nativa di 2048x1536. Questo può causare problemi di visualizzazione se il limite di dimensione dell&#39;immagine dell&#39;azienda è pubblicato, impostato inferiore a quello.

* iPhone4

   * Icona Riproduci effetto sostituita dall’icona Riproduci dopo lo scorrimento della pagina.

* Internet Explorer

   * In IE 10 e la vecchia modalità a schermo intero non occupa l&#39;intero schermo, invece ridimensiona l&#39;applicazione alle dimensioni della finestra del browser.
   * La modalità di rendering delle query non è supportata.
   * Al momento Internet Explorer su dispositivi mobili non è supportato.
   * Util.js potrebbe non riuscire a caricarsi se incluso in modo asincrono.
   * L’icona IconEffect blocca gli eventi di clic sui componenti Visualizzazione 360 gradi e Visualizzazione zoom.

* Lettori video dei dispositivi nativi

   * I componenti dell&#39;interfaccia utente di livello su VideoPlayer non sono supportati quando VideoPlayer viene utilizzato per chiamare il lettore nativo del dispositivo.
   * La riproduzione video in modalità nativa non è coerente in Safari 6.
   * La riproduzione nativa sostituisce l’icona di riproduzione con l’icona di riproduzione dopo lo scorrimento della pagina.

* Dispositivi touch

   * La modalità a schermo intero non occupa l&#39;intero schermo del dispositivo, ma ridimensiona l&#39;applicazione alle dimensioni della finestra del browser.
   * I cursori personalizzati non funzionano sui dispositivi touch.
   * Al momento non è supportato il ridimensionamento della pagina su dispositivi touch. Per incorporare i visualizzatori HTML5 è necessario un tag meta riquadro di visualizzazione con le impostazioni appropriate.

* Xoom

   * Tocca due volte per ingrandire il visualizzatore e la pagina quando è attivo il ridimensionamento lato browser.

**Problemi noti e restrizioni**

* Tutti i componenti

   * Nelle versioni 2.7.2 e precedenti alcuni componenti sono stati aggiunti al DOM utilizzando `insertBefore()` API. Di conseguenza, tali componenti si collocherebbero nella parte inferiore dell’ordine di sovrapposizione, indipendentemente dal momento in cui l’istanza del componente viene creata rispetto ad altri componenti. Con la versione 2.8.1, tutti i componenti utilizzano ora l’ `appendChild()` API , il che significa che l’ordine di sovrapposizione dei componenti corrisponderebbe all’ordine di creazione dell’istanza.

   * L’utilizzo del modificatore `iscommand` per impostare il formato del canale alfa dell’immagine non è supportato. Utilizza invece il parametro del componente `FMT` .
   * Al momento la proprietà di trasformazione CSS non è supportata.

* Dispositivi touch

   * Il gesto di avvicinamento delle dita sui dispositivi touch non genera un evento di zoom

* Contenitore

   * Bordo, spaziatura e margini del contenitore non supportati. Adobe suggerisce di aggiungere elementi di stile al DIV principale.
   * È necessario impostare esplicitamente la dimensione del contenitore oppure i componenti possono essere dimensionati correttamente.

* Componente Stampa

   * A causa di limitazioni del browser, in Internet Explorer 9 il componente per la stampa potrebbe non essere scalato correttamente sul foglio.

* IconEffect, componente

   * IconEffect genera un errore di script su Internet Explorer se `autohide` è disabilitato (impostato su `0`).

* Componente ImageMapEffect

   * Ritardo con l’icona di riposizionamento durante il panning dell’immagine sul componente di visualizzazione.

* Componente MediaSet

   * Le risorse in linea richiedono la stessa codifica dell’URL.

* Componente NavigationView

   * Attualmente il componente non supporta il ridimensionamento.

* Componente PageScrubber

   * Su iPhone 5, quando la bolla PageScrubber è impostata su testo, mostra artefatti quando scorri il pulsante lungo la traccia. L’utilizzo di `-webkit-background-clip: content;` nello stile risolve il problema.

* Componente SpinView

   * SpinView a volte sembra bloccarsi dopo il gesto di scorrimento e ruotare il dispositivo mentre l&#39;immagine è in rotazione.

* Componente Campioni

   * Quando si seleziona un campione fuori limite, vengono visualizzate 2 evidenziazioni.
   * Lo scorrimento automatico con il metodo `selectSwatch()` non funziona correttamente.

* VideoPlayer

   * Frame video non aggiornato se la ricerca è impostata su 100% con il fallback impostato su auto.
   * Il blocco occasionale delle macro può verificarsi durante la ricerca video in modalità streaming HLS nei browser Chrome, Firefox e Internet Explorer.
   * L&#39;immagine miniatura potrebbe non essere visualizzata nel browser Microsoft Edge per la prima volta.
   * L&#39;immagine poster può nascondersi dopo il caricamento del video in Internet Explorer 9 quando si utilizza la riproduzione progressiva.

## Image Serving 6.3.2 e Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2} di Dynamic Media

* Utility IC - Il flag `downsample2x2` non è più supportato. Questo flag era un downsampler 2x2 di scarsa qualità che non è più utilizzato da IPS.
* Intestazione CORS - Attualmente, l’intestazione CORS è configurata per le richieste `/is/content/`.

