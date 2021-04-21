---
description: Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni del comportamento per il Visualizzatore video interattivo vengono effettuate creando un CSS personalizzato.
keywords: reattivo
solution: Experience Manager
title: Personalizzazione del visualizzatore video interattivo
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,Business Practitioner
exl-id: c428c3e6-81be-4708-b064-f9d794183209
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '1399'
ht-degree: 0%

---

# Personalizzazione del visualizzatore video interattivo{#customizing-interactive-video-viewer}

Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni del comportamento per il Visualizzatore video interattivo vengono effettuate creando un CSS personalizzato.

Il flusso di lavoro consigliato consiste nell’inserire il file CSS predefinito per il visualizzatore appropriato, copiarlo in un percorso diverso, personalizzarlo e specificare il percorso del file personalizzato nel comando `style=` .

I file CSS predefiniti si trovano nel seguente percorso:

`<s7_viewers_root>/html5/InteractiveVideoViewer_dark.css`

Il visualizzatore viene fornito con due file CSS preconfigurati, per schemi di colore &quot;chiari&quot; e &quot;scuri&quot;. La versione &quot;scura&quot; viene utilizzata per impostazione predefinita, ma è facile passare alla versione &quot;chiara&quot; utilizzando il seguente CSS standard:

`<s7_viewers_root>/html5/InteractiveVideoViewer_light.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quella predefinita. Se una dichiarazione di classe viene omessa, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell’interfaccia utente.

Un modo alternativo per fornire regole CSS personalizzate è quello di utilizzare stili incorporati direttamente sulla pagina web o in una delle regole CSS esterne collegate.

Quando crei CSS personalizzati, ricorda che il visualizzatore assegna la classe `.s7interactivevideoviewer` al suo elemento DOM contenitore. Se utilizzi un file CSS esterno passato con il comando `style=`, utilizza la classe `.s7interactivevideoviewer` come classe principale nel selettore discendente per le regole CSS. Se stai utilizzando stili incorporati nella pagina web, qualifica inoltre questo selettore con un ID dell’elemento DOM del contenitore come segue:

`#<containerId>.s7interactivevideoviewer`

## Creazione di CSS adattabili {#section-0bb49aca42d242d9b01879d5ba59d33b}

È possibile indirizzare diversi dispositivi e dimensioni di incorporamento in CSS per rendere la visualizzazione del contenuto diversa a seconda del dispositivo di un utente o di un particolare layout di pagina web. Sono inclusi, ma senza limitazioni, layout diversi, dimensioni degli elementi dell’interfaccia utente e risoluzione delle immagini.

Il visualizzatore supporta due meccanismi per creare CSS adattabili: Marcatori CSS e query multimediali CSS standard. Puoi utilizzarli in modo indipendente o insieme.

**Marcatori CSS**

Per facilitare la creazione di CSS adattabili, il visualizzatore supporta i marcatori CSS. Si tratta di classi CSS speciali che vengono assegnate dinamicamente all’elemento contenitore del visualizzatore di livello principale in base alle dimensioni del visualizzatore in fase di esecuzione e al tipo di input utilizzato sul dispositivo corrente.

Il primo gruppo di marcatori CSS include le classi `.s7size_large`, `.s7size_medium` e `.s7size_small`. Vengono applicati in base all’area in fase di esecuzione del contenitore del visualizzatore. Se l&#39;area del visualizzatore è uguale o maggiore delle dimensioni di un monitor desktop comune, viene utilizzato `.s7size_large`; se l&#39;area è vicina a un dispositivo tablet comune, viene assegnato `.s7size_medium` . Per le aree simili agli schermi dei telefoni cellulari, viene impostato `.s7size_small`. Lo scopo principale di questi marcatori CSS è quello di creare layout di interfaccia utente diversi per schermi e dimensioni di visualizzatore diversi.

Il secondo gruppo di Marcatori CSS contiene `.s7mouseinput` e `.s7touchinput`. `.s7touchinput` è impostato se il dispositivo corrente dispone di capacità di input touch; in caso contrario,  `.s7mouseinput` viene utilizzato. Questi marker sono destinati principalmente a creare elementi di input dell&#39;interfaccia utente con diverse dimensioni dello schermo per diversi tipi di ingresso, perché normalmente l&#39;input touch richiede elementi più grandi.

Il terzo gruppo di Marcatori CSS contiene `.s7device_landscape` e `.s7device_portrait`. `.s7device_landscape` è impostato se il dispositivo touch è orientato in orizzontale;  `.s7device_portrait` viene utilizzato quando il dispositivo touch viene ruotato per l’orientamento verticale. Questi marcatori CSS sono destinati all’utilizzo solo su sistemi desktop.

Il seguente esempio CSS imposta la dimensione del pulsante di riproduzione/pausa su 28x28 pixel sui sistemi con input del mouse e 56x56 pixel sui dispositivi touch. Inoltre, nasconde completamente il pulsante se le dimensioni del visualizzatore vengono ridotte in modo significativo:

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7interactivevideoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7interactivevideoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

In questo esempio successivo, la barra di controllo del video è posizionata a 138 pixel sopra il fondo del visualizzatore se il dispositivo touch è in orientamento verticale e in tutti gli altri casi la sposta nella parte inferiore del visualizzatore:

```
.s7interactivevideoviewer.s7touchinput.s7device_landscape .s7controlbar, 
.s7interactivevideoviewer.s7mouseinput .s7controlbar { 
 bottom:0px; 
} 
.s7interactivevideoviewer.s7touchinput.s7device_portrait .s7controlbar { 
 bottom:136px; 
}
```

Per eseguire il targeting di dispositivi con densità di pixel diversa è necessario utilizzare query multimediali CSS. Il seguente blocco di query per contenuti multimediali conterrebbe CSS specifici per le schermate ad alta densità:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilizzo dei marcatori CSS è il modo più flessibile per creare CSS reattivi, in quanto consente di eseguire il targeting non solo delle dimensioni dello schermo del dispositivo, ma anche delle dimensioni effettive del visualizzatore, utile per i layout di progettazione reattiva.

Puoi utilizzare il file CSS del visualizzatore predefinito come esempio di approccio CSS Markers.

**Query multimediali CSS**

Puoi anche eseguire il rilevamento dei dispositivi utilizzando semplici query multimediali CSS. Tutto ciò che è racchiuso in un determinato blocco di query multimediale viene applicato solo quando viene eseguito su un dispositivo corrispondente.

Se applicati ai visualizzatori mobili, utilizza quattro query multimediali CSS, definite nel CSS, nell’ordine indicato di seguito:

1. Contiene solo regole specifiche per tutti i dispositivi touch.

   ```
   @media only screen and (max-device-width:13.5in) and (max-device- 
   height:13.5in) and (max-device-width:799px),  
   only screen and (max-device-width:13.5in) and (max-device-height:13.5in)  
   and (max-device-height:799px) 
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

## Sprite CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Molti elementi dell’interfaccia utente del visualizzatore sono formattati utilizzando immagini bitmap e hanno più di un diverso stato visivo. Un buon esempio è un pulsante che normalmente ha almeno 3 stati diversi: &quot;su&quot;, &quot;sopra&quot; e &quot;giù&quot;. Ogni stato richiede l&#39;assegnazione di una propria immagine bitmap.

Con un approccio classico allo stile, il CSS avrebbe un riferimento separato al singolo file di immagine sul server per ogni stato dell’elemento dell’interfaccia utente. Di seguito è riportato un esempio di CSS per lo stile di un pulsante a schermo intero:

```
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

L’inconveniente di questo approccio è che l’utente finale si trova in una situazione di sfarfallio o di ritardo nella risposta dell’interfaccia utente quando l’elemento viene interagito per la prima volta. Questa azione si verifica perché l’immagine per il nuovo stato elemento non è ancora stata scaricata. Inoltre, questo approccio può avere un leggero impatto negativo sulle prestazioni a causa di un aumento del numero di chiamate HTTP al server.

Gli spriti CSS è un approccio diverso in cui l’immagine per tutti gli stati degli elementi viene combinata in un singolo file PNG denominato &quot;sprite&quot;. Tale &quot;sprite&quot; ha tutti gli stati visivi per l&#39;elemento specificato posizionato uno dopo l&#39;altro. Quando si crea lo stile di un elemento dell’interfaccia utente con sprites, viene fatta riferimento alla stessa immagine sprite per tutti gli stati diversi del CSS. Inoltre, la proprietà `background-position` viene utilizzata per ogni stato per specificare quale parte dell&#39;immagine &quot;sprite&quot; viene utilizzata. È possibile strutturare un&#39;immagine &quot;sprite&quot; in qualsiasi modo appropriato. In genere, i visualizzatori lo dispongono di una sovrapposizione verticale. Di seguito è riportato un esempio di stile dello stesso pulsante a schermo intero precedente basato su &quot;sprite&quot;:

```
.s7interactivevideoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7interactivevideoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Note generali sullo stile e consigli {#section-95855dccbbc444e79970f1aaa3260b7b}

* Quando si personalizza l’interfaccia utente del visualizzatore con CSS, l’utilizzo della regola `!IMPORTANT` non è supportato dagli elementi del visualizzatore di stili. In particolare, la regola `!IMPORTANT` non deve essere utilizzata per sostituire uno stile predefinito o di esecuzione fornito dal visualizzatore o dall’SDK del visualizzatore. Il motivo è che può influenzare il comportamento dei componenti appropriati. Invece, utilizza i selettori CSS con la specificità appropriata per impostare le proprietà CSS documentate in questa guida di riferimento.

* Tutti i percorsi delle risorse esterne all’interno dei CSS vengono risolti rispetto alla posizione CSS, non alla posizione della pagina HTML del visualizzatore. Tieni presente questa regola quando copi il CSS predefinito in una posizione diversa. Puoi copiare anche le risorse predefinite o aggiornare i percorsi all’interno del CSS personalizzato.
* Il formato preferito per le immagini bitmap è PNG.
* La grafica bitmap viene assegnata agli elementi dell&#39;interfaccia utente tramite la proprietà `background-image` .
* Le proprietà `width` e `height` di un elemento dell’interfaccia utente ne definiscono la dimensione logica. La dimensione della bitmap passata a `background-image` non influisce sulle dimensioni logiche.

* Per utilizzare l&#39;alta densità di pixel di schermi ad alta risoluzione come Retina, specificare immagini bitmap due volte più grandi della dimensione dell&#39;elemento dell&#39;interfaccia utente logica. Quindi, applica la proprietà `-webkit-background-size:contain` per ridimensionare lo sfondo fino alla dimensione dell&#39;elemento dell&#39;interfaccia utente logica.
* Per rimuovere un pulsante dall’interfaccia utente, aggiungi `display:none` alla relativa classe CSS.
* È possibile utilizzare vari formati per il valore del colore supportato da CSS. Se hai bisogno di trasparenza, utilizza il formato `rgba(R,G,B,A)`. In caso contrario, è possibile utilizzare il formato `#RRGGBB`.

## Elementi comuni dell&#39;interfaccia utente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Di seguito è riportata la documentazione di riferimento relativa agli elementi dell’interfaccia utente applicabili al visualizzatore video interattivo:
