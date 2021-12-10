---
title: Personalizzazione del visualizzatore di ricerca eCatalog
description: Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni del comportamento per il visualizzatore di ricerca eCatalog vengono effettuate creando un CSS personalizzato.
keywords: reattivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 32b55fb1-1408-4264-92fa-b3a73f31df1d
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '1396'
ht-degree: 0%

---

# Personalizzazione del visualizzatore di ricerca eCatalog{#customizing-ecatalog-search-viewer}

Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni del comportamento per il visualizzatore di ricerca eCatalog vengono effettuate creando un CSS personalizzato.

Il flusso di lavoro consigliato consiste nell’accettare il file CSS predefinito per il visualizzatore appropriato, copiarlo in un percorso diverso, personalizzarlo e specificare il percorso del file personalizzato nella `style=` comando.

I file CSS predefiniti si trovano nel seguente percorso:

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quella predefinita. Se una dichiarazione di classe viene omessa, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell’interfaccia utente.

Un modo alternativo per fornire regole CSS personalizzate è quello di utilizzare stili incorporati direttamente sulla pagina web o in una delle regole CSS esterne collegate.

Quando crei CSS personalizzati, ricorda che il visualizzatore assegna `.s7ecatalogsearchviewer` all&#39;elemento DOM contenitore. Se utilizzi un file CSS esterno passato con `style=` comando, utilizza `.s7ecatalogsearchviewer` Classe come classe padre nel selettore discendente per le regole CSS. Se stai utilizzando stili incorporati nella pagina web, devi anche qualificare questo selettore con un ID dell’elemento DOM del contenitore come segue:

`#<containerId>.s7ecatalogsearchviewer`

## Creazione di CSS reattivi {#section-c1e74f5114ad418884ca1c95f5ea5b63}

È possibile indirizzare diversi dispositivi e dimensioni di incorporamento in CSS per rendere diversa la visualizzazione del contenuto, a seconda del dispositivo di un utente o di un particolare layout di pagina web. Questo targeting include, ma non è limitato a, diversi layout di pagina web, dimensioni degli elementi dell&#39;interfaccia utente e risoluzione dell&#39;immagine.

Il visualizzatore supporta due metodi per creare CSS adattabili: Marcatori CSS e query multimediali CSS standard. È possibile utilizzare questi metodi in modo indipendente o insieme.

**Marcatori CSS**

Per creare CSS adattabili, il visualizzatore supporta gli indicatori CSS che assegnano in modo dinamico classi CSS speciali all’elemento contenitore di visualizzatori di livello superiore in base alle dimensioni del visualizzatore in fase di esecuzione e al tipo di input sul dispositivo corrente.

Il primo gruppo di marcatori CSS include `.s7size_large`, `.s7size_medium`e `.s7size_small` classi. Vengono applicati in base all’area di runtime del contenitore del visualizzatore. Se l&#39;area di visualizzazione è uguale o maggiore delle dimensioni di un monitor desktop comune `.s7size_large` è utilizzato; se l&#39;area è vicina alle dimensioni di un dispositivo tablet comune `.s7size_medium` è assegnato. Per aree simili agli schermi dei telefoni cellulari. Il marcatore `.s7size_small` è impostato. Lo scopo principale di questi marcatori CSS è quello di creare layout di interfaccia utente diversi per schermi e dimensioni di visualizzatore diversi.

Il secondo gruppo di Marcatori CSS include `.s7mouseinput` e `.s7touchinput`. Il marcatore `.s7touchinput` è impostato se il dispositivo corrente dispone di capacità di input touch; altrimenti, `.s7mouseinput` viene utilizzato. Questi marcatori sono destinati a creare elementi di input dell&#39;interfaccia utente con diverse dimensioni dello schermo per diversi tipi di input, perché normalmente l&#39;input touch richiede elementi più grandi. Nel caso in cui il dispositivo sia dotato di funzionalità di input del mouse e touch, `.s7touchinput` è impostato e il visualizzatore esegue il rendering di un’interfaccia utente touch.

Il seguente esempio CSS imposta le dimensioni del pulsante zoom in su 28 x 28 pixel sui sistemi con input del mouse e 56 x 56 pixel sui dispositivi touch. Inoltre, nasconde completamente il pulsante se la dimensione del visualizzatore diventa troppo piccola:

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

Per eseguire il targeting dei dispositivi con una densità di pixel diversa, utilizza le query multimediali CSS. Il seguente blocco di query per contenuti multimediali conterrebbe CSS specifici per le schermate ad alta densità:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilizzo dei marcatori CSS è il modo più flessibile per creare CSS adattabili. Consente di eseguire il targeting non solo delle dimensioni dello schermo del dispositivo, ma anche delle dimensioni effettive del visualizzatore, utile per i layout di pagina adattabili.

Utilizza il file CSS del visualizzatore predefinito come esempio di approccio a marcatori CSS.

**Query multimediali CSS**

Il rilevamento dei dispositivi può essere eseguito anche utilizzando semplici query multimediali CSS. Tutto ciò che è racchiuso in un determinato blocco di query multimediale viene applicato solo quando viene eseguito su un dispositivo corrispondente.

Quando vengono applicati ai visualizzatori mobili, utilizza quattro query multimediali CSS, definite nel CSS nel seguente ordine:

1. Contiene solo regole specifiche per tutti i dispositivi touch.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-width:799px), 
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in) and (max-device-height:799px) 
   { 
   }
   ```

1. Contiene solo regole specifiche per tablet con schermi ad alta risoluzione.

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

Utilizzando un approccio alle query multimediali, è necessario organizzare i CSS con rilevamento del dispositivo come segue:

* Innanzitutto, la sezione specifica per il desktop definisce tutte le proprietà specifiche per il desktop o comuni a tutte le schermate.
* In secondo luogo, le quattro query multimediali vanno nell&#39;ordine definito in precedenza e forniscono regole CSS specifiche per il tipo di dispositivo corrispondente.

Non è necessario duplicare l’intero CSS del visualizzatore in ogni query multimediale. Solo le proprietà specifiche per determinati dispositivi vengono ridefinite all&#39;interno di una query multimediale.

## Sprite CSS {#section-9d570f95eb2443aca74c1b02f6e89aff}

Molti elementi dell’interfaccia utente del visualizzatore sono formattati utilizzando immagini bitmap e hanno più di un diverso stato visivo. Un buon esempio è un pulsante che normalmente ha almeno tre stati diversi: &quot;su&quot;, &quot;sopra&quot; e &quot;giù&quot;. Ogni stato richiede l&#39;assegnazione di una propria immagine bitmap.

Con un approccio classico allo stile, il CSS avrebbe un riferimento separato al singolo file di immagine sul server per ogni stato dell’elemento dell’interfaccia utente. Di seguito è riportato un esempio di CSS per lo stile di un pulsante di zoom in:

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

L’inconveniente di questo approccio è che l’utente finale si trova in una situazione di sfarfallio o di ritardo nella risposta dell’interfaccia utente quando l’elemento viene interagito per la prima volta. Questa azione si verifica perché l’immagine per il nuovo stato elemento non è ancora stata scaricata. Inoltre, questo approccio può avere un leggero impatto negativo sulle prestazioni a causa di un aumento del numero di chiamate HTTP al server.

Gli spriti CSS è un approccio diverso in cui l’immagine per tutti gli stati degli elementi viene combinata in un singolo file PNG denominato &quot;sprite&quot;. Tale &quot;sprite&quot; ha tutti gli stati visivi per l&#39;elemento specificato posizionato uno dopo l&#39;altro. Quando si crea lo stile di un elemento dell’interfaccia utente con sprites, viene fatto riferimento alla stessa immagine sprite per tutti gli stati diversi del CSS. Inoltre, il `background-position` viene utilizzata per ogni stato per specificare quale parte dell&#39;immagine &quot;sprite&quot; viene utilizzata. È possibile strutturare un&#39;immagine &quot;sprite&quot; in qualsiasi modo appropriato. In genere, i visualizzatori lo dispongono di una sovrapposizione verticale. Di seguito è riportato un esempio basato su &quot;sprite&quot; di stile dello stesso pulsante di zoom in dall’alto:

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

* Quando si personalizza l’interfaccia utente del visualizzatore con CSS, l’utilizzo di `!IMPORTANT` La regola non è supportata per gli elementi del visualizzatore di stili. In particolare, `!IMPORTANT` Questa regola non deve essere utilizzata per sostituire uno stile predefinito o di esecuzione fornito dal visualizzatore o dall’SDK del visualizzatore. Il motivo è che può influenzare il comportamento dei componenti appropriati. Invece, utilizza i selettori CSS con la specificità appropriata per impostare le proprietà CSS documentate in questa guida di riferimento.
* Tutti i percorsi delle risorse esterne all’interno dei CSS vengono risolti rispetto alla posizione CSS, non alla posizione della pagina HTML del visualizzatore. Tieni presente questa regola quando copi il CSS predefinito in una posizione diversa. Puoi copiare anche le risorse predefinite o aggiornare i percorsi all’interno del CSS personalizzato.
* Il formato preferito per le immagini bitmap è PNG.
* L’immagine bitmap viene assegnata agli elementi dell’interfaccia utente tramite `background-image` proprietà.
* La `width` e `height` le proprietà di un elemento dell’interfaccia utente ne definiscono la dimensione logica. Dimensione della bitmap passata a `background-image` non influisce sulle dimensioni logiche.
* Per utilizzare l&#39;alta densità di pixel di schermi ad alta risoluzione come Retina, specificare immagini bitmap due volte più grandi della dimensione dell&#39;elemento dell&#39;interfaccia utente logica. Quindi, applica il `-webkit-background-size:contain` per ridimensionare lo sfondo fino alle dimensioni dell&#39;elemento dell&#39;interfaccia utente logica.
* Per rimuovere un pulsante dall’interfaccia utente, aggiungi `display:none` alla relativa classe CSS.
* È possibile utilizzare vari formati per il valore del colore supportato da CSS. Se hai bisogno di trasparenza, utilizza il formato `rgba(R,G,B,A)`. In caso contrario, è possibile utilizzare il formato `#RRGGBB`.

## Elementi comuni dell&#39;interfaccia utente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Di seguito è riportata la documentazione di riferimento relativa agli elementi dell’interfaccia utente applicabili al visualizzatore di ricerca eCatalog:

* [Pulsante Aggiungi preferito](r-html5-ecatsearch-customize-addfavorite.md)
* [Pulsante Chiudi](r-html5-ecatsearch-customize-closebutton.md)
* [Scarica](r-html5-ecatsearch-customize-download.md)
* [Condivisione e-mail](r-html5-ecatsearch-customize-emailshare.md)
* [Quota di incorporamento](r-html5-ecatsearch-customize-embedshare.md)
* [Condivisione facebook](r-html5-ecatsearch-customize-facebookshare.md)
* [Effetto Preferiti](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Menu Preferiti](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Vista Preferiti](r-html5-ecatsearch-customize-favoritesview.md)
* [Pulsante Prima pagina](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Evidenziazione](r-html5-ecatsearch-customize-focushighlight.md)
* [Pulsante Schermo intero](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Icona, effetto](r-html5-ecatsearch-customize-iconeffect.md)
* [Popup pannello informazioni](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Effetto mappa immagine](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Pulsante Pagina successiva grande](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Pulsante Pagina precedente grande](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Pulsante Ultima pagina](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Condivisione collegamenti](r-html5-ecatsearch-customize-linkshare.md)
* [Barra di controllo principale](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Area visualizzatore principale](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Pulsante Pagina successiva](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Indicatore di pagina](r-html5-ecatsearch-customize-pageindicator.md)
* [Vista a pagina](r-html5-ecatsearch-customize-pageview.md)
* [Pulsante Pagina precedente](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Stampa](r-html5-ecatsearch-customize-print.md)
* [Pulsante Rimuovi preferito](r-html5-ecatsearch-customize-removefavorite.md)
* [Pulsante Ricerca](r-html5-ecatsearch-customize-searchbutton.md)
* [Effetto Ricerca](r-html5-ecatsearch-customize-searcheffect.md)
* [Pannello dei risultati di ricerca](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Barra di controllo secondaria](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Quota sociale](r-html5-ecatsearch-customize-socialshare.md)
* [Sommario](r-html5-ecatsearch-customize-tableofcontents.md)
* [Miniature](r-html5-ecatsearch-customize-thumbnails.md)
* [Pulsante Miniature](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Descrizioni comandi](r-html5-ecatsearch-customize-tooltips.md)
* [Condivisione twitter](r-html5-ecatsearch-customize-twittershare.md)
* [Pulsante Visualizza tutti i Preferiti](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Pulsante Zoom in](r-html5-ecatsearch-customize-zoominbutton.md)
* [Pulsante Zoom out](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Pulsante Ripristina zoom](r-html5-ecatsearch-customize-zoomresetbutton.md)
