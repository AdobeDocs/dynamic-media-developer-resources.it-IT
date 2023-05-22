---
title: Personalizzazione del visualizzatore zoom di base
description: Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni comportamentali per il Visualizzatore zoom di base vengono eseguite creando un CSS personalizzato.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 9cbce980-83fd-40a7-8bcd-f9bc4dd477a8
source-git-commit: 61e3a1fd0e21d336eaf5232096f5b1b54f2a6353
workflow-type: tm+mt
source-wordcount: '1335'
ht-degree: 0%

---

# Personalizzazione del visualizzatore zoom di base{#customizing-basic-zoom-viewer}

Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni comportamentali per il Visualizzatore zoom di base vengono eseguite creando un CSS personalizzato.

Il flusso di lavoro consigliato consiste nel prendere il file CSS predefinito per il visualizzatore appropriato, copiarlo in una posizione diversa, personalizzarlo e specificare la posizione del file personalizzato nel `style=` comando.

I file CSS predefiniti si trovano nella posizione seguente:

`<s7_viewers_root>/html5/BasicZoomViewer_light.css`

Il visualizzatore viene fornito con due file CSS predefiniti, per combinazioni di colori &quot;chiaro&quot; e &quot;scuro&quot;. La versione &quot;chiara&quot; è utilizzata per impostazione predefinita, ma puoi passare alla versione &quot;scura&quot; utilizzando il seguente CSS standard:

`<s7_viewers_root>/html5/BasicZoomViewer_dark.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quello predefinito. Se viene omessa una dichiarazione di classe, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell&#39;interfaccia utente.

Un modo alternativo di fornire regole CSS personalizzate consiste nell’utilizzare gli stili incorporati direttamente nella pagina web o in una delle regole CSS esterne collegate.

Quando crei CSS personalizzato, tieni presente che il visualizzatore assegna `.s7basiczoomviewer` al relativo elemento DOM contenitore. Se utilizzi un file CSS esterno passato con `style=` comando, utilizza `.s7basiczoomviewer` come classe padre nel selettore discendente per le regole CSS. Se esegui stili incorporati nella pagina web, qualifica anche questo selettore con un ID dell’elemento DOM del contenitore come segue:

`#<containerId>.s7basiczoomviewer`

## Creazione di CSS di progettazione reattiva {#section-0bb49aca42d242d9b01879d5ba59d33b}

È possibile indirizzare dispositivi diversi e incorporare dimensioni in CSS per rendere la visualizzazione del contenuto diversa a seconda del dispositivo di un utente o di un layout di pagina web specifico. Questo targeting include, ma non è limitato a, layout diversi, dimensioni degli elementi dell’interfaccia utente e risoluzione del disegno.

Il visualizzatore supporta due meccanismi per la creazione di CSS dinamici: marcatori CSS e query multimediali CSS standard. È possibile utilizzare questi meccanismi in modo indipendente o insieme.

**Marcatori CSS**

Per facilitare la creazione di CSS dinamici, il visualizzatore supporta i marcatori CSS. Questi marcatori sono classi CSS speciali. Vengono assegnati in modo dinamico all’elemento contenitore del visualizzatore di primo livello in base alle dimensioni del visualizzatore in fase di esecuzione e al tipo di input utilizzato sul dispositivo corrente.

Il primo gruppo di marcatori CSS include `.s7size_large`, `.s7size_medium`, e `.s7size_small` classi. Vengono applicati in base all’area di runtime del contenitore del visualizzatore. Se l&#39;area del visualizzatore è uguale o superiore alle dimensioni di un monitor desktop comune, `.s7size_large` viene utilizzato; se l’area è vicina a un comune dispositivo tablet, `.s7size_medium` è assegnato. Per aree simili agli schermi dei telefoni cellulari, `.s7size_small` è impostato. Lo scopo principale di questi marcatori CSS è quello di creare layout di interfaccia utente diversi per schermi e dimensioni di visualizzatore diverse.

Il secondo gruppo di marcatori CSS contiene `.s7mouseinput` e `.s7touchinput`. Il `.s7touchinput` il marcatore viene impostato se il dispositivo corrente dispone di funzionalità di input tocco; in caso contrario, `.s7mouseinput` viene utilizzato. Questi marcatori sono destinati principalmente a creare elementi di input dell’interfaccia utente con dimensioni dello schermo diverse per tipi di input diversi, perché l’input tocco di solito richiede elementi più grandi. Nei casi in cui il dispositivo sia dotato di funzionalità di input del mouse e di funzionalità touch, `.s7touchinput` e il visualizzatore esegue il rendering di un’interfaccia touch-screen.

Il seguente esempio di CSS imposta la dimensione del pulsante di zoom in su 28 x 28 pixel nei sistemi con input del mouse e su 56 x 56 pixel nei dispositivi touch. Inoltre, il pulsante viene nascosto completamente se la dimensione del visualizzatore diventa piccola:

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton { 
    width:28px; 
    height:28px; 
} 
.s7basiczoomviewer.s7touchinput .s7zoominbutton { 
    width:56px; 
    height:56px; 
} 
.s7basiczoomviewer.s7size_small .s7zoominbutton { 
    visibility:hidden; 
}
```

Per eseguire il targeting di dispositivi con densità di pixel diversa, è necessario utilizzare le query multimediali CSS. Il seguente blocco di query multimediale contiene CSS specifico per gli schermi ad alta densità:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilizzo dei marcatori CSS è il modo più flessibile per creare CSS per la progettazione reattiva. Il motivo è che consente di impostare come destinazione non solo la dimensione dello schermo del dispositivo, ma anche quella effettiva del visualizzatore, utile per i layout reattivi.

Puoi utilizzare il file CSS del visualizzatore predefinito come esempio di approccio ai marcatori CSS.

**Query multimediali CSS**

Puoi anche eseguire il rilevamento dei dispositivi utilizzando query multimediali CSS pure. Tutto ciò che è racchiuso all’interno di un determinato blocco di query multimediale viene applicato solo quando viene eseguito su un dispositivo corrispondente.

Quando applicato ai visualizzatori mobili, utilizza quattro query multimediali CSS, definite nel CSS, nell’ordine elencato di seguito:

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

Utilizzando un approccio basato su query multimediali, è necessario organizzare i CSS con il rilevamento dei dispositivi come segue:

* Innanzitutto, la sezione specifica per il desktop definisce tutte le proprietà specifiche del desktop o comuni a tutti gli schermi.
* E, in secondo luogo, le quattro query multimediali vanno nell’ordine definito in precedenza e forniscono regole CSS specifiche per il tipo di dispositivo corrispondente.

Non è necessario duplicare l’intero CSS del visualizzatore in ogni query multimediale. Solo le proprietà specifiche di determinati dispositivi vengono ridefinite all&#39;interno di una query multimediale.

## Spunti CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Molti elementi dell&#39;interfaccia utente del visualizzatore sono formattati utilizzando immagini bitmap e hanno più stati visivi distinti. Un buon esempio è un pulsante che normalmente ha almeno tre stati diversi: &quot;su&quot;, &quot;su&quot; e &quot;giù&quot;. A ogni stato deve essere assegnato un disegno bitmap specifico.

Con un approccio classico allo stile, il CSS avrebbe un riferimento separato a un singolo file di immagine sul server per ogni stato dell’elemento dell’interfaccia utente. Di seguito è riportato un esempio di CSS per la formattazione del pulsante di zoom in:

```
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-image:url(images/v2/ZoomInButton_dark_up.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-image:url(images/v2/ZoomInButton_dark_over.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-image:url(images/v2/ZoomInButton_dark_down.png);  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] {  
background-image:url(images/v2/ZoomInButton_dark_disabled.png);  
}
```

Lo svantaggio di questo approccio è che l’utente finale riceve una risposta interattiva o ritardata dall’interfaccia quando l’elemento viene interagito per la prima volta. Questa azione si verifica perché il disegno dell&#39;immagine per il nuovo stato dell&#39;elemento non è ancora stato scaricato. Inoltre, questo approccio potrebbe avere un leggero impatto negativo sulle prestazioni a causa di un aumento del numero di chiamate HTTP al server.

Gli sprite CSS sono un approccio diverso in cui il disegno dell&#39;immagine per tutti gli stati degli elementi viene combinato in un unico file PNG chiamato &quot;sprite&quot;. Tale &quot;sprite&quot; ha tutti gli stati visivi per l&#39;elemento dato posizionati uno dopo l&#39;altro. Quando si applica uno stile a un elemento dell’interfaccia utente con sprite, si fa riferimento alla stessa immagine sprite per tutti i diversi stati nel CSS. Inoltre, il `background-position` viene utilizzata per ogni stato per specificare quale parte dell’immagine &quot;sprite&quot; viene utilizzata. È possibile strutturare un&#39;immagine &quot;sprite&quot; in qualsiasi modo appropriato. I visualizzatori di solito lo sovrappongono verticalmente. Di seguito è riportato un esempio basato su &quot;sprite&quot; di come formattare lo stesso pulsante di zoom in dall’alto:

```
.s7basiczoomviewer .s7zoominbutton[state]  { 
    background-image: url(images/v2/ZoomInButton_dark_sprite.png); 
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='up'] {  
background-position: -84px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='over'] {  
background-position: -56px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='down'] {  
background-position: -28px -560px;  
} 
.s7basiczoomviewer.s7mouseinput .s7zoominbutton[state='disabled'] { 
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

Di seguito è riportata la documentazione di riferimento sugli elementi dell’interfaccia utente applicabile al visualizzatore zoom di base:
