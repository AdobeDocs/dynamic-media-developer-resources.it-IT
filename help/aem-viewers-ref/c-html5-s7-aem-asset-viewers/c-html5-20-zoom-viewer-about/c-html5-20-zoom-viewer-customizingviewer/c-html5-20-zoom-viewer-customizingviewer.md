---
description: La personalizzazione visiva e la maggior parte delle personalizzazioni del comportamento per il visualizzatore zoom vengono effettuate mediante la creazione di un CSS personalizzato.
keywords: responsive
seo-description: La personalizzazione visiva e la maggior parte delle personalizzazioni del comportamento per il visualizzatore zoom vengono effettuate mediante la creazione di un CSS personalizzato.
seo-title: Personalizzazione del visualizzatore zoom
solution: Experience Manager
title: Personalizzazione del visualizzatore zoom
topic: Dynamic Media
uuid: 7ecbc4cc-b5c0-4f4a-b747-03c484de6851
translation-type: tm+mt
source-git-commit: e4695cc4e882351ec3f2c55fd8a3cfca455bd79d
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 0%

---


# Personalizzazione del visualizzatore zoom{#customizing-zoom-viewer}

La personalizzazione visiva e la maggior parte delle personalizzazioni del comportamento per il visualizzatore zoom vengono effettuate mediante la creazione di un CSS personalizzato.

Il flusso di lavoro consigliato consiste nell&#39;acquisire il file CSS predefinito per il visualizzatore appropriato, copiarlo in un percorso diverso, personalizzarlo e specificare il percorso del file personalizzato nel comando `style=`.

I file CSS predefiniti si trovano nella posizione seguente:

`<s7_viewers_root>/html5/ZoomViewer_light.css`

Il visualizzatore viene fornito con due file CSS integrati, per schemi di colore &quot;chiari&quot; e &quot;scuri&quot;. La versione &quot;light&quot; viene utilizzata per impostazione predefinita, ma potete passare alla versione &quot;dark&quot; utilizzando il seguente CSS standard:

`<s7_viewers_root>/html5/ZoomViewer_dark.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quella predefinita. Se viene omessa una dichiarazione di classe, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell&#39;interfaccia utente.

In alternativa, per fornire regole CSS personalizzate potete utilizzare gli stili incorporati direttamente sulla pagina Web o in una delle regole CSS esterne collegate.

Quando create CSS personalizzato, tenete presente che il visualizzatore assegna la classe `.s7zoomviewer` al relativo elemento DOM contenitore. Se utilizzate un file CSS esterno passato con il comando `style=`, utilizzate la classe `.s7zoomviewer` come classe principale nel selettore discendente per le regole CSS. Se state utilizzando stili incorporati nella pagina Web, qualificate anche questo selettore con un ID dell&#39;elemento DOM contenitore come segue:

`#<containerId>.s7zoomviewer`

## Creazione di CSS reattivo {#section-0bb49aca42d242d9b01879d5ba59d33b}

È possibile impostare come destinazione dispositivi e dimensioni di incorporazione diverse nei CSS per consentire la visualizzazione dei contenuti in modo diverso a seconda del dispositivo dell&#39;utente o di un particolare layout di pagina Web. Ciò include, ma non è limitato a, layout diversi, dimensioni degli elementi dell&#39;interfaccia utente e risoluzione dell&#39;immagine.

Il visualizzatore supporta due metodi per creare CSS reattivo: Marcatori CSS e query multimediali CSS standard. Potete utilizzarli in modo indipendente o insieme.

**Marcatori CSS**

Per facilitare la creazione di CSS reattivi, il visualizzatore supporta i marcatori CSS. Si tratta di classi CSS speciali che vengono assegnate dinamicamente all&#39;elemento contenitore del visualizzatore di livello principale in base alle dimensioni del visualizzatore in fase di esecuzione e al tipo di input utilizzato sul dispositivo corrente.

Il primo gruppo di marcatori CSS include le classi `.s7size_large`, `.s7size_medium` e `.s7size_small`. Vengono applicate in base all’area di runtime del contenitore del visualizzatore. Se l&#39;area del visualizzatore è uguale o maggiore delle dimensioni di un monitor desktop comune, viene utilizzato `.s7size_large`; se l&#39;area è vicina a un dispositivo tablet comune, viene assegnato `.s7size_medium`. Per le aree simili agli schermi dei telefoni cellulari, viene impostato `.s7size_small`. Lo scopo principale di questi marcatori CSS è quello di creare layout di interfaccia utente diversi per schermi e dimensioni di visualizzatore diversi.

Il secondo gruppo di marcatori CSS contiene `.s7mouseinput` e `.s7touchinput`. `.s7touchinput` è impostato se il dispositivo corrente dispone di capacità di input touch; altrimenti  `.s7mouseinput` viene utilizzato. Questi marcatori sono destinati principalmente alla creazione di elementi di input dell&#39;interfaccia utente con diverse dimensioni di schermo per diversi tipi di input, perché normalmente l&#39;input tocco richiede elementi più grandi. Se il dispositivo è dotato sia di ingresso del mouse che di capacità touch, viene impostato `.s7touchinput` e il visualizzatore esegue il rendering di un&#39;interfaccia utente touch.

Il seguente file CSS di esempio imposta la dimensione del pulsante di zoom su 28x28 pixel nei sistemi con input del mouse e su 56x56 pixel nei dispositivi touch. Inoltre, nasconde completamente il pulsante se le dimensioni del visualizzatore sono molto ridotte:

```
.s7zoomviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7zoomviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7zoomviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Per i dispositivi con densità di pixel diversa è necessario utilizzare le media query CSS. Il seguente blocco di query per file multimediali contiene CSS specifico per le schermate ad alta densità:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L&#39;utilizzo dei marcatori CSS è il modo più flessibile per creare CSS reattivo, in quanto consente di impostare come destinazione non solo la dimensione dello schermo del dispositivo, ma anche la dimensione effettiva del visualizzatore, il che è utile per i layout di progettazione reattivi.

Potete usare il file CSS del visualizzatore predefinito come esempio di approccio per i marcatori CSS.

**Query multimediali CSS**

Potete anche eseguire il rilevamento dei dispositivi utilizzando semplici query multimediali CSS. Tutto ciò che si trova all&#39;interno di un determinato blocco di query multimediale viene applicato solo quando viene eseguito su un dispositivo corrispondente.

Quando applicate ai visualizzatori per dispositivi mobili, usate quattro query multimediali CSS, definite nel CSS, nell’ordine elencato di seguito:

1. Contiene solo regole specifiche per tutti i dispositivi touch.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
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

## Sprite CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Molti elementi dell’interfaccia utente del visualizzatore sono formattati utilizzando immagini bitmap e hanno più di un diverso stato visivo. Un buon esempio è un pulsante che normalmente ha almeno 3 stati diversi: &quot;su&quot;, &quot;sopra&quot; e &quot;giù&quot;. A ogni stato è assegnata una propria immagine bitmap.

Con un approccio classico allo stile, il CSS avrebbe un riferimento separato al singolo file di immagine sul server per ogni stato dell&#39;elemento dell&#39;interfaccia utente. Di seguito è riportato un esempio di CSS per lo stile del pulsante di zoom in:

```
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

Lo svantaggio di questo approccio è che l&#39;utente finale si trova in una situazione di sfarfallio o ritardo nella risposta dell&#39;interfaccia utente quando l&#39;elemento viene interagito per la prima volta. Questa azione si verifica perché la grafica dell&#39;immagine per il nuovo stato dell&#39;elemento non è ancora stata scaricata. Inoltre, questo approccio potrebbe avere un lieve impatto negativo sulle prestazioni a causa di un aumento del numero di chiamate HTTP al server.

Gli spriti CSS sono un approccio diverso in cui la grafica immagine per tutti gli stati degli elementi viene combinata in un singolo file PNG denominato &quot;sprite&quot;. Tale &quot;sprite&quot; contiene tutti gli stati visivi per l&#39;elemento specificato posizionato uno dopo l&#39;altro. Quando si formatta un elemento dell&#39;interfaccia utente con sprite, viene fatto riferimento alla stessa immagine sprite per tutti gli stati diversi del CSS. Inoltre, la proprietà `background-position` viene utilizzata per ogni stato per specificare quale parte dell&#39;immagine &quot;sprite&quot; viene utilizzata. Potete strutturare un&#39;immagine &quot;sprite&quot; in qualsiasi modo appropriato. In genere, i visualizzatori possono sovrapporsi verticalmente. Di seguito è riportato un esempio &quot;sprite&quot; in cui viene formattato lo stesso pulsante di zoom in dall’alto:

```
.s7zoomviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7zoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
background-position: -0px -560px;  
}
```

## Note generali sullo stile e consigli {#section-95855dccbbc444e79970f1aaa3260b7b}

* Quando personalizzate l&#39;interfaccia utente del visualizzatore con CSS, l&#39;utilizzo della regola `!IMPORTANT` non è supportato per gli elementi del visualizzatore di stile. In particolare, la regola `!IMPORTANT` non deve essere utilizzata per ignorare lo stile predefinito o runtime fornito dall&#39;SDK del visualizzatore o del visualizzatore. Il motivo è che potrebbe influenzare il comportamento dei componenti appropriati. Al contrario, utilizzate i selettori CSS con la specificità appropriata per impostare le proprietà CSS documentate in questa guida di riferimento.
* Tutti i percorsi delle risorse esterne all&#39;interno di CSS vengono risolti rispetto al percorso CSS, non al percorso della pagina HTML del visualizzatore. Tenete presente questa regola quando copiate il CSS predefinito in un percorso diverso. Potete copiare anche le risorse predefinite oppure aggiornare i percorsi all&#39;interno del CSS personalizzato.
* Il formato preferito per le immagini bitmap è il formato PNG.
* La grafica bitmap viene assegnata agli elementi dell&#39;interfaccia utente tramite la proprietà `background-image`.
* Le proprietà `width` e `height` di un elemento dell&#39;interfaccia utente ne definiscono la dimensione logica. Le dimensioni dell&#39;elemento bitmap passato a `background-image` non influiscono sulle dimensioni logiche.
* Per utilizzare l&#39;alta densità di pixel di schermi ad alta risoluzione come Retina, specificate immagini bitmap il doppio delle dimensioni dell&#39;elemento logico dell&#39;interfaccia utente. Quindi, applicate la proprietà `-webkit-background-size:contain` per ridimensionare lo sfondo fino alla dimensione logica dell&#39;elemento dell&#39;interfaccia utente.
* Per rimuovere un pulsante dall&#39;interfaccia utente, aggiungete `display:none` alla relativa classe CSS.
* Potete usare vari formati per il valore del colore supportato da CSS. Se è necessaria la trasparenza, utilizzate il formato `rgba(R,G,B,A)`. In caso contrario, è possibile utilizzare il formato `#RRGGBB`.

## Elementi comuni dell&#39;interfaccia utente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Di seguito è riportata la documentazione di riferimento degli elementi dell’interfaccia utente applicata al visualizzatore video:
