---
description: La personalizzazione visiva e la maggior parte delle personalizzazioni comportamentali per il visualizzatore di ricerca per eCatalog vengono effettuate mediante la creazione di un CSS personalizzato.
keywords: responsive
seo-description: La personalizzazione visiva e la maggior parte delle personalizzazioni comportamentali per il visualizzatore di ricerca per eCatalog vengono effettuate mediante la creazione di un CSS personalizzato.
seo-title: Personalizzazione del visualizzatore di ricerca per eCatalog
solution: Experience Manager
title: Personalizzazione del visualizzatore di ricerca per eCatalog
topic: Dynamic media
uuid: a715399b-7b02-4656-8257-4c390c6f629c
translation-type: tm+mt
source-git-commit: 8d7fdab78c5d23d0e541effa9b9c470921bd144b

---


# Personalizzazione del visualizzatore di ricerca per eCatalog{#customizing-ecatalog-search-viewer}

La personalizzazione visiva e la maggior parte delle personalizzazioni comportamentali per il visualizzatore di ricerca per eCatalog vengono effettuate mediante la creazione di un CSS personalizzato.

Il flusso di lavoro consigliato consiste nell&#39;acquisire il file CSS predefinito per il visualizzatore appropriato, copiarlo in un percorso diverso, personalizzarlo e specificare la posizione del file personalizzato nel `style=` comando.

I file CSS predefiniti si trovano nella posizione seguente:

`<s7_viewers_root>/html5/eCatalogSearchViewer_dark.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quella predefinita. Se viene omessa una dichiarazione di classe, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell&#39;interfaccia utente.

Un modo alternativo per fornire regole CSS personalizzate consiste nell&#39;utilizzare gli stili incorporati direttamente sulla pagina Web o in una delle regole CSS esterne collegate.

Quando create CSS personalizzato, tenete presente che il visualizzatore assegna la `.s7ecatalogsearchviewer` classe al relativo elemento DOM contenitore. Se utilizzate un file CSS esterno passato con il `style=` comando, utilizzate la `.s7ecatalogsearchviewer` classe come classe principale nel selettore discendente per le regole CSS. Se state utilizzando stili incorporati nella pagina Web, qualificate anche questo selettore con un ID dell&#39;elemento DOM contenitore come segue:

`#<containerId>.s7ecatalogsearchviewer`

## Creazione di CSS reattivi {#section-c1e74f5114ad418884ca1c95f5ea5b63}

È possibile impostare come destinazione dispositivi e dimensioni di incorporazione diverse nei CSS per rendere diversa la visualizzazione dei contenuti, a seconda del dispositivo dell&#39;utente o di un particolare layout di pagina Web. Ciò include, ma non è limitato a, diversi layout di pagina Web, dimensioni degli elementi dell&#39;interfaccia utente e risoluzione dell&#39;immagine.

Il visualizzatore supporta due metodi per creare CSS reattivo: Marcatori CSS e query multimediali CSS standard. È possibile utilizzare questi metodi in modo indipendente o insieme.

**Marcatori CSS**

Per facilitare la creazione di CSS reattivi, il visualizzatore supporta i marcatori CSS che assegnano classi CSS speciali all&#39;elemento contenitore del visualizzatore di livello principale in modo dinamico, in base alle dimensioni del visualizzatore in fase di esecuzione e al tipo di input utilizzato sul dispositivo corrente.

Il primo gruppo di marcatori CSS include `.s7size_large`, `.s7size_medium`e `.s7size_small` classi. Vengono applicate in base all&#39;area di runtime del contenitore del visualizzatore. ossia se l’area del visualizzatore è uguale o maggiore delle dimensioni di un monitor desktop comune `.s7size_large` viene utilizzata; se l&#39;area ha dimensioni simili a quelle di un dispositivo tablet comune `.s7size_medium` è assegnata. Per aree simili agli schermi dei telefoni cellulari `.s7size_small` è impostato. Lo scopo principale di questi marcatori CSS è quello di creare layout di interfaccia utente diversi per schermi e dimensioni di visualizzatore diversi.

Il secondo gruppo di marcatori CSS include `.s7mouseinput` e `.s7touchinput`. `.s7touchinput` è impostato se il dispositivo corrente dispone di capacità di input touch; altrimenti `.s7mouseinput` viene utilizzato. Questi marcatori sono progettati per creare elementi di input dell&#39;interfaccia utente con diverse dimensioni di schermo per diversi tipi di input, perché normalmente l&#39;input touch richiede elementi più grandi. Nel caso in cui il dispositivo disponga sia di ingresso del mouse che di funzioni touch, `.s7touchinput` viene impostato e il visualizzatore riproduce un’interfaccia utente touch.

Il seguente CSS di esempio imposta la dimensione del pulsante di zoom su 28x28 pixel nei sistemi con input del mouse e su dispositivi touch da 56x56 pixel. Inoltre, nasconde completamente il pulsante se le dimensioni del visualizzatore diventano davvero ridotte:

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

Per i dispositivi con una densità di pixel diversa, utilizzate le media query CSS. Il seguente blocco di query per contenuti multimediali contiene CSS specifico per le schermate ad alta densità:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L&#39;utilizzo dei marcatori CSS è il modo più flessibile per creare CSS reattivo, in quanto consente di impostare come destinazione non solo la dimensione dello schermo del dispositivo, ma anche la dimensione effettiva del visualizzatore, il che potrebbe essere utile per i layout di pagina reattivi.

Usate il file CSS del visualizzatore predefinito come esempio di approccio basato su marcatori CSS.

**Query multimediali CSS**

Il rilevamento dei dispositivi può essere effettuato anche utilizzando semplici query multimediali CSS. Tutto ciò che si trova all&#39;interno di un determinato blocco di query multimediale viene applicato solo quando viene eseguito su un dispositivo corrispondente.

Quando applicate ai visualizzatori per dispositivi mobili, usate quattro query multimediali CSS, definite nel CSS nel seguente ordine:

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

Con l’approccio delle media query, potete organizzare i CSS con il rilevamento del dispositivo nel modo seguente:

* Innanzitutto, la sezione specifica per il desktop definisce tutte le proprietà specifiche per il desktop o comuni a tutte le schermate.
* In secondo luogo, le quattro query multimediali vanno nell&#39;ordine definito sopra e forniscono regole CSS specifiche per il tipo di dispositivo corrispondente.

Non è necessario duplicare l’intero CSS del visualizzatore in ciascuna query multimediale. Solo le proprietà specifiche per determinati dispositivi vengono ridefinite all&#39;interno di una query multimediale.

## Sprite CSS {#section-9d570f95eb2443aca74c1b02f6e89aff}

Molti elementi dell’interfaccia utente del visualizzatore sono formattati utilizzando immagini bitmap e hanno più di un diverso stato visivo. Un buon esempio è rappresentato da un pulsante con almeno tre stati diversi: &quot;su&quot;, &quot;sopra&quot; e &quot;giù&quot;. A ogni stato è assegnata una propria immagine bitmap.

Con un approccio classico allo stile, il CSS avrebbe un riferimento separato al singolo file di immagine sul server per ogni stato dell&#39;elemento dell&#39;interfaccia utente. Di seguito è riportato un esempio di CSS per lo stile di un pulsante di zoom in:

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

Lo svantaggio di questo approccio è che l&#39;utente finale si trova in una situazione di sfarfallio o ritardo nella risposta dell&#39;interfaccia utente quando l&#39;elemento viene interagito per la prima volta. Questa azione si verifica perché la grafica dell&#39;immagine per il nuovo stato dell&#39;elemento non è ancora stata scaricata. Inoltre, questo approccio potrebbe avere un lieve impatto negativo sulle prestazioni a causa di un aumento del numero di chiamate HTTP al server.

Gli spriti CSS sono un approccio diverso in cui la grafica immagine per tutti gli stati degli elementi viene combinata in un singolo file PNG denominato &quot;sprite&quot;. Tale &quot;sprite&quot; contiene tutti gli stati visivi per l&#39;elemento specificato posizionato uno dopo l&#39;altro. Quando si formatta un elemento dell&#39;interfaccia utente con sprite, viene fatto riferimento alla stessa immagine sprite per tutti gli stati diversi del CSS. Inoltre, la `background-position` proprietà viene utilizzata per ogni stato per specificare quale parte dell&#39;immagine &quot;sprite&quot; viene utilizzata. Potete strutturare un&#39;immagine &quot;sprite&quot; in qualsiasi modo appropriato. In genere, i visualizzatori possono sovrapporsi verticalmente. Di seguito è riportato un esempio &quot;sprite&quot; in cui viene formattato lo stesso pulsante di zoom in dall’alto:

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

## Note generali di stile e consigli {#section-95855dccbbc444e79970f1aaa3260b7b}

* Quando personalizzate l&#39;interfaccia utente del visualizzatore con CSS, l&#39;uso della `!IMPORTANT` regola non è supportato per gli elementi del visualizzatore di stile. In particolare, `!IMPORTANT` la regola non deve essere utilizzata per ignorare eventuali stili predefiniti o runtime forniti dall’SDK del visualizzatore o del visualizzatore. Il motivo è che potrebbe influenzare il comportamento dei componenti appropriati. Al contrario, utilizzate i selettori CSS con la specificità appropriata per impostare le proprietà CSS documentate in questa guida di riferimento.
* Tutti i percorsi delle risorse esterne all&#39;interno di CSS vengono risolti rispetto al percorso CSS, non al percorso della pagina HTML del visualizzatore. Tenete presente questa regola quando copiate il CSS predefinito in un percorso diverso. Potete copiare anche le risorse predefinite oppure aggiornare i percorsi all&#39;interno del CSS personalizzato.
* Il formato preferito per la grafica bitmap è PNG.
* La grafica bitmap viene assegnata agli elementi dell&#39;interfaccia utente tramite la `background-image` proprietà .
* Le dimensioni logiche `width` e `height` le proprietà di un elemento dell&#39;interfaccia utente sono definite. Le dimensioni dell&#39;elemento bitmap passato non `background-image` influiscono sulle dimensioni logiche.
* Per utilizzare l&#39;alta densità di pixel di schermi ad alta risoluzione come Retina, specificate immagini bitmap il doppio delle dimensioni dell&#39;elemento logico dell&#39;interfaccia utente. Quindi, applicate la `-webkit-background-size:contain` proprietà per ridimensionare lo sfondo fino alla dimensione logica dell&#39;elemento dell&#39;interfaccia utente.
* Per rimuovere un pulsante dall&#39;interfaccia utente, aggiungete `display:none` alla classe CSS corrispondente.
* Potete usare vari formati per il valore del colore supportato da CSS. Se avete bisogno di trasparenza, usate il formato `rgba(R,G,B,A)`. In caso contrario, è possibile utilizzare il formato `#RRGGBB`.

## Elementi comuni dell&#39;interfaccia utente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Di seguito è riportata la documentazione di riferimento degli elementi dell’interfaccia utente applicata al visualizzatore di ricerca per eCatalog:

* [Pulsante Aggiungi preferito](r-html5-ecatsearch-customize-addfavorite.md)
* [Pulsante Chiudi](r-html5-ecatsearch-customize-closebutton.md)
* [Scarica](r-html5-ecatsearch-customize-download.md)
* [Condivisione e-mail](r-html5-ecatsearch-customize-emailshare.md)
* [Incorpora condivisione](r-html5-ecatsearch-customize-embedshare.md)
* [Condivisione Facebook](r-html5-ecatsearch-customize-facebookshare.md)
* [Effetto Preferiti](r-html5-ecatsearch-customize-favoriteseffect.md)
* [Menu Preferiti](r-html5-ecatsearch-customize-favoritesmenu.md)
* [Visualizzazione Preferiti](r-html5-ecatsearch-customize-favoritesview.md)
* [Pulsante Prima pagina](r-html5-ecatsearch-customize-firstpagebutton.md)
* [Evidenziazione dello stato](r-html5-ecatsearch-customize-focushighlight.md)
* [Pulsante Schermo intero](r-html5-ecatsearch-customize-fullscreenbutton.md)
* [Effetto Icona](r-html5-ecatsearch-customize-iconeffect.md)
* [Finestra a comparsa del pannello Info](r-html5-ecatsearch-customize-infopanelpopup.md)
* [Effetto mappa immagine](r-html5-ecatsearch-customize-imagemapeffect.md)
* [Pulsante Pagina successiva grande](r-html5-ecatsearch-customize-largenextpagebutton.md)
* [Pulsante Pagina precedente grande](r-html5-ecatsearch-customize-largepreviouspagebutton.md)
* [Pulsante Ultima pagina](r-html5-ecatsearch-customize-lastpagebutton.md)
* [Condivisione collegamenti](r-html5-ecatsearch-customize-linkshare.md)
* [Barra di controllo principale](r-html5-ecatsearch-customize-maincontrolbar.md)
* [Area visualizzatore principale](r-html5-ecatsearch-customize-mainviewerarea.md)
* [Pulsante Pagina successiva](r-html5-ecatsearch-customize-nextpagebutton.md)
* [Indicatore pagina](r-html5-ecatsearch-customize-pageindicator.md)
* [Visualizzazione pagina](r-html5-ecatsearch-customize-pageview.md)
* [Pulsante Pagina precedente](r-html5-ecatsearch-customize-previouspagebutton.md)
* [Stampa](r-html5-ecatalog-viewer-20-customize-print.md)
* [Pulsante Rimuovi preferito](r-html5-ecatsearch-customize-removefavorite.md)
* [Pulsante Ricerca](r-html5-ecatsearch-customize-searchbutton.md)
* [Effetto Ricerca](r-html5-ecatsearch-customize-searcheffect.md)
* [Pannello Risultati ricerca](r-html5-ecatsearch-customize-searchresultspanel.md)
* [Barra di controllo secondaria](r-html5-ecatsearch-customize-secondarycontrolbar.md)
* [Condivisione social network](r-html5-ecatsearch-customize-socialshare.md)
* [Sommario](r-html5-ecatsearch-customize-tableofcontents.md)
* [Miniature](r-html5-ecatsearch-customize-thumbnails.md)
* [Pulsante Miniature](r-html5-ecatsearch-customize-thumbnailsbutton.md)
* [Descrizioni comandi](r-html5-ecatsearch-customize-tooltips.md)
* [Condivisione Twitter](r-html5-ecatsearch-customize-twittershare.md)
* [Pulsante Visualizza tutti i preferiti](r-html5-ecatsearch-customize-viewallfavorites.md)
* [Pulsante Zoom in](r-html5-ecatsearch-customize-zoominbutton.md)
* [Pulsante Zoom out](r-html5-ecatsearch-customize-zoomoutbutton.md)
* [Pulsante di ripristino dello zoom](r-html5-ecatsearch-customize-zoomresetbutton.md)

