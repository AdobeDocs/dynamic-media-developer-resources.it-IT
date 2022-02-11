---
title: Personalizzazione del visualizzatore video
description: Personalizzazione del visualizzatore video
keywords: reattivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Video
role: Developer,User
exl-id: 90dc93ee-fdd0-41c9-9eef-4c9952198356
source-git-commit: ceb9483f67a19d969ecbbd01cede11f3dae86467
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 0%

---

# Personalizzazione del visualizzatore video{#customizing-video-viewer}

Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni del comportamento vengono effettuate creando un CSS personalizzato.

Il flusso di lavoro consigliato consiste nell’accettare il file CSS predefinito per il visualizzatore appropriato, copiarlo in un percorso diverso, personalizzarlo e specificare il percorso del file personalizzato nella `style=` comando.

I file CSS predefiniti si trovano nel seguente percorso:

`<s7_viewers_root>/html5/VideoViewer.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quella predefinita. Se una dichiarazione di classe viene omessa, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell’interfaccia utente.

Un modo alternativo per fornire regole CSS personalizzate è quello di utilizzare stili incorporati direttamente sulla pagina web o in una delle regole CSS esterne collegate.

Quando crei CSS personalizzati, ricorda che il visualizzatore assegna `.s7videoviewer` all&#39;elemento DOM contenitore. Se utilizzi un file CSS esterno passato con `style=` comando, utilizza `.s7videoviewer` Classe come classe padre nel selettore discendente per le regole CSS. Se incorpori stili nella pagina web, qualifica anche questo selettore con un ID dell’elemento DOM del contenitore come segue:

`#<containerId>.s7videoviewer`

## Creazione di CSS reattivi {#section-63e8f93ee2f14fd8bba1ce33a6870b80}

È possibile eseguire il targeting di dispositivi diversi in CSS per rendere il contenuto visualizzato in modo diverso a seconda del dispositivo di un utente. Questo targeting include, ma non è limitato a, diverse dimensioni degli elementi dell&#39;interfaccia utente e risoluzione dell&#39;immagine.

Il visualizzatore supporta due meccanismi per creare CSS adattabili: Marcatori CSS e query multimediali CSS standard. Potete usare questi due meccanismi in modo indipendente o insieme.

**Marcatori CSS**

Per facilitare la creazione di CSS adattabili, il visualizzatore supporta i marcatori CSS che assegnano in modo dinamico classi CSS speciali all’elemento contenitore visualizzatore di livello principale. L&#39;assegnazione si basa sulle dimensioni del visualizzatore in fase di esecuzione e sul tipo di input utilizzato sul dispositivo corrente.

Il primo gruppo di marcatori CSS include `.s7size_large`, `.s7size_medium`e `.s7size_small` classi. Vengono applicati in base all’area di runtime del contenitore del visualizzatore. Se l&#39;area di visualizzazione è uguale o maggiore delle dimensioni di un monitor desktop comune `.s7size_large` è utilizzato; se l&#39;area è vicina alle dimensioni di un dispositivo tablet comune `.s7size_medium` è assegnato. per aree simili agli schermi dei telefoni cellulari, `.s7size_small` è impostato. Lo scopo principale di questi marcatori CSS è quello di creare layout di interfaccia utente diversi per schermi e dimensioni di visualizzatore diversi.

Il secondo gruppo di marcatori CSS include `.s7mouseinput` e `.s7touchinput`. Il marcatore `.s7touchinput` è impostato se il dispositivo corrente dispone di capacità di input touch; altrimenti, `.s7mouseinput` viene utilizzato. Questi marcatori sono destinati a creare elementi di input dell&#39;interfaccia utente con diverse dimensioni dello schermo per diversi tipi di input, perché normalmente l&#39;input touch richiede elementi più grandi. Nel caso in cui il dispositivo sia dotato di funzionalità di input del mouse e touch, `.s7touchinput` è impostato e il visualizzatore esegue il rendering di un’interfaccia utente touch.

Il seguente esempio CSS imposta la dimensione del pulsante di riproduzione/pausa su 28 x 28 pixel sui sistemi con input del mouse e 56 x 56 pixel sui dispositivi touch. Inoltre, nasconde completamente il pulsante se la dimensione del visualizzatore diventa troppo piccola:

```
.s7videoviewer.s7mouseinput .s7playpausebutton { 
    width:28px; 
    height:28px; 
} 
.s7videoviewer.s7touchinput .s7playpausebutton { 
    width:56px; 
    height:56px; 
} 
.s7videoviewer.s7size_small .s7playpausebutton { 
    visibility:hidden; 
}
```

Per eseguire il targeting dei dispositivi con una densità di pixel diversa, utilizza le query multimediali CSS. Il seguente blocco di query per contenuti multimediali conterrebbe CSS specifici per le schermate ad alta densità:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilizzo dei marcatori CSS è il modo più flessibile per creare CSS adattabili. Il motivo è che consente di eseguire il targeting non solo delle dimensioni dello schermo del dispositivo, ma anche di quelle effettive del visualizzatore, il che può essere utile per i layout reattivi della pagina di progettazione.

Utilizza il file CSS del visualizzatore predefinito come esempio di approccio a marcatori CSS.

**Query multimediali CSS**

Il rilevamento dei dispositivi può essere eseguito anche utilizzando semplici query multimediali CSS. Tutto ciò che è racchiuso in un determinato blocco di query multimediale viene applicato solo quando viene eseguito su un dispositivo corrispondente.

Quando vengono applicati ai visualizzatori mobili, utilizza quattro query multimediali CSS, definite nel CSS nell’ordine indicato di seguito:

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

Utilizzando l’approccio delle query multimediali CSS, è necessario organizzare i CSS con il rilevamento del dispositivo come segue:

* Innanzitutto, la sezione specifica per il desktop definisce tutte le proprietà specifiche per il desktop o comuni a tutte le schermate.
* In secondo luogo, le quattro query multimediali devono andare in ordine definito sopra e fornire regole CSS specifiche per il tipo di dispositivo corrispondente.

Non è necessario duplicare l’intero CSS del visualizzatore in ogni query multimediale. Solo le proprietà specifiche per determinati dispositivi vengono ridefinite all&#39;interno di una query multimediale.

## Sprite CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Molti elementi dell’interfaccia utente del visualizzatore sono formattati utilizzando immagini bitmap e hanno più di un diverso stato visivo. Un buon esempio è un pulsante che normalmente ha almeno tre stati diversi: &quot;su&quot;, &quot;sopra&quot; e &quot;giù&quot;. Ogni stato richiede l&#39;assegnazione di una propria immagine bitmap.

Con un approccio classico allo stile, il CSS avrebbe un riferimento separato al singolo file di immagine sul server per ogni stato dell’elemento dell’interfaccia utente. Di seguito è riportato un esempio di CSS per lo stile di un pulsante a schermo intero:

```
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='up'] {  
background-image:url(images/v2/PlayButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='over'] {  
background-image:url(images/v2/PlayButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='down'] {  
background-image:url(images/v2/PlayButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][state='disabled'] {  
background-image:url(images/v2/PlayButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='up'] {  
background-image:url(images/v2/PauseButton_up.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='over'] {  
background-image:url(images/v2/PauseButton_over.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='down'] {  
background-image:url(images/v2/PauseButton_down.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='false'][state='disabled'] {  
background-image:url(images/v2/PauseButton_disabled.png);  
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='up'] { 
background-image:url(images/v2/ReplayButton_up.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='over'] { 
background-image:url(images/v2/ReplayButton_over.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='down'] { 
background-image:url(images/v2/ReplayButton_down.png); 
} 
.s7videoviewer.s7mouseinput .s7playpausebutton[selected='true'][replay='true'][state='disabled'] { 
background-image:url(images/v2/ReplayButton_disabled.png); 
}
```

L’inconveniente di questo approccio è che l’utente finale si trova in una situazione di sfarfallio o di ritardo nella risposta dell’interfaccia utente quando l’elemento viene interagito per la prima volta. Questa azione si verifica perché l’immagine per il nuovo stato elemento non è ancora stata scaricata. Inoltre, questo approccio può avere un leggero impatto negativo sulle prestazioni a causa di un aumento del numero di chiamate HTTP al server.

Gli spriti CSS è un approccio diverso in cui l’immagine per tutti gli stati degli elementi viene combinata in un singolo file PNG denominato &quot;sprite&quot;. Tale &quot;sprite&quot; ha tutti gli stati visivi per l&#39;elemento specificato posizionato uno dopo l&#39;altro. Quando si crea lo stile di un elemento dell’interfaccia utente con sprites, viene fatto riferimento alla stessa immagine sprite per tutti gli stati diversi del CSS. Inoltre, il `background-position` viene utilizzata per ogni stato per specificare quale parte dell&#39;immagine &quot;sprite&quot; viene utilizzata. È possibile strutturare un&#39;immagine &quot;sprite&quot; in qualsiasi modo appropriato. In genere, i visualizzatori lo dispongono di una sovrapposizione verticale. Di seguito è riportato un esempio basato su &quot;sprite&quot; di stile dello stesso pulsante a schermo intero dall’alto:

```
.s7videoviewer .s7fullscreenbutton[state][selected]{ 
 background-image: url(images/v2/FullScreenButton_dark_sprite.png); 
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='up'] {  
background-position: -84px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='over'] {  
background-position: -56px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='down'] {  
background-position: -28px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='true'][state='disabled'] {  
background-position: -0px -1148px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='up'] {  
background-position: -84px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='over'] {  
background-position: -56px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='down'] {  
background-position: -28px -1120px;  
} 
.s7videoviewer.s7mouseinput .s7fullscreenbutton[selected='false'][state='disabled'] {  
background-position: -0px -1120px;  
}
```

## Note generali sullo stile e consigli {#section-097418bd618740bba36352629e4d88e1}

* Tutti i percorsi delle risorse esterne all’interno dei CSS vengono risolti rispetto alla posizione CSS non alla posizione della pagina HTML del visualizzatore. Ricorda di tenere conto di questa regola quando copi il CSS predefinito in una posizione diversa. Copia le risorse predefinite o i percorsi di aggiornamento all’interno del CSS personalizzato.
* Il formato preferito per le immagini bitmap è PNG.
* L’immagine bitmap viene assegnata agli elementi dell’interfaccia utente tramite `background-image` proprietà.
* La `width` e `height` le proprietà di un elemento dell’interfaccia utente ne definiscono la dimensione logica. Dimensione della bitmap passata a `background-image` non influisce sulle dimensioni logiche.

* Per utilizzare l&#39;alta densità di pixel di schermi ad alta risoluzione come Retina, specificare immagini bitmap due volte più grandi della dimensione dell&#39;elemento dell&#39;interfaccia utente logica. Quindi, applica il `-webkit-background-size:contain` per ridimensionare lo sfondo fino alle dimensioni dell&#39;elemento dell&#39;interfaccia utente logica.
* Per rimuovere un pulsante dall’interfaccia utente, aggiungi `display:none` alla relativa classe CSS.
* È possibile utilizzare vari formati per il valore del colore supportato da CSS. Se hai bisogno di trasparenza, utilizza il formato `rgba(R,G,B,A)`. In caso contrario, è possibile utilizzare il formato `#RRGGBB`.

* Quando si personalizza l’interfaccia utente del visualizzatore con CSS, l’utilizzo di `!IMPORTANT` La regola non è supportata per gli elementi del visualizzatore di stili. In particolare, `!IMPORTANT` Questa regola non deve essere utilizzata per sostituire uno stile predefinito o di esecuzione fornito dal visualizzatore o dall’SDK del visualizzatore. Il motivo è che può influenzare il comportamento dei componenti appropriati. Invece, utilizza i selettori CSS con la specificità appropriata per impostare le proprietà CSS documentate in questa guida di riferimento.

## Elementi comuni dell&#39;interfaccia utente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Di seguito è riportata la documentazione di riferimento relativa agli elementi dell’interfaccia utente applicabili al visualizzatore video:
