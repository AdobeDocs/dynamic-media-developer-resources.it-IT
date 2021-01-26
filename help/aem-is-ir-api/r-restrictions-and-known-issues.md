---
description: Quando si utilizza Dynamic Media Image Serving è necessario tenere in considerazione alcuni problemi noti e limitazioni.
seo-description: Quando si utilizza Dynamic Media Image Serving è necessario tenere in considerazione alcuni problemi noti e limitazioni.
seo-title: Restrizioni e problemi noti
solution: Experience Manager
title: Restrizioni e problemi noti
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# Restrizioni e problemi noti{#restrictions-and-known-issues}

Quando si utilizza Dynamic Media Image Serving è necessario tenere in considerazione alcuni problemi noti e limitazioni.

## Correzione documentazione {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* Il numero di righe non supera il massimo dell&#39;impostazione `\copyfitmaxlines` e il numero di righe esplicite nel testo immesso.
* Nei set di immagini sono necessarie parentesi graffe e parentesi corrispondenti. Se le parentesi graffe e le parentesi non corrispondono, devono essere codificate nell’URL.
* L&#39;avviso sul tempo di risposta globale lato server include le risposte agli errori.
* Il comando `id=` è attualmente richiesto quando si utilizza il comando `rect=` con una richiesta di immagine o maschera.

## Differenze note textPs= rispetto a text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* Il rendering del corsivo sintetico viene eseguito meno inclinato rispetto a quando si utilizza `text=`.
* La sottolineatura è un po&#39; più bassa e sottile rispetto all&#39;utilizzo di `text=`.
* `\expnd` e  `\expndtw` utilizzati con valori negativi elevati, i caratteri vengono posizionati l&#39;uno davanti all&#39;altro durante l&#39;uso  `text=`.

* `\charscaley` viene ridimensionata in modo diverso rispetto all&#39;uso,  `text=` ma non influisce sull&#39;altezza della riga.

* Se l&#39;ultima riga di testo non rientra, l&#39;intera riga viene eliminata invece di essere visualizzata come interruzione.
* `\slmult` e  `\sl` si comportano in modo diverso da MS Word e  `text=`, diventano semplicemente efficaci per i paragrafi correnti e successivi.

* `\sb` viene applicato al primo paragrafo sia per MS Word che per  `text=`,  Adobe InDesign e Photoshop non lo fanno.

* `\sa` si applica all&#39;ultimo paragrafo per Microsoft Word e  `text=`,  Adobe InDesign e Photoshop non lo fanno.

## Compatibilità con le versioni precedenti {#section-a76842f751944f4fb664af296d064122}

* La fuga del carattere di sottolineatura ( `\_`) in una stringa RTF non funziona con tutti i font che utilizzano `textPs=`

* Non è supportata la gestione delle macro con distinzione tra maiuscole e minuscole.
* La cache del catalogo è stata ridotta da 60 a 10 secondi.
* La funzione di reindirizzamento degli errori ora reindirizza solo le richieste che fanno riferimento a immagini danneggiate, font, profili colore e immagini pubblicate in un catalogo, ma non trovate sul disco.
* `posN=`,  `anchor=`,  `anchorN=`,  `origin=`e  `originN=` ora restituiscono un errore di analisi se uno dei valori del modificatore è maggiore di 2147483648.

* La codifica delle richieste nidificate non è supportata. Transizione verso il nuovo comportamento e decodifica di eventuali valori di richiesta nidificati presenti nelle richieste URL sul sito e nei cataloghi aziendali.
* DefaultImage applica ora gli attributi delle miniature quando si utilizza `req=tmb`.
* Nelle versioni precedenti con `flip=`, l&#39;immagine non veniva mai riposizionata indipendentemente dal punto di ancoraggio.

## Restrizioni applicabili alle librerie di terze parti {#section-79768b96bf634e44ab672c5b893f343d}

La libreria Digimarc rifiuta di applicare una filigrana Digimarc a un&#39;immagine, se già rilevata. Se a un&#39;immagine principale viene apportata una modifica sufficiente, la libreria Digimarc potrebbe essere in grado di riconoscere che la filigrana è stata applicata. Tuttavia, potrebbe non essere in grado di leggere tali informazioni. In questo modo si ottiene una nuova immagine in cui non è possibile ottenere le informazioni Digimarc originali applicate all’immagine originale. Image Server può ora applicare la filigrana Digimarc definita nel catalogo aziendale.

## Restrizioni applicabili sia al server immagini che al rendering delle immagini {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* Image Server e Image Rendering potrebbero non sfruttare appieno tutte le CPU quando sono disponibili più di 4 CPU. Simulare il traffico su questi computer per vedere quanto sia vantaggioso con più di 4 CPU.
* Gli URL remoti che restituiscono un reindirizzamento (stati HTTP 301, 302 o 303) vengono rifiutati.
* Durante la configurazione di `errorRedirect.rootUrl` l&#39;indirizzo IP definito in questa proprietà deve essere incluso nel valore del tag ruleset `<addressfilter>` su tale server.

   *Esempio*:

   Il server A ha definito `errorRedirect.rootUrl=10.10.10.10` .

   Il server B, che ha l&#39;indirizzo IP 10.10.10.10, imposta il valore del tag `<addressfilter>` nel file ruleset in modo che includa il suo indirizzo IP (10.10.10.10).

* Il testo punto e il tracciato di testo con il posizionamento possono presentare un ritaglio.
* `text=` viene applicato solo  `\sa` e  `\sb` all’intero blocco di testo, non per paragrafo.

* Quando si utilizza una società definita nell&#39;URL e un&#39;altra società definita per il modificatore `src=` o `mask=`, è necessario assegnare il prefisso a una barra in avanti alla società definita per `src=` o `mask=` affinché questo modulo di richiesta funzioni.

   *Esempio*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   Invece di: `/is/image/MyCompany?src=YourCompany/MyImage` .

* Le richieste Tiff o vignettatura non piramidali generano un messaggio di errore simile a

   *&quot;L&#39;immagine non  `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` ha un DSF valido e un&#39;area di 2,25 MPixel supera il massimo di 2 MPixel&quot;* .

   Come procedura ottimale si consiglia di utilizzare polsini piramidali e vignettature. Se avete la necessità di utilizzare poligonali o vignettature non piramidali, seguite le istruzioni riportate di seguito per aumentare il limite di dimensione.

   *Soluzione*:

   Per il rendering di immagini con vignettature non a piramide, aumentate il valore della proprietà per IrMaxNonPyrVignetteSize nel file di configurazione [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

   Per i TIFF non piramidali di Image Server, aumentate il valore della proprietà per `MaxNonDsfSize` nel file di configurazione [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml].

*  Adobe Photoshop CS3 non salva i file PSD con più livelli per impostazione predefinita, come immagine composita.

   *Sintomi*:

   Il  file PSD con livelli Adobe Photoshop CS3 viene visualizzato in nero con testo che indica: &quot;Il file Photoshop con più livelli non è stato salvato con un&#39;immagine composita&quot;. per l’immagine di risposta Image Server o in IPS.

   *Soluzione*:

   Salvate il file Adobe Photoshop CS3  con l&#39;opzione di massimizzazione della compatibilità attivata.

* Se si assegna il profilo ICC a un&#39;immagine di risposta CMYK/JPEG, in alcuni browser i colori vengono invertiti.*Soluzione*:

   Modificare il formato immagine della risposta utilizzando `fmt=`

* La dimensione dei dati immagine della risposta HTTP dopo la compressione, inclusa l’intestazione del file, è limitata a 16 MB.
* &quot; ..&quot; non è consentito in alcun elemento percorso nelle richieste HTTP.
* La disinstallazione può rimuovere il file creato dall&#39;utente o modificato da *[!DNL install_root]* o da qualsiasi sottocartella. Copiate tali file in un percorso diverso prima di disinstallare.

## Restrizioni applicabili solo a Image Server {#section-b08ad535e4454265b8157dec244c4faf}

* I colori di primo piano nel comando RTF ( `\cf`) non sono supportati per il testo PhotoFont.
* La sintassi in grassetto, corsivo e grassetto/corsivo verrà rifiutata come errore per il testo PhotoFont.
* Lo scorrimento verticale del testo non è supportato per il testo PhotoFont.
* Le immagini PNG a 16 bpc non sono supportate per il testo PhotoFont.
* Le correzioni colore per le immagini PNG con profili colore incorporati utilizzano opzioni hard-coded. L&#39;intento di rendering è colorimetrico relativo e la compensazione del punto nero è attivata per il testo PhotoFont.
* La ricerca basata su file non è supportata quando la traduzione locale è abilitata nel file della società [!DNL ini].
* Image Server non scrive correttamente percorsi Photoshop non chiusi.
* Image Server non supporta attualmente l&#39;elaborazione di file TIFF esportati con Adobe Media Encoder 4.0.1 o versioni precedenti. Adobe Media Encoder è incluso in Premiere Pro CS4,  After Effects CS4 e Creative Suite 4 Production Premium.
* L&#39;utilizzo di `text=` con livelli di ridimensionamento automatico non supporta stringhe RTF che utilizzano più di un&#39;impostazione per la giustificazione della riga.

   *Esempio*

   La stringa RTF non può utilizzare la giustificazione della riga sinistra e della riga destra per un livello di testo con ridimensionamento automatico.

* SVG dispone di una propria proprietà per il percorso di ricerca dei font di riferimento che non sono incorporati nel file SVG.

   *Sintomi*

   Le immagini SVG sottoposte a rendering che contengono definizioni di font utilizzano un font errato.

   *Soluzione*

   Impostare la proprietà `svgProvider.fontRoot=` in [!DNL install_root/ImageServing/conf/PlatformServer.conf] .

* Il ritaglio utilizza attualmente `bgColor=` invece di `color=` per riempire l&#39;area estesa di recente.

* La conversione del colore potrebbe non essere corretta se `bgColor=` non corrisponde allo spazio colore di base relativo ai profili colore.
* Gli effetti di livello esterno non vengono sottoposti a rendering se il livello non dispone di una maschera o di dati alfa.

## Restrizioni applicabili solo al rendering delle immagini {#section-4c6949e797174607a3d1ab4d3d4a725a}

* Decorazioni e materiali da parete non sono rimovibili.
* Le dimensioni delle texture sono limitate rispetto alle dimensioni della vista vignettatura. In rare circostanze, il limite predefinito del 425% delle dimensioni di visualizzazione potrebbe interferire con un&#39;applicazione che utilizza texture molto grandi e non ripetibili. Se non è possibile modificare l&#39;applicazione o il contenuto in modo che funzioni entro i limiti predefiniti, la percentuale può essere aumentata come segue. Utilizzando un editor di testo, aprire [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml], individuare `IrMaxTextureSizeFactor` e immettere un nuovo valore percentuale. La modifica ha effetto immediato senza riavviare il server immagini.

* I motori JavaScript nei dati di risposta della cache Netscape e Opera anche se è impostata l&#39;intestazione nocache. Ciò interferisce con il corretto funzionamento delle richieste statiche.

   *Soluzione*

   Aggiungete una marca temporale o un altro identificatore univoco alla stringa di richiesta, ad esempio `"&.ts=currentTime`.

## Restrizioni applicabili solo alle utility {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`a volte si verifica un arresto anomalo con un errore di segmentazione quando interrotto con un  `control-c`.
