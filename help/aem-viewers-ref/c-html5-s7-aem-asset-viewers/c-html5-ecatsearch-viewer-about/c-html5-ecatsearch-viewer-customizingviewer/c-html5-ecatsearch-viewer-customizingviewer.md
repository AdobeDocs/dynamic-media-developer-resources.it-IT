---
title: Personalizzazione del visualizzatore di ricerca eCatalog
description: Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni comportamentali per il visualizzatore di ricerca eCatalog vengono eseguite creando un CSS personalizzato.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1395'
ht-degree: 0%

---

# Personalizzazione del visualizzatore di ricerca eCatalog{#customizing-ecatalog-search-viewer}

Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni comportamentali per il visualizzatore di ricerca eCatalog vengono eseguite creando un CSS personalizzato.

Il flusso di lavoro consigliato consiste nel prendere il file CSS predefinito per il visualizzatore appropriato, copiarlo in una posizione diversa, personalizzarlo e specificare la posizione del file personalizzato nel `style=` comando.

I file CSS predefiniti si trovano nella posizione seguente:

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quello predefinito. Se viene omessa una dichiarazione di classe, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell&#39;interfaccia utente.

Un modo alternativo di fornire regole CSS personalizzate consiste nell’utilizzare gli stili incorporati direttamente nella pagina web o in una delle regole CSS esterne collegate.

Quando crei CSS personalizzato, tieni presente che il visualizzatore assegna `.s7ecatalogsearchviewer` al relativo elemento DOM contenitore. Se utilizzi un file CSS esterno passato con `style=` comando, utilizza `.s7ecatalogsearchviewer` come classe padre nel selettore discendente per le regole CSS. Se stai utilizzando stili incorporati nella pagina web, devi qualificare questo selettore anche con un ID dell’elemento DOM contenitore come segue:

`#<containerId>.s7ecatalogsearchviewer`

## Creazione di CSS reattivo {#section-c1e74f5114ad418884ca1c95f5ea5b63}

È possibile eseguire il targeting di dispositivi diversi e incorporare dimensioni in CSS per rendere il contenuto visualizzato in modo diverso, a seconda del dispositivo di un utente o di un particolare layout di pagina web. Questo targeting include, ma non è limitato a, layout di pagina web diversi, dimensioni degli elementi dell’interfaccia utente e risoluzione del disegno.

Il visualizzatore supporta due metodi per creare CSS dinamici: marcatori CSS e query multimediali CSS standard. È possibile utilizzare questi metodi in modo indipendente o insieme.

**Marcatori CSS**

Per creare un CSS dinamico, il visualizzatore supporta i marcatori CSS che specifiche classi CSS vengono assegnate in modo dinamico all’elemento contenitore del visualizzatore di primo livello in base alle dimensioni del visualizzatore in fase di esecuzione e al tipo di input sul dispositivo corrente.

Il primo gruppo di marcatori CSS include `.s7size_large`, `.s7size_medium`, e `.s7size_small` classi. Vengono applicati in base all’area di runtime del contenitore del visualizzatore. In altre parole, se l&#39;area di visualizzazione è uguale o maggiore delle dimensioni di un monitor desktop comune `.s7size_large` viene utilizzato; se l’area è di dimensioni simili a quelle di un comune dispositivo tablet `.s7size_medium` è assegnato. Per aree simili agli schermi dei cellulari. Il marcatore `.s7size_small` è impostato. Lo scopo principale di questi marcatori CSS è quello di creare layout di interfaccia utente diversi per schermi e dimensioni di visualizzatore diverse.

Il secondo gruppo di marcatori CSS include `.s7mouseinput` e `.s7touchinput`. Il marcatore `.s7touchinput` è impostato se il dispositivo corrente dispone di funzionalità di input tocco; in caso contrario, `.s7mouseinput` viene utilizzato. Questi marcatori sono destinati a creare elementi di input dell’interfaccia utente con dimensioni dello schermo diverse per tipi di input diversi, perché normalmente l’input tocco richiede elementi più grandi. Nel caso in cui il dispositivo sia dotato di funzionalità di input del mouse e di funzionalità touch, `.s7touchinput` e il visualizzatore esegue il rendering di un’interfaccia touch-screen.

Il seguente esempio di CSS imposta la dimensione del pulsante di zoom in su 28 x 28 pixel nei sistemi con input del mouse e su 56 x 56 pixel nei dispositivi touch. Inoltre, nasconde completamente il pulsante se le dimensioni del visualizzatore diventano troppo piccole:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7ecatalogsearchviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7ecatalogsearchviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Per eseguire il targeting di dispositivi con una densità di pixel diversa, utilizza le query multimediali CSS. Il seguente blocco di query multimediale contiene CSS specifico per gli schermi ad alta densità:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilizzo dei marcatori CSS è il modo più flessibile per creare CSS dinamici. Consente di eseguire il targeting non solo delle dimensioni dello schermo del dispositivo, ma anche delle dimensioni effettive del visualizzatore, utile per i layout di pagina dinamici.

Utilizza il file CSS del visualizzatore predefinito come esempio di approccio ai marcatori CSS.

**Query multimediali CSS**

Il rilevamento del dispositivo può essere eseguito anche utilizzando query multimediali CSS pure. Tutto ciò che è racchiuso all’interno di un determinato blocco di query multimediale viene applicato solo quando viene eseguito su un dispositivo corrispondente.

Quando viene applicato ai visualizzatori mobili, utilizza quattro query multimediali CSS, definite nel CSS nel seguente ordine:

1. Contiene solo regole specifiche per tutti i dispositivi touch.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. Contiene solo regole specifiche per i tablet con schermi ad alta risoluzione.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px) and (-webkit-min-device-pixel-ratio:1.5), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) and (-webkit-min-device-pixel-ratio:1.5)  
   { 
   }
   ```

1. Contiene solo regole specifiche per tutti i telefoni cellulari.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) 
   { 
   }
   ```

1. Contiene solo regole specifiche per i telefoni cellulari con schermi ad alta risoluzione.

   ```
   @media only screen and (max-device-width:9in) and (max-device-height:9in) and (-webkit-min-device-pixel-ratio: 1.5), 
     only screen and (device-width:720px) and (device-height:1280px) and (-webkit-device-pixel-ratio: 2), 
     only screen and (device-width:1280px) and (device-height:720px) and (-webkit-device-pixel-ratio: 2) 
   { 
   }
   ```

Utilizzando un approccio basato su query multimediali, è necessario organizzare i CSS con il rilevamento dei dispositivi come segue:

* Innanzitutto, la sezione specifica per il desktop definisce tutte le proprietà specifiche del desktop o comuni a tutti gli schermi.
* E, in secondo luogo, le quattro query multimediali vanno nell’ordine definito in precedenza e forniscono regole CSS specifiche per il tipo di dispositivo corrispondente.

Non è necessario duplicare l’intero CSS del visualizzatore in ogni query multimediale. Solo le proprietà specifiche di determinati dispositivi vengono ridefinite all&#39;interno di una query multimediale.

## Spunti CSS {#section-9d570f95eb2443aca74c1b02f6e89aff}

Molti elementi dell&#39;interfaccia utente del visualizzatore sono formattati utilizzando immagini bitmap e hanno più stati visivi distinti. Un buon esempio è un pulsante che normalmente ha almeno tre stati diversi: &quot;su&quot;, &quot;su&quot; e &quot;giù&quot;. A ogni stato deve essere assegnato un disegno bitmap specifico.

Con un approccio classico allo stile, il CSS avrebbe un riferimento separato a un singolo file di immagine sul server per ogni stato dell’elemento dell’interfaccia utente. Di seguito è riportato un esempio di CSS per la formattazione di un pulsante di zoom in:

```
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

Lo svantaggio di questo approccio è che l’utente finale riceve una risposta interattiva o ritardata dall’interfaccia quando l’elemento viene interagito per la prima volta. Questa azione si verifica perché il disegno dell&#39;immagine per il nuovo stato dell&#39;elemento non è ancora stato scaricato. Inoltre, questo approccio potrebbe avere un leggero impatto negativo sulle prestazioni a causa di un aumento del numero di chiamate HTTP al server.

Gli sprite CSS sono un approccio diverso in cui il disegno dell&#39;immagine per tutti gli stati degli elementi viene combinato in un unico file PNG chiamato &quot;sprite&quot;. Tale &quot;sprite&quot; ha tutti gli stati visivi per l&#39;elemento dato posizionati uno dopo l&#39;altro. Quando si applica uno stile a un elemento dell’interfaccia utente con sprite, si fa riferimento alla stessa immagine sprite per tutti i diversi stati nel CSS. Inoltre, il `background-position` viene utilizzata per ogni stato per specificare quale parte dell’immagine &quot;sprite&quot; viene utilizzata. È possibile strutturare un&#39;immagine &quot;sprite&quot; in qualsiasi modo appropriato. I visualizzatori di solito lo sovrappongono verticalmente. Di seguito è riportato un esempio basato su &quot;sprite&quot; di come formattare lo stesso pulsante di zoom in dall’alto:

```
.s7ecatalogsearchviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7ecatalogsearchviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Note generali sullo stile e consigli {#section-95855dccbbc444e79970f1aaa3260b7b}

* Quando si personalizza l’interfaccia utente del visualizzatore con i CSS, l’utilizzo di `!IMPORTANT` la regola non è supportata per gli elementi visualizzatore di stili. In particolare: `!IMPORTANT` La regola non deve essere utilizzata per sostituire gli stili predefiniti o di runtime forniti dal visualizzatore o dall’SDK del visualizzatore. Questo perché può influenzare il comportamento dei componenti appropriati. Per impostare le proprietà CSS documentate in questa guida di riferimento, è invece necessario utilizzare i selettori CSS con la specificità appropriata.
* Tutti i percorsi delle risorse esterne all’interno di CSS vengono risolti in base alla posizione CSS, non in base alla posizione della pagina del visualizzatore HTML. Tieni presente questa regola quando copi il CSS predefinito in una posizione diversa. Copia anche le risorse predefinite oppure aggiorna i percorsi all’interno del CSS personalizzato.
* Il formato preferito per la grafica bitmap è PNG.
* Il disegno bitmap viene assegnato agli elementi dell&#39;interfaccia utente mediante `background-image` proprietà.
* Il `width` e `height` Le proprietà di un elemento dell&#39;interfaccia utente ne definiscono la dimensione logica. Dimensione della bitmap passata a `background-image` non influisce sulla dimensione logica.
* Per utilizzare l&#39;elevata densità di pixel di schermi ad alta risoluzione come Retina, specificate un disegno bitmap di dimensioni doppie rispetto a quelle dell&#39;elemento dell&#39;interfaccia utente logico. Quindi, applica il `-webkit-background-size:contain` per ridurre lo sfondo alle dimensioni dell&#39;elemento dell&#39;interfaccia utente logica.
* Per rimuovere un pulsante dall’interfaccia utente, aggiungi `display:none` alla relativa classe CSS.
* Per il valore del colore supportato dagli stili CSS è possibile utilizzare vari formati. Se è necessaria la trasparenza, utilizzare il formato `rgba(R,G,B,A)`. In caso contrario, è possibile utilizzare il formato `#RRGGBB`.

## Elementi dell’interfaccia utente comune {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Di seguito è riportata la documentazione di riferimento sugli elementi dell’interfaccia utente applicabile al visualizzatore di ricerca eCatalog:

* [Pulsante Aggiungi preferito](r-html5-ecatsearch-customize-addfavorite.md)
* [Pulsante Chiudi](r-html5-ecatsearch-customize-closebutton.md)
* [Scarica](r-html5-ecatsearch-customize-download.md)
* [Condivisione e-mail](r-html5-ecatsearch-customize-emailshare.md)
* [Incorpora condivisione](r-html5-ecatsearch-customize-embedshare.md)
* [Condivisione facebook](r-html5-ecatsearch-customize-facebookshare.md)
* [Effetto Preferiti](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Menu Preferiti](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Visualizzazione Preferiti](r-html5-ecatsearch-customize-favoritesview.md)
* [Pulsante Prima pagina](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Evidenziazione focus](r-html5-ecatsearch-customize-focushighlight.md)
* [pulsante a schermo intero](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Effetto icona](r-html5-ecatsearch-customize-iconeffect.md)
* [Menu a comparsa del pannello Info](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Effetto mappa immagine](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Pulsante Pagina successiva grande](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Pulsante Pagina precedente grande](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Pulsante Ultima pagina](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Condivisione collegamento](r-html5-ecatsearch-customize-linkshare.md)
* [Barra di controllo principale](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Area visualizzatore principale](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Pulsante Pagina successiva](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Indicatore di pagina](r-html5-ecatsearch-customize-pageindicator.md)
* [Visualizzazione pagina](r-html5-ecatsearch-customize-pageview.md)
* [Pulsante Pagina precedente](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Stampa](r-html5-ecatsearch-customize-print.md)
* [Rimuovi pulsante Preferiti](r-html5-ecatsearch-customize-removefavorite.md)
* [Pulsante Cerca](r-html5-ecatsearch-customize-searchbutton.md)
* [Effetto di ricerca](r-html5-ecatsearch-customize-searcheffect.md)
* [Pannello Risultati ricerca](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Barra di controllo secondaria](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Condivisione social](r-html5-ecatsearch-customize-socialshare.md)
* [Sommario](r-html5-ecatsearch-customize-tableofcontents.md)
* [Miniature](r-html5-ecatsearch-customize-thumbnails.md)
* [Pulsante Miniature](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Descrizione](r-html5-ecatsearch-customize-tooltips.md)
* [Condivisione twitter](r-html5-ecatsearch-customize-twittershare.md)
* [Pulsante Visualizza tutti i preferiti](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Pulsante Zoom in](r-html5-ecatsearch-customize-zoominbutton.md)
* [Pulsante Zoom out](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Pulsante di ripristino zoom](r-html5-ecatsearch-customize-zoomresetbutton.md)
