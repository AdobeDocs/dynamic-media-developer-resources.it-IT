---
title: Rilascio di Scene7 - Autunno 2016
description: Note aggiornate sulla versione di Adobe Scene7 - Autunno 2016, parte della soluzione Adobe Experience Manager di Adobe Experience Cloud.
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '2236'
ht-degree: 0%

---

# Rilascio di Scene7 - Autunno 2016{#scene-fall-release}

Note aggiornate sulla versione di Adobe Scene7 - Autunno 2016 - parte della soluzione Adobe Experience Manager in Adobe Experience Cloud.

## Rilascio di Scene7 - Autunno 2016 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

Note aggiornate sulla versione di [!DNL Adobe Scene7] - Autunno 2016 - parte della soluzione [!DNL Adobe Experience Manager] in [!DNL Adobe Experience Cloud].

* [Generali](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [Visualizzatori (Image Server 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [Visualizzatori (Image Server 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [Visualizzatori (Image Server 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic Image Serving 6.3.2 e Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## Generali {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe è entusiasta di annunciare la disponibilità della distribuzione HTTP/2 dei contenuti che offre il vantaggio complessivo di prestazioni migliorate.

Consulta [Domande frequenti sulla distribuzione HTTP2 dei contenuti](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html?lang=it#dynamic).

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

Per la documentazione completa, vedi [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html?lang=it](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html?lang=it)

**Nuove funzioni, miglioramenti e correzioni di bug**

* La funzionalità remix video è stata rimossa dall&#39;interfaccia utente [!DNL Adobe Scene7 Publishing System].
* Se necessario e possibile, è stata aggiunta l’autenticazione a tutti i servlet Scene7
* Correzione di bug relativi alla vista a elenco nel cestino.
* La funzionalità utente **Crea Dynamic Media Classic (Scene7) Amministratore** è stata rimossa da Gestione utenti a causa di problemi di sicurezza.
* FTP WebAdmin ora supporta l&#39;autenticazione OKTA.
* È stata rimossa la funzione della password predefinita creata per i nuovi utenti di Media Portal.
* Correzione di bug relativi alla password temporanea generata quando è stato aggiunto un nuovo utente. La password non soddisfa i requisiti necessari.
* Risoluzione dei problemi relativi al disco radice WebAdmin pieno.
* Correzione di bug che comporta la disabilitazione di un utente che non viene riflessa immediatamente nell’interfaccia utente.
* Correzione di bug che comporta l’eliminazione di un utente e che non ti ha consentito di ricrearlo in un secondo momento.
* Correzione di bug relativi all&#39;e-mail di benvenuto inviata ai nuovi utenti di Scene7 che non includeva l&#39;autenticazione per controllare alcune impostazioni.
* Correzione di bug a causa del quale non è stato possibile recuperare un elenco di cartelle FTP se il nome di una cartella conteneva caratteri speciali.
* Configurare i provider di servizi OKTA per gli ambienti Scene7.
* È stato aggiunto il supporto per l’ID organizzazione di Experience Cloud per Viewer Analytics.
* È stato implementato il consumer SAML di Scene7.

## Visualizzatori (Image Server 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

Per la documentazione completa, consulta [Guida di riferimento visualizzatori](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=it).

**Correzioni di bug per Image Server 5.5.3**

* Compatibilità con le librerie RequireJS e DOJO.

  Memorizzazione consolidata nella cache di SDK JS durante l’implementazione del visualizzatore.

## Visualizzatori (Image Server 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

Per la documentazione completa, consulta [Guida di riferimento visualizzatori](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=it).

**Correzioni di bug per Image Server 5.5.2**

* Impossibile riprodurre il video in Internet Explorer 11 su Windows 7.
* `initialframe` non influiva sulla modalità verticale sui dispositivi mobili per HTML5 eCatalog.

## Visualizzatori (Image Server 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

Per la documentazione completa, consulta [Guida di riferimento visualizzatori](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=it).

**Nuove funzioni, miglioramenti e correzioni di bug per Image Server 5.5.1**

* Visualizzatore eCatalog HTML5 con funzione di ricerca.
* È stata aggiunta la riproduzione video in streaming di HLS come metodo di distribuzione video predefinito per la maggior parte dei sistemi desktop. Lo streaming video HDS basato su Flash è ancora disponibile come opzione di riproduzione alternativa.
* È stato aggiunto il supporto per dispositivi con input sia per il mouse che per il tocco che eseguono il browser Chrome.
* È stato aggiunto il supporto per Experience Cloud Org ID all’integrazione Analytics.
* Aggiorna la libreria JavaScript di AppMeasurement alla versione 1.6.1.
* È stato aggiunto il supporto per l’orientamento da destra a sinistra nel visualizzatore eCatalog.
* È stato risolto un problema a causa del quale `tip=0,-1,0` causava un errore fuori intervallo.

**Note sulla compatibilità**

* Blackberry®

   * Incompatibilità con i set AVS precedenti. I client devono ricaricare i set AVS per consentire la riproduzione.

* Generali

   * Il ridimensionamento del lato browser può causare la sfocatura dell’interfaccia utente e delle immagini quando l’utente si ingrandisce nella pagina. La formattazione dell’interfaccia utente potrebbe non essere visualizzata correttamente a seconda dello zoom. Questo effetto viene trasferito allo schermo intero.
   * A causa delle dimensioni limitate dei dispositivi mobili, il visualizzatore di file multimediali diversi utilizza il movimento della diapositiva per scambiare i fotogrammi nei set di immagini incorporati invece di toccare il componente Campioni incorporati. Il componente è presente come indicatore visivo.
   * Nei browser di Internet Explorer e in alcuni dispositivi touch, la modalità a schermo intero non occupa l&#39;intero schermo del dispositivo. Piuttosto, ridimensiona l’applicazione alle dimensioni della finestra del browser.
   * Il pulsante Chiudi non funziona con iOS 8.0 e 8.1, ma non è più disponibile in iOS 8.2

* Galaxy SIII

   * Perdita di memoria rilevata con i visualizzatori Zoom ed eCatalog HTML5. La navigazione ripetuta attraverso i frame può causare l&#39;arresto anomalo del browser.
   * Il doppio tocco sul visualizzatore può causare lo zoom di un’intera pagina invece che del solo visualizzatore con ridimensionamento lato browser abilitato.

* Galaxy S4

   * Dispositivo rilevato come tablet in modalità verticale con schermo intero selezionato nelle impostazioni del browser.

* Galaxy Nexus

   * Il doppio tocco sul visualizzatore può causare lo zoom di un’intera pagina invece che del solo visualizzatore con ridimensionamento lato browser abilitato.

* Galaxy Nexus 10 e Galaxy Tablet

   * L’eCatalog mostra pagine affiancate non corrette con orientamenti in verticale e orizzontale.

* Dispositivi mobili HTC

   * I risultati di Adobe sui dispositivi mobili HTC mostrano che l’incapacità di disabilitare lo zoom nativo con pressione è una &quot;funzione&quot; del wrapper dell’interfaccia utente HTC (HTC Sense). Questo problema può causare lo zoom dell’intera pagina quando si utilizza il gesto &quot;pizzica per ingrandire&quot; sul visualizzatore. Suggerisci invece di utilizzare il doppio tocco.
   * Le icone della mappa immagine possono sovrapporsi se le mappe immagine sono piccole e vicine tra loro.

* Video HTML5

   * Internet Explorer 9: le immagini poster personalizzate non vengono visualizzate.
   * Il modificatore `IntialBitRate` è supportato solo con la riproduzione di software HLS e Flash HDS. Non funziona se la riproduzione utilizza il lettore nativo.
   * Riproduzione progressiva OGG e WebM non attualmente supportata.
   * Il ridimensionamento del browser può causare la visualizzazione del lettore video con dimensioni non corrette (incluse le impostazioni di visualizzazione del pannello di controllo del sistema operativo Windows).
   * La ricerca di video con lo streaming HLS su Safari potrebbe non essere coerente.

* Internet Explorer

   * La modalità Quirks non è attualmente supportata.
   * La modalità di compatibilità non è attualmente supportata.
   * Internet Explorer su dispositivi mobili non è attualmente supportato.

* iOS

   * Gli eCatalog di grandi dimensioni possono causare un arresto anomalo del browser in iPad 2.
   * I telefoni iPhone 6+ vengono rilevati come tablet dai visualizzatori.

* Safari

   * Safari 6.1 o versione successiva: le impostazioni dei plug-in Internet potrebbero impedire la riproduzione di video Flash.
   * La ricerca video con lo streaming HLS su Safari potrebbe non essere coerente.
   * Impossibile cercare la fine del video su Safari 6 utilizzando lo streaming HLS.

**Problemi noti e restrizioni**

* I modificatori Image Server di `iscommands` non sono stati aggiunti alla richiesta `req=set` per progettazione. I modificatori che influiscono solo sulla visualizzazione delle immagini funzionano correttamente. I modificatori che influiscono sulle dimensioni devono essere utilizzati in una risorsa complessa. Ad esempio:

  `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [A comparsa] IE9 a volte rimane sullo schermo dopo lo spegnimento del mouse.
* Il ridimensionamento del browser non funziona correttamente.
* iPad 2: una risorsa di eCatalog di grandi dimensioni provoca l’arresto anomalo di Safari su iOS.
* Tutti i visualizzatori

   * Filigrane, offuscamento e blocco non sono supportati.
   * I predefiniti per immagini non sono supportati.
   * L&#39;aggiunta o la rimozione del visualizzatore dal DOM tramite CSS `display:none` o il suo distacco dinamico dal nodo padre non è attualmente supportato.

* Tutti i visualizzatori HTML5

   * L’incorporamento del visualizzatore nella tabella potrebbe causare un ridimensionamento o un posizionamento errato del visualizzatore in modalità a schermo intero non nativa. Consiglia invece di utilizzare i DIV.
   * I parametri con nomi di istanza espliciti nel codice richiedono che i nomi di istanza nell&#39;URL vengano sovrascritti (ad esempio, `zoomView.iconfeffect=0`).
   * Il ritaglio dei comandi Image Server non è attualmente supportato.
   * Il pulsante Chiudi funziona solo se il visualizzatore è aperto nella finestra figlio.
   * Il modificatore `iscommands` non supporta i modificatori Image Server che influiscono sulle dimensioni dell&#39;immagine.

* eCatalog HTML5

   * Quando si passa a un’altra pagina di HTML e si ritorna, il visualizzatore torna occasionalmente alla prima pagina.
   * Il layout di pagina viene visualizzato occasionalmente in modo errato dopo la rotazione del dispositivo iOS. Lo zoom nella pagina corregge il layout.
   * Collegamenti interni solo alla pagina più a sinistra in pagine affiancate multipagina. Interessa i dispositivi mobili in modalità verticale.
   * InitalFrame effettua il collegamento solo alla pagina più a sinistra negli spread multipagina. Interessa i dispositivi mobili in modalità verticale.
   * A causa di limitazioni del browser, la funzione di stampa non è disponibile in IE9.

* File multimediali diversi HTML5

   * La riproduzione della colonna sonora non è supportata.

* HTML5 Social

   * Per eseguire correttamente il rendering delle miniature nell&#39;e-mail in uscita, il modificatore `serverurl` deve avere un URL assoluto.

* Video HTML5

   * L&#39;immagine del poster potrebbe contenere un errore di &quot;dimensione massima&quot;. La società deve aumentare il limite impostato per la pubblicazione da server immagini.
   * I sottotitoli video richiedono un set di regole aziendali se la pagina HTML in hosting viene trasmessa da un server esterno (non da un server Scene7). Per assistenza, contatta il supporto Adobe.
   * Il tracciamento di Analytics potrebbe segnalare una percentuale di riproduzione errata a causa del buffering
   * Sui dispositivi iPad o Android™ è possibile che venga visualizzata una cornice nera invece di un&#39;immagine poster.
   * Il fotogramma nero può lampeggiare sullo schermo durante il caricamento del visualizzatore su dispositivi iPad o Android™.
   * I bordi neri vengono visualizzati sul lato del componente VideoPlayer quando lo sfondo è impostato su bianco/trasparente sui dispositivi iPad.
   * L’ultimo fotogramma del video potrebbe essere distorto su iPad con iOS 7.
   * Occasionalmente si possono verificare macroblocchi durante la ricerca di video in modalità streaming HLS nei browser Chrome, Firefox e Internet Explorer.
      * L’immagine del poster potrebbe non essere visualizzata per la prima volta nel browser Microsoft® Edge.
      * L&#39;immagine poster potrebbe nascondersi dopo il caricamento del video in Internet Explorer 9 quando viene utilizzata la riproduzione progressiva.

## SDK visualizzatore Scene7 HTML5 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

La Guida utente si trova nella cartella Adobe HTML5 Viewer SDK dell’installazione client. La documentazione API dei componenti si trova nella sottocartella docs dell’installazione client.

**Correzioni di bug per 3.0.2**

* VideoPlayer - Impossibile riprodurre il video in Internet Explorer 11 su Windows 7.
* Sommario - `initialframe` non ha influito sulla modalità ritratto sui dispositivi mobili per il visualizzatore eCatalog di HTML5.

**Nuove funzioni, miglioramenti e correzioni di bug per 3.0.1**

* Generali

   * È stata aggiunta la riproduzione video in streaming di HLS come metodo di distribuzione video predefinito per la maggior parte dei sistemi desktop. Lo streaming video HDS basato su Flash è ancora disponibile come opzione di riproduzione alternativa.
   * Sono stati aggiunti i componenti SearchManager, SearchPanel, SearchEffect e SearchButton per supportare la nuova funzione di ricerca nei visualizzatori eCatalog.
   * È stato aggiunto il supporto per dispositivi con input tocco e mouse in esecuzione sul browser Chrome.
   * Rilevamento delle versioni Android™ con refactoring per supportare le versioni future del sistema operativo.
   * È stato aggiunto il supporto per l’orientamento da destra a sinistra nei componenti SDK specifici per eCatalog.

* Barra di controllo

   * È stato aggiunto lo scorrimento opzionale del contenuto della barra di controllo nel caso in cui non rientri nella larghezza disponibile.

* FlyoutzoomView

   * È stato corretto un caso in cui `tip=0,-1,0` causava un errore fuori intervallo.

**Note sulla compatibilità**

* Android™ 4.x

   * Per disattivare l’impostazione predefinita, evidenziazione blu: è necessario aggiungere la seguente regola CSS per il componente:

     `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry®

   * La riproduzione video potrebbe cessare quando si modificano i flussi della velocità bit nei set AVS.

* Chrome

   * Eventuali chiamate API che forzano la ricostruzione dei componenti potrebbero essere ignorate a causa del caching interno di Chrome.

* Galaxy SIII

   * A volte il visualizzatore non viene caricato a schermo intero.
   * Al momento Pageview soffre di una perdita di memoria sul dispositivo.
   * Il movimento del doppio tocco ingrandisce il visualizzatore e la pagina quando è attiva la modifica in scala laterale del browser.

* Galaxy Nexus

   * Artefatti visualizzati su alcuni componenti della vista.
   * Il movimento del doppio tocco ingrandisce il visualizzatore e la pagina quando è attiva la modifica in scala laterale del browser.

* IPAD 3

   * IPad 3 ha una risoluzione nativa di 2048x1536. Questa risoluzione può causare problemi di visualizzazione se la pubblicazione IS dell&#39;azienda, il limite di dimensione dell&#39;immagine è impostato più basso.

* IPHONE4

   * Icona di ripetizione Iconeffect sostituita con icona di riproduzione dopo lo scorrimento della pagina.

* Internet Explorer

   * In IE 10 e versioni precedenti la modalità a schermo intero non occupa l&#39;intero schermo, ma semplicemente ridimensiona l&#39;applicazione alle dimensioni della finestra del browser.
   * La modalità di rendering Quirks non è supportata.
   * Internet Explorer su dispositivi mobili non è attualmente supportato.
   * Il caricamento di Util.js potrebbe non riuscire se incluso in modo asincrono.
   * L&#39;icona IconEffect blocca gli eventi di clic sui componenti SpinView e ZoomView.

* Lettori video per dispositivi nativi

   * I componenti dell’interfaccia utente di livello su VideoPlayer non sono supportati quando VideoPlayer viene utilizzato per chiamare il lettore nativo del dispositivo.
   * La riproduzione video in modalità nativa non è coerente in Safari 6.
   * La riproduzione nativa sostituisce l’icona di ripetizione con l’icona di riproduzione dopo lo scorrimento della pagina.

* Dispositivi touch

   * la modalità a schermo intero non occupa l’intero schermo del dispositivo, ma si limita a ridimensionare l’applicazione in base alle dimensioni della finestra del browser.
   * I cursori personalizzati non funzionano sui dispositivi touch.
   * Il ridimensionamento delle pagine sui dispositivi touch non è attualmente supportato. L’incorporamento dei visualizzatori HTML5 richiede il metatag viewport con le impostazioni appropriate.

* Xoom

   * Il movimento del doppio tocco ingrandisce il visualizzatore e la pagina quando è attiva la modifica in scala laterale del browser.

**Problemi noti e restrizioni**

* Tutti i componenti

   * Nelle versioni 2.7.2 e precedenti, alcuni componenti sono stati aggiunti al DOM utilizzando l&#39;API `insertBefore()`. Di conseguenza, tali componenti si posizionano in fondo all’ordine di sovrapposizione, indipendentemente dal momento in cui viene creata l’istanza del componente rispetto ad altri componenti. Con la versione 2.8.1 tutti i componenti utilizzano ora l&#39;API `appendChild()`, il che significa che l&#39;ordine di impilamento dei componenti corrisponderebbe all&#39;ordine di creazione dell&#39;istanza.

   * L&#39;utilizzo del modificatore `iscommand` per impostare il formato del canale alfa dell&#39;immagine non è supportato. Utilizzare il parametro `FMT` del componente.
   * La proprietà di trasformazione CSS non è attualmente supportata.

* Dispositivi touch

   * Il movimento di pizzicamento sui dispositivi touch non genera un evento di zoom

* Contenitore

   * Bordo, spaziatura interna e margini sul contenitore non supportati. Adobe consiglia di aggiungere elementi di stile all’elemento DIV principale.
   * È necessario impostare in modo esplicito la dimensione del contenitore o i componenti possono essere ridimensionati correttamente.

* Stampa componente

   * A causa di limitazioni del browser, in Internet Explorer 9 il componente Stampa potrebbe non ridimensionare correttamente il contenuto sulla carta.

* Componente IconEffect

   * IconEffect genera un errore di script in Internet Explorer se `autohide` è disabilitato (impostato su `0`).

* Componente ImageMapEffect

   * Ritarda con l’icona di riposizionamento durante la panoramica dell’immagine nel componente Vista.

* Componente MediaSet

   * Le risorse in linea richiedono la stessa codifica dell’URL.

* Componente NavigationView

   * Attualmente il componente non supporta il ridimensionamento.

* Componente PageScrubber

   * In iPhone 5, quando la bolla PageScrubber è impostata sul testo, vengono visualizzati artefatti quando si fa scorrere il pulsante lungo il brano. L&#39;utilizzo di `-webkit-background-clip: content;` nello stile risolve il problema.

* Componente SpinView

   * Talvolta, durante la rotazione dell&#39;immagine, SpinView sembra bloccarsi dopo un gesto di scorrimento e la rotazione del dispositivo.

* Componente Campioni

   * Quando si seleziona un campione fuori dai limiti, vengono visualizzate due evidenziazioni.
   * Lo scorrimento automatico con il metodo `selectSwatch()` non funziona correttamente.

* LettoreVideo

   * Il fotogramma video non viene aggiornato se la ricerca è impostata sul 100% e il fallback è impostato su auto.
   * Il blocco macro occasionale può verificarsi durante la ricerca di video in modalità streaming HLS nei browser Chrome, Firefox e Internet Explorer.
   * L’immagine del poster potrebbe non essere visualizzata per la prima volta nel browser Microsoft® Edge.
   * L&#39;immagine poster potrebbe nascondersi dopo il caricamento del video in Internet Explorer 9 quando viene utilizzata la riproduzione progressiva.

## Image Serving 6.3.2 per Dynamic Media e Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* Utility IC - Il flag `downsample2x2` non è più supportato. Questo flag era un downsampler 2x2 di scarsa qualità che non è più utilizzato da IPS.
* Intestazione CORS - Attualmente, l&#39;intestazione CORS è configurata per `/is/content/` richieste.
