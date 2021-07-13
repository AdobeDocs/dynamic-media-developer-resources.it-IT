---
description: Ci sono alcune restrizioni e problemi noti che devono essere presi in considerazione quando si utilizza Dynamic Media Image Serving.
solution: Experience Manager
title: Restrizioni e problemi noti
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 0%

---

# Restrizioni e problemi noti{#restrictions-and-known-issues}

Ci sono alcune restrizioni e problemi noti che devono essere presi in considerazione quando si utilizza Dynamic Media Image Serving.

## errata documentazione {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Il numero di righe non supera il massimo dell’impostazione `\copyfitmaxlines` e il numero di righe esplicite nel testo immesso.
* Nei set di immagini sono necessarie parentesi graffe e parentesi corrispondenti. Se le parentesi graffe e parentesi non corrispondono, devono essere codificate nell’URL.
* L&#39;avviso temporale di risposta globale lato server include le risposte all&#39;errore.
* Il comando `id=` è attualmente richiesto quando si utilizza il comando `rect=` con una richiesta di immagine o maschera.

## Differenze note textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Il corsivo sintetico viene riprodotto meno inclinato rispetto a quando si utilizza `text=`.
* La sottolineatura è un po&#39; più bassa e sottile rispetto all&#39;utilizzo di `text=`.
* `\expnd` e  `\expndtw` utilizzati con valori negativi elevati fanno sì che i caratteri vengano posizionati uno davanti all’altro quando si utilizza  `text=`.

* `\charscaley` viene ridimensionato in modo diverso rispetto all’utilizzo  `text=` ma non influisce sull’altezza della riga.

* Se l’ultima riga di testo non rientra nell’intervallo, l’intera riga viene rilasciata anziché essere visualizzata come interruzione.
* `\slmult` e  `\sl` si comportano in modo diverso da MS Word e  `text=`, hanno semplicemente effetto per i paragrafi correnti e successivi.

* `\sb` si applica al primo paragrafo sia per MS Word che  `text=`, Adobe InDesign e Photoshop non lo fanno.

* `\sa` si applica all&#39;ultimo paragrafo sia per MS Word che  `text=`, Adobe InDesign e Photoshop non lo fanno.

## Compatibilità con le versioni precedenti {#section-a76842f751944f4fb664af296d064122}

* La fuga dal carattere di sottolineatura ( `\_`) in una stringa RTF non funziona con tutti i font che utilizzano `textPs=`

* Supporto della gestione delle macro senza distinzione tra maiuscole e minuscole.
* La cache del catalogo è stata ridotta da 60 secondi a 10 secondi.
* La funzione di reindirizzamento degli errori ora reindirizza solo le richieste che fanno riferimento a immagini corrotte, font, profili di colore e immagini pubblicate in un catalogo, ma non trovate sul disco.
* `posN=`,  `anchor=`,  `anchorN=`,  `origin=` e  `originN=` ora restituisce un errore di analisi se uno dei valori del modificatore è maggiore di 2147483648.

* La codifica delle richieste nidificate non è supportata. Transizione al nuovo comportamento e annulla la codifica di eventuali valori di richiesta nidificati presenti nelle richieste URL sul sito e nei cataloghi aziendali.
* DefaultImage ora applica gli attributi delle miniature quando si utilizza `req=tmb`.
* Nelle versioni precedenti che utilizzano `flip=`, l&#39;immagine non è mai stata riposizionata indipendentemente dal punto di ancoraggio.

## Restrizioni applicabili alle librerie di terze parti {#section-79768b96bf634e44ab672c5b893f343d}

La libreria Digimarc rifiuta di applicare una filigrana Digimarc a un&#39;immagine, se già rilevata. Se si esegue una modifica sufficiente a un&#39;immagine primaria, la libreria Digimarc potrebbe comunque essere in grado di riconoscere che la filigrana è stata applicata. Tuttavia, potrebbe non essere in grado di leggere tali informazioni. Questo si traduce in una nuova immagine in cui non è possibile ottenere le informazioni Digimarc originali applicate all&#39;immagine originale. Image Serving può ora applicare la filigrana Digimarc definita nel catalogo aziendale.

## Restrizioni applicabili sia al servizio immagini che al rendering delle immagini {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Image Server e Image Rendering potrebbero non sfruttare appieno tutte le CPU quando sono disponibili più di 4 CPU. Simula il traffico su questi computer per vedere quanto è vantaggioso con più di 4 CPU.
* Gli URL remoti che restituiscono un reindirizzamento (stati HTTP 301, 302 o 303) vengono rifiutati.
* Durante la configurazione di `errorRedirect.rootUrl` l&#39;indirizzo IP definito in questa proprietà deve essere incluso nel valore di tag `<addressfilter>` del set di regole su tale server.

   *Esempio*:

   Il server A ha definito `errorRedirect.rootUrl=10.10.10.10` .

   Il server B, che ha l&#39;indirizzo IP 10.10.10.10, imposta il valore del tag `<addressfilter>` nel file del set di regole per includere il suo indirizzo IP (10.10.10.10).

* Il testo punto e il tracciato di testo con posizionamento possono presentare ritaglio.
* `text=` si applica solo  `\sa` e  `\sb` all’intero blocco di testo e non al paragrafo.

* Quando utilizzi una società definita nell’URL e un’altra società definita per il modificatore `src=` o `mask=`, devi assegnare il prefisso &quot; forward slash&quot; alla società definita per `src=` o `mask=` affinché questo tipo di richiesta funzioni.

   *Esempio*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   Invece di: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Le richieste Tiff o vignette non piramidate producono un messaggio di errore simile a

   *&quot;L&#39;immagine non  `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` ha un DSF valido e l&#39;area di 2,25MPixel supera il massimo di 2 MPixel&quot;* .

   Si consiglia di utilizzare polsini e vignette piramidali. Se hai bisogno di utilizzare poligonali o vignette non piramidali, segui le istruzioni qui sotto per aumentare il limite di dimensione.

   *Soluzione alternativa*:

   Per Image Rendering di vignette non a piramide, aumenta il valore della proprietà per IrMaxNonPyrVignetteSize nel file di configurazione [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

   Per i TIFF non piramidali di Image Serving, aumentare il valore della proprietà per `MaxNonDsfSize` nel file di configurazione [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

* Adobe Photoshop CS3 non salva i file PSD a livelli per impostazione predefinita un&#39;immagine composita.

   *Sintomi*:

   Il file PSD a livelli Adobe Photoshop CS3 viene visualizzato in nero con testo che indica: &quot;Questo file Photoshop a livelli non è stato salvato con un&#39;immagine composita&quot;. per l&#39;immagine di risposta di Image Serving o in IPS.

   *Soluzione alternativa*:

   Salva il file Adobe Photoshop CS3 con l&#39;opzione di ottimizzazione della compatibilità attivata.

* L&#39;assegnazione del profilo ICC a un&#39;immagine di risposta CMYK/JPEG causa l&#39;inversione dei colori in alcuni browser.*Soluzione alternativa*:

   Modificare il formato immagine della risposta utilizzando `fmt=`

* La dimensione dei dati immagine di risposta HTTP dopo la compressione, inclusa l&#39;intestazione del file, è limitata a 16 MB.
* &quot; ...&quot; non è consentito in alcun elemento del percorso nelle richieste HTTP.
* La disinstallazione può rimuovere il file creato o modificato dall&#39;utente da *[!DNL install_root]* o da qualsiasi sottocartella. Copiare tali file in un percorso diverso prima di disinstallare.

## Restrizioni applicabili solo a Image Serving {#section-b08ad535e4454265b8157dec244c4faf}

* I colori in primo piano nel comando RTF ( `\cf`) non sono supportati per il testo PhotoFont.
* La sintassi in grassetto, corsivo e grassetto/corsivo verrà rifiutata come errore per il testo PhotoFont.
* Il flusso di testo verticale non è supportato per il testo PhotoFont.
* Le immagini PNG a 16 bpc non sono supportate per il testo PhotoFont.
* Le correzioni del colore per le immagini PNG con profili di colore incorporati utilizzano opzioni hard-coded. L&#39;intento di rendering è colorimetrico relativo e la compensazione Blackpoint è attivata per il testo PhotoFont.
* La ricerca basata su file non è supportata quando la traduzione locale è abilitata nel file [!DNL ini] della società.
* Image Server non scrive correttamente i percorsi Photoshop non chiusi.
* Image Serving al momento non supporta l’elaborazione di file TIFF esportati utilizzando Adobe Media Encoder 4.0.1 o versioni precedenti. Adobe Media Encoder è incluso in Premiere Pro CS4, After Effects CS4 e Creative Suite 4 Production Premium.
* L&#39;utilizzo di `text=` con livelli di ridimensionamento automatico non supporta stringhe RTF che utilizzano più di un&#39;impostazione per la giustificazione della riga.

   *Esempio*

   La stringa RTF non può utilizzare sia la giustificazione della riga sinistra che quella destra per un livello di testo con ridimensionamento automatico.

* SVG ha una propria proprietà per il percorso di ricerca dei font dei font a cui si fa riferimento che non sono incorporati nel file SVG.

   *Sintomi*

   Le immagini SVG sottoposte a rendering che contengono definizioni di font utilizzano un font errato.

   *Soluzione alternativa*

   Imposta la proprietà `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* Il ritaglio sta utilizzando `bgColor=` invece di `color=` per riempire qualsiasi area estesa di recente.

* La conversione del colore potrebbe non essere corretta se `bgColor=` non corrisponde allo spazio colore di base che include i profili colore.
* Gli effetti di livello esterno non vengono renderizzati se il livello non ha una maschera o dati alfa.

## Restrizioni applicabili solo al rendering delle immagini {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Le decorazioni e i materiali di parete non sono rimovibili.
* Le dimensioni delle texture sono limitate rispetto alle dimensioni della vista vignetta. In rare circostanze, il limite predefinito del 425% delle dimensioni della visualizzazione può interferire con un&#39;applicazione che utilizza texture non ripetibili molto grandi. Se non è possibile modificare l&#39;applicazione o il contenuto in modo che funzionino entro i limiti predefiniti, la percentuale può essere aumentata come segue. Utilizzando un editor di testo, apri [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], individua `IrMaxTextureSizeFactor` e immetti un nuovo valore percentuale. La modifica ha effetto immediatamente senza riavviare il server di immagini.

* I motori JavaScript in Netscape e Opera dati di risposta della cache anche se l&#39;intestazione nocache è impostata. Ciò interferisce con il corretto funzionamento delle richieste di stato.

   *Soluzione alternativa*

   Aggiungi una marca temporale o un altro identificatore univoco alla stringa di richiesta, ad esempio `"&.ts=currentTime`.

## Restrizioni applicabili solo ai servizi di pubblica utilità {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`a volte si blocca con un errore di segmentazione quando viene interrotto con un  `control-c`.
