---
title: Personalizzazione del visualizzatore zoom di base
description: Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni del comportamento per il visualizzatore zoom di base vengono effettuate creando un CSS personalizzato.
keywords: reattivo
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

Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni del comportamento per il visualizzatore zoom di base vengono effettuate creando un CSS personalizzato.

Il flusso di lavoro consigliato consiste nell’accettare il file CSS predefinito per il visualizzatore appropriato, copiarlo in un percorso diverso, personalizzarlo e specificare il percorso del file personalizzato nella `style=` comando.

I file CSS predefiniti si trovano nel seguente percorso:

`<s7_viewers_root>/html5/BasicZoomViewer_light.css`

Il visualizzatore viene fornito con due file CSS preconfigurati, per schemi di colore &quot;chiari&quot; e &quot;scuri&quot;. La versione &quot;chiara&quot; viene utilizzata per impostazione predefinita, ma puoi passare alla versione &quot;scura&quot; utilizzando il seguente CSS standard:

`<s7_viewers_root>/html5/BasicZoomViewer_dark.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quella predefinita. Se una dichiarazione di classe viene omessa, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell’interfaccia utente.

Il modo alternativo per fornire regole CSS personalizzate consiste nell’utilizzare stili incorporati direttamente sulla pagina web o in una delle regole CSS esterne collegate.

Quando crei CSS personalizzati, ricorda che il visualizzatore assegna `.s7basiczoomviewer` all&#39;elemento DOM contenitore. Se utilizzi un file CSS esterno passato con `style=` comando, utilizza `.s7basiczoomviewer` Classe come classe padre nel selettore discendente per le regole CSS. Se esegui stili incorporati nella pagina web, qualifica anche questo selettore con un ID dell’elemento DOM contenitore come segue:

`#<containerId>.s7basiczoomviewer`

## Creazione di CSS per design reattivo {#section-0bb49aca42d242d9b01879d5ba59d33b}

È possibile indirizzare diversi dispositivi e dimensioni di incorporamento in CSS per rendere la visualizzazione del contenuto diversa a seconda del dispositivo di un utente o di un particolare layout di pagina web. Questo targeting include, ma non è limitato a, diversi layout, dimensioni degli elementi dell&#39;interfaccia utente e risoluzione delle immagini.

Il visualizzatore supporta due meccanismi per creare CSS adattabili: Marcatori CSS e query multimediali CSS standard. Puoi usare questi meccanismi in modo indipendente o insieme.

**Marcatori CSS**

Per facilitare la creazione di CSS adattabili, il visualizzatore supporta i marcatori CSS. Questi marcatori sono classi CSS speciali. Vengono assegnati in modo dinamico all’elemento contenitore di visualizzatori di livello superiore in base alle dimensioni del visualizzatore in fase di esecuzione e al tipo di input utilizzato sul dispositivo corrente.

Il primo gruppo di marcatori CSS include `.s7size_large`, `.s7size_medium`e `.s7size_small` classi. Vengono applicati in base all’area in fase di esecuzione del contenitore del visualizzatore. Se l&#39;area di visualizzazione è uguale o maggiore delle dimensioni di un monitor desktop comune, allora `.s7size_large` è utilizzato; se l&#39;area è vicina a un dispositivo tablet comune, allora `.s7size_medium` è assegnato. per aree simili agli schermi dei telefoni cellulari, `.s7size_small` è impostato. Lo scopo principale di questi marcatori CSS è quello di creare layout di interfaccia utente diversi per schermi e dimensioni di visualizzatore diversi.

Il secondo gruppo di marcatori CSS contiene `.s7mouseinput` e `.s7touchinput`. La `.s7touchinput` è impostato se il dispositivo corrente dispone di capacità di ingresso touch; altrimenti, `.s7mouseinput` viene utilizzato. Questi marker sono destinati principalmente a creare elementi di input dell&#39;interfaccia utente con diverse dimensioni dello schermo per diversi tipi di input, perché l&#39;input touch richiede normalmente elementi più grandi. Nei casi in cui il dispositivo dispone sia di input del mouse che di funzionalità touch, `.s7touchinput` è impostato e il visualizzatore esegue il rendering di un’interfaccia utente touch.

Il seguente esempio CSS imposta le dimensioni del pulsante zoom in su 28 x 28 pixel sui sistemi con input del mouse e su 56 x 56 pixel sui dispositivi touch. Inoltre, nasconde completamente il pulsante se le dimensioni del visualizzatore sono piccole:

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

Per eseguire il targeting di dispositivi con densità di pixel diversa, è necessario utilizzare query multimediali CSS. Il seguente blocco di query per contenuti multimediali conterrebbe CSS specifici per le schermate ad alta densità:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilizzo dei marcatori CSS è il modo più flessibile per creare CSS per una progettazione reattiva. Il motivo è che ti consente di eseguire il targeting non solo delle dimensioni dello schermo del dispositivo, ma anche delle dimensioni effettive del visualizzatore, utile per i layout reattivi progettati.

Puoi utilizzare il file CSS del visualizzatore predefinito come esempio di approccio CSS Markers.

**Query multimediali CSS**

Puoi anche eseguire il rilevamento dei dispositivi utilizzando semplici query CSS per file multimediali. Tutto ciò che è racchiuso in un determinato blocco di query multimediale viene applicato solo quando viene eseguito su un dispositivo corrispondente.

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

Molti elementi dell’interfaccia utente del visualizzatore sono formattati utilizzando immagini bitmap e hanno più di un diverso stato visivo. Un buon esempio è un pulsante che normalmente ha almeno tre stati diversi: &quot;su&quot;, &quot;sopra&quot; e &quot;giù&quot;. Ogni stato richiede l&#39;assegnazione di una propria immagine bitmap.

Con un approccio classico allo stile, il CSS avrebbe un riferimento separato al singolo file di immagine sul server per ogni stato dell’elemento dell’interfaccia utente. Di seguito è riportato un esempio di CSS per lo stile del pulsante di ingrandimento:

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

L’inconveniente di questo approccio è che l’utente finale si trova in una situazione di sfarfallio o di ritardo nella risposta dell’interfaccia utente quando l’elemento viene interagito per la prima volta. Questa azione si verifica perché l’immagine per il nuovo stato elemento non è ancora stata scaricata. Inoltre, questo approccio può avere un leggero impatto negativo sulle prestazioni a causa di un aumento del numero di chiamate HTTP al server.

Gli spriti CSS è un approccio diverso in cui l’immagine per tutti gli stati degli elementi viene combinata in un singolo file PNG denominato &quot;sprite&quot;. Tale &quot;sprite&quot; ha tutti gli stati visivi per l&#39;elemento specificato posizionato uno dopo l&#39;altro. Quando si crea lo stile di un elemento dell’interfaccia utente con sprites, viene fatto riferimento alla stessa immagine sprite per tutti gli stati diversi del CSS. Inoltre, il `background-position` viene utilizzata per ogni stato per specificare quale parte dell&#39;immagine &quot;sprite&quot; viene utilizzata. È possibile strutturare un&#39;immagine &quot;sprite&quot; in qualsiasi modo appropriato. In genere, i visualizzatori lo dispongono di una sovrapposizione verticale. Di seguito è riportato un esempio basato su &quot;sprite&quot; di stile dello stesso pulsante di zoom in dall’alto:

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

* Quando si personalizza l’interfaccia utente del visualizzatore con CSS, l’utilizzo di `!IMPORTANT` La regola non è supportata per gli elementi del visualizzatore di stili. In particolare, `!IMPORTANT` Questa regola non deve essere utilizzata per sostituire uno stile predefinito o di esecuzione fornito dal visualizzatore o dall’SDK del visualizzatore. Il motivo è che può influenzare il comportamento dei componenti appropriati. Invece, utilizza i selettori CSS con la specificità appropriata per impostare le proprietà CSS documentate in questa guida di riferimento.
* Tutti i percorsi delle risorse esterne all’interno dei CSS vengono risolti rispetto alla posizione CSS, non alla posizione della pagina HTML del visualizzatore. Tieni presente questa regola quando copi il CSS predefinito in una posizione diversa. Puoi copiare anche le risorse predefinite o aggiornare i percorsi all’interno del CSS personalizzato.
* Il formato preferito per le immagini bitmap è PNG.
* L’immagine bitmap viene assegnata agli elementi dell’interfaccia utente tramite `background-image` proprietà.
* La `width` e `height` le proprietà di un elemento dell’interfaccia utente ne definiscono la dimensione logica. Dimensione della bitmap passata a `background-image` non influisce sulle dimensioni logiche.
* Per utilizzare l&#39;alta densità di pixel di schermi ad alta risoluzione come Retina, specificare immagini bitmap due volte più grandi della dimensione dell&#39;elemento dell&#39;interfaccia utente logica. Quindi, applica il `-webkit-background-size:contain` per ridimensionare lo sfondo fino alle dimensioni dell&#39;elemento dell&#39;interfaccia utente logica.
* Per rimuovere un pulsante dall’interfaccia utente, aggiungi `display:none` alla relativa classe CSS.
* È possibile utilizzare vari formati per il valore del colore supportato da CSS. Se hai bisogno di trasparenza, utilizza il formato `rgba(R,G,B,A)`. In caso contrario, è possibile utilizzare il formato `#RRGGBB`.

## Elementi comuni dell&#39;interfaccia utente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Di seguito è riportata la documentazione di riferimento relativa agli elementi dell’interfaccia utente applicabili al visualizzatore zoom di base:
