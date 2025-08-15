---
description: Quando si utilizza Dynamic Media Image Server, è necessario prendere in considerazione alcune restrizioni e alcuni problemi noti.
solution: Experience Manager
title: Restrizioni e problemi noti
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1233'
ht-degree: 0%

---

# Restrizioni e problemi noti{#restrictions-and-known-issues}

Quando si utilizza Dynamic Media Image Server, è necessario prendere in considerazione alcune restrizioni e alcuni problemi noti.

## Errori nella documentazione {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Il numero di righe non supera il massimo dell&#39;impostazione `\copyfitmaxlines` e il numero di righe esplicite nell&#39;input di testo.
* Nei set di immagini sono necessarie parentesi graffe e parentesi. Se le parentesi graffe e le parentesi non corrispondono, devono essere codificate in URL.
* L&#39;avviso relativo al tempo di risposta globale lato server include risposte di errore.
* Il comando `id=` è attualmente richiesto quando si utilizza il comando `rect=` con una richiesta di immagine o maschera.

## Differenze note textPs= vs text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Il corsivo sintetico viene reso meno inclinato rispetto all&#39;utilizzo di `text=`.
* La sottolineatura è un po&#39; più bassa e sottile di quando si utilizza `text=`.
* `\expnd` e `\expndtw` utilizzati con valori negativi elevati fanno sì che i caratteri vengano posizionati uno davanti all&#39;altro quando si utilizza `text=`.

* `\charscaley` viene ridimensionato in modo diverso rispetto a quando si utilizza `text=`, ma non influisce sull&#39;altezza della riga.

* Se l&#39;ultima riga di testo non è adatta, l&#39;intera riga viene rilasciata invece di apparire come interruzione.
* `\slmult` e `\sl` si comportano in modo diverso rispetto a MS Word e `text=`, ma hanno semplicemente effetto per i paragrafi correnti e successivi.

* `\sb` si applica al primo paragrafo sia per MS Word che per `text=`; Adobe InDesign e [!DNL Photoshop] non eseguono questa operazione.

* `\sa` si applica all&#39;ultimo paragrafo sia per MS Word che per `text=`. Adobe InDesign e [!DNL Photoshop] non eseguono questa operazione.

## Compatibilità con le versioni precedenti {#section-a76842f751944f4fb664af296d064122}

* L&#39;escape del carattere di sottolineatura ( `\_`) in una stringa RTF non funziona con tutti i font che utilizzano `textPs=`

* Supporto della gestione delle macro senza distinzione tra maiuscole e minuscole.
* La cache del catalogo è stata ridotta da 60 secondi a 10 secondi.
* La funzione di reindirizzamento degli errori ora reindirizza solo le richieste che fanno riferimento a immagini, font, profili colore e immagini danneggiati, pubblicati in un catalogo ma non presenti su disco.
* `posN=`, `anchor=`, `anchorN=`, `origin=` e `originN=` ora restituiscono un errore di analisi se uno qualsiasi dei valori del modificatore è maggiore di 2147483648.

* La codifica delle richieste nidificate non è supportata. Transizione al nuovo comportamento e annullamento della codifica di eventuali valori di richiesta nidificati trovati nelle richieste URL sul sito e nei cataloghi aziendali.
* DefaultImage ora applica gli attributi di miniatura quando si utilizza `req=tmb`.
* Nelle versioni precedenti che utilizzavano `flip=`, l&#39;immagine non è mai stata riposizionata indipendentemente dal punto di ancoraggio.

## Restrizioni applicabili alle librerie di terze parti {#section-79768b96bf634e44ab672c5b893f343d}

La libreria Digimarc rifiuta di applicare una filigrana Digimarc a un&#39;immagine, se ne è già stata rilevata una. Se un&#39;immagine primaria viene modificata a sufficienza, la libreria Digimarc potrebbe essere ancora in grado di riconoscere che la filigrana è stata applicata. Tuttavia, potrebbe non essere in grado di leggere tali informazioni. Ciò determina una nuova immagine in cui non è possibile ottenere le informazioni Digimarc originali applicate all&#39;immagine originale. Image Server può ora applicare la filigrana Digimarc definita nel catalogo aziendale.

## Restrizioni applicabili sia a Image Server che a Image Rendering {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Image Server e Image Rendering potrebbero non sfruttare appieno tutte le CPU quando sono disponibili più di 4 CPU. Simulare il traffico su questi computer per verificare il vantaggio con più di 4 CPU.
* Gli URL remoti che restituiscono un reindirizzamento (stati HTTP 301, 302 o 303) vengono rifiutati.
* Durante la configurazione di `errorRedirect.rootUrl`, l&#39;indirizzo IP definito in questa proprietà deve essere incluso nel valore del tag `<addressfilter>` del set di regole in tale server.

  *Esempio*:

  Il server A ha definito `errorRedirect.rootUrl=10.10.10.10`.

  Il server B con indirizzo IP 10.10.10.10 imposta il valore del tag `<addressfilter>` nel file del set di regole in modo da includere il relativo indirizzo IP (10.10.10.10).

* Il testo di punto e il tracciato di testo con posizionamento possono presentare ritagli.
* `text=` applica solo `\sa` e `\sb` all&#39;intero blocco di testo e non per paragrafo.

* Quando si utilizza una società definita nell&#39;URL e un&#39;altra società definita per il modificatore `src=` o `mask=`, è necessario anteporre una barra (/) alla società definita per `src=` o `mask=` affinché questo tipo di richiesta funzioni.

  *Esempio*:

  `/is/image/MyCompany?src=/YourCompany/MyImage`.

  Invece di: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Le richieste Tiff o vignettatura non piramidali generano un messaggio di errore simile a

  *&quot;L&#39;immagine `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` non ha un DSF valido e l&#39;area di 2,25 MPixel supera il massimo di 2 MPixel&quot;* .

  La best practice prevede l’utilizzo di tappeti e vignette piramidali. Se hai bisogno di utilizzare sfarfallii o vignette non piramidali, segui le istruzioni riportate di seguito per aumentare il limite di dimensione.

  *Elaborazione*:

  Per le vignettature non piramidali Image Rendering, aumentare il valore della proprietà per IrMaxNonPyrVignetteSize nel file di configurazione [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

  Per i TIFF non piramidali di Image Server, aumentare il valore della proprietà per `MaxNonDsfSize` nel file di configurazione [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

* Per impostazione predefinita, Adobe [!DNL Photoshop] CS3 non salva i file PSD con livelli in un&#39;immagine composita.

  *Sintomi*:

  Il file PSD con livelli Adobe [!DNL Photoshop] CS3 viene visualizzato in nero con testo che indica: &quot;Il file [!DNL Photoshop] con livelli non è stato salvato con un&#39;immagine composita&quot;. per l’immagine di risposta di Image Server o in IPS.

  *Soluzione alternativa*:

  Salvare il file Adobe [!DNL Photoshop] CS3 con l&#39;opzione di ottimizzazione della compatibilità attivata.

* L&#39;assegnazione di un profilo ICC a un&#39;immagine di risposta CMYK/JPEG causa l&#39;inversione dei colori in alcuni browser.*Elaborazione*:

  Cambia il formato dell&#39;immagine di risposta utilizzando `fmt=`

* La dimensione dei dati immagine di risposta HTTP dopo la compressione, inclusa l’intestazione del file, è limitata a 16 MB.
* &quot;...&quot; non è consentito in alcun elemento path nelle richieste HTTP.
* La disinstallazione può rimuovere il file creato o modificato dall&#39;utente da *[!DNL install_root]* o da qualsiasi sottocartella. Copiare tali file in un percorso diverso prima di disinstallare.

## Restrizioni applicabili solo a Image Server {#section-b08ad535e4454265b8157dec244c4faf}

* I colori di primo piano nel comando RTF ( `\cf`) non sono supportati per il testo PhotoFont.
* La sintesi di grassetto, corsivo e grassetto/corsivo viene rifiutata come errore per il testo di PhotoFont.
* Flusso di testo verticale non supportato per il testo PhotoFont.
* Le immagini PNG a 16 bpc non sono supportate per il testo PhotoFont.
* Le correzioni dei colori per le immagini PNG con profili colore incorporati utilizzano opzioni hardcoded. L&#39;intento di rendering è colorimetrico relativo e la compensazione del punto nero è attivata per il testo PhotoFont.
* La ricerca basata su file non è supportata se la traduzione delle impostazioni locali è abilitata nel file [!DNL ini] della società.
* Image Server non scrive correttamente i percorsi [!DNL Photoshop] non chiusi.
* Image Server non supporta attualmente l&#39;elaborazione di file TIFF esportati con Adobe Media Encoder 4.0.1 o versioni precedenti. Adobe Media Encoder è incluso con Premiere Pro CS4, After Effects CS4 e Creative Suite 4 Production Premium.
* L&#39;utilizzo di `text=` con livelli di ridimensionamento automatico non supporta stringhe RTF che utilizzano più di un&#39;impostazione per la giustificazione delle linee.

  *Esempio*

  La stringa RTF non può utilizzare la giustificazione della riga sinistra e destra per un livello di testo con ridimensionamento automatico.

* SVG dispone di una proprietà specifica per il percorso di ricerca dei font di riferimento che non sono incorporati nel file SVG.

  *Sintomi*

  Le immagini SVG sottoposte a rendering che contengono definizioni di font utilizzano font non corretti.

  *Soluzione alternativa*

  Impostare la proprietà `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf].

* Il ritaglio sta attualmente utilizzando `bgColor=` invece di `color=` per riempire un&#39;area appena estesa.

* La conversione colore potrebbe non essere corretta quando `bgColor=` non corrisponde allo spazio colore di base dei profili colore.
* Se il livello non contiene una maschera o dati alfa, gli effetti del livello esterno non vengono sottoposti a rendering.

## Restrizioni applicabili solo al rendering immagini {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Le decalcomanie e i materiali per pareti non sono rimovibili.
* Le dimensioni delle texture sono limitate rispetto alle dimensioni della vista vignettatura. In rare circostanze, il limite predefinito del 425% della dimensione di visualizzazione può interferire con un&#39;applicazione che utilizza texture non ripetibili di grandi dimensioni. Se non è possibile modificare l’applicazione o il contenuto in modo che funzioni entro i limiti predefiniti, la percentuale può essere aumentata come segue. Utilizzando un editor di testo, aprire [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], individuare `IrMaxTextureSizeFactor` e immettere un nuovo valore percentuale. La modifica ha effetto immediato senza riavviare il server immagini.

* I motori JavaScript nei dati di risposta della cache di Netscape e Opera anche se l’intestazione nocache è impostata. Questo interferisce con il corretto funzionamento delle richieste di conservazione dello stato.

  *Soluzione alternativa*

  Aggiungere una marca temporale o un altro identificatore univoco alla stringa di richiesta, ad esempio `"&.ts=currentTime`.

## Restrizioni applicabili solo ai servizi di pubblica utilità {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`a volte si verifica un arresto anomalo con un errore di segmentazione quando viene interrotto con `control-c`.
