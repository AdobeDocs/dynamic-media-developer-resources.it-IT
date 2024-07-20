---
title: Personalizzazione del visualizzatore carosello
description: Tutta la personalizzazione visiva e la maggior parte della personalizzazione del comportamento per il visualizzatore carosello viene eseguita creando un CSS personalizzato.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Carousel Banners
role: Developer,User
exl-id: f392d830-5c75-45dd-bab8-29a38218790d
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '1343'
ht-degree: 0%

---

# Personalizzazione del visualizzatore carosello{#customizing-carousel-viewer}

Tutta la personalizzazione visiva e la maggior parte della personalizzazione del comportamento per il visualizzatore carosello viene eseguita creando un CSS personalizzato.

Il flusso di lavoro suggerito consiste nel prendere il file CSS predefinito per il visualizzatore appropriato, copiarlo in una posizione diversa, personalizzarlo e specificare la posizione del file personalizzato nel comando `style=`.

I file CSS predefiniti si trovano nella posizione seguente:

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/CarouselViewer_dotted_light.css`

Il visualizzatore è dotato di quattro file CSS preconfigurati, per indicatori set numerici e punteggiati, ciascuno in uno schema di colori &quot;chiaro&quot; e &quot;scuro&quot;. La versione con &quot;Luce punteggiata&quot; viene utilizzata per impostazione predefinita, ma è facile passare a una versione diversa utilizzando CSS standard diversi e impostando il parametro `SetIndicator.mode`. Altri CSS standard si trovano nella seguente posizione:

`<s7_viewers_root>/html5/CarouselViewer_dotted_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_dark.css`

`<s7_viewers_root>/html5/CarouselViewer_numeric_light.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quello predefinito. Se viene omessa una dichiarazione di classe, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell&#39;interfaccia utente.

Un modo alternativo di fornire regole CSS personalizzate consiste nell’utilizzare gli stili incorporati direttamente nella pagina web o in una delle regole CSS esterne collegate.

Quando crei un CSS personalizzato, tieni presente che il visualizzatore assegna la classe `.s7carouselviewer` al suo elemento DOM contenitore. Se si utilizza un file CSS esterno passato con il comando `style=`, utilizzare la classe `.s7carouselviewer` come classe padre nel selettore discendente per le regole CSS. Se stai aggiungendo stili incorporati alla pagina web, qualifica anche questo selettore con un ID dell’elemento DOM contenitore come segue:

`#<containerId>.s7carouselviewer`

## Creazione di CSS reattivo {#section-0bb49aca42d242d9b01879d5ba59d33b}

È possibile eseguire il targeting di dispositivi diversi e incorporare dimensioni in CSS per rendere il contenuto visualizzato in modo diverso, a seconda del dispositivo di un utente o di un particolare layout di pagina web. Questa tecnica include, ma non è limitata a, layout diversi, dimensioni degli elementi dell&#39;interfaccia utente e risoluzione del disegno.

Il visualizzatore supporta due meccanismi di creazione di CSS dinamici: marcatori CSS e query multimediali CSS standard. È possibile utilizzare questi due meccanismi in modo indipendente o insieme.

**Indicatori CSS**

Per facilitare la creazione di CSS dinamici, il visualizzatore supporta i marcatori CSS. Questi marcatori sono classi CSS speciali assegnate dinamicamente all’elemento contenitore del visualizzatore di primo livello. Si basano sulle dimensioni del visualizzatore runtime e sul tipo di input utilizzato sul dispositivo corrente.

Il primo gruppo di marcatori CSS contiene `.s7size_large`, `.s7size_medium` e `.s7size_small` classi. Vengono applicati in base all’area di runtime del contenitore del visualizzatore. Ad esempio, se l&#39;area del visualizzatore è uguale o maggiore delle dimensioni di un monitor desktop comune, utilizzare `.s7size_large`. Se l&#39;area è vicina a un dispositivo tablet comune, assegnare `.s7size_medium`. Per aree simili agli schermi dei cellulari, utilizzare `.s7size_small`. Lo scopo principale di questi marcatori CSS è quello di creare layout di interfaccia utente diversi per schermi e dimensioni di visualizzatore diverse.

Il secondo gruppo di marcatori CSS contiene `.s7mouseinput` e `.s7touchinput`. Il marcatore CSS `.s7touchinput` è impostato se il dispositivo corrente è un input tocco. In caso contrario, viene utilizzato `.s7mouseinput`. Questi marcatori sono destinati principalmente a creare elementi di input dell’interfaccia utente con dimensioni dello schermo diverse per tipi di input diversi, perché normalmente l’input tocco richiede elementi più grandi.

Il seguente esempio di CSS imposta la dimensione del pulsante di zoom in su 28 x 28 pixel nei sistemi con input del mouse e su 56 x 56 pixel nei dispositivi di input tocco. Se il visualizzatore è ancora più piccolo, è impostato su 20 x 20 pixel.

```
.s7carouselviewer.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7carouselviewer.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7carouselviewer.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

Per eseguire il targeting di dispositivi con densità di pixel diversa, è necessario utilizzare le query multimediali CSS. Il seguente blocco di query multimediale contiene CSS specifico per gli schermi ad alta densità:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L’utilizzo dei marcatori CSS è il modo più flessibile per creare CSS dinamici, in quanto consente di impostare come destinazione non solo la dimensione dello schermo del dispositivo, ma anche la dimensione effettiva del visualizzatore, utile per i layout di progettazione dinamici.

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

## Sprite CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

Molti elementi dell&#39;interfaccia utente del visualizzatore sono formattati utilizzando immagini bitmap e hanno più stati visivi distinti. Un buon esempio è un pulsante che normalmente ha almeno tre stati diversi: `up`, `over` e `down`. A ogni stato deve essere assegnato un disegno bitmap specifico.

Con un approccio classico allo stile, il CSS avrebbe un riferimento separato al singolo file di immagine sul server per ogni stato dell’elemento dell’interfaccia utente. Di seguito è riportato un esempio di CSS per la formattazione di un pulsante di zoom in:

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

Lo svantaggio di questo approccio è che l’utente finale riceve una risposta interattiva o ritardata dall’interfaccia quando l’elemento viene interagito per la prima volta. Questa azione si verifica perché il disegno dell&#39;immagine per il nuovo stato dell&#39;elemento non è ancora stato scaricato. Inoltre, questo approccio potrebbe avere un leggero impatto negativo sulle prestazioni a causa di un aumento del numero di chiamate HTTP al server.

Gli sprite CSS sono un approccio diverso in cui il disegno dell&#39;immagine per tutti gli stati degli elementi viene combinato in un unico file PNG chiamato &quot;sprite&quot;. Tale &quot;sprite&quot; ha tutti gli stati visivi per l&#39;elemento dato posizionati uno dopo l&#39;altro. Quando si applica uno stile a un elemento dell’interfaccia utente con sprite, si fa riferimento alla stessa immagine sprite per tutti i diversi stati nel CSS. Inoltre, la proprietà `background-position` viene utilizzata per ogni stato per specificare quale parte dell&#39;immagine &quot;sprite&quot; viene utilizzata. È possibile strutturare un&#39;immagine &quot;sprite&quot; in qualsiasi modo appropriato. I visualizzatori di solito lo sovrappongono verticalmente.

Di seguito è riportato un esempio basato su &quot;sprite&quot; di formattazione della stessa icona di punto attivo:

```
.s7carouselviewer .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7carouselviewer .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## Note generali sullo stile e consigli {#section-95855dccbbc444e79970f1aaa3260b7b}

* Quando si personalizza l&#39;interfaccia utente del visualizzatore con CSS, l&#39;utilizzo della regola `!IMPORTANT` non è supportato per gli elementi visualizzatore di stile. In particolare, la regola `!IMPORTANT` non deve essere utilizzata per sostituire gli stili predefiniti o di runtime forniti dal visualizzatore o dall&#39;SDK del visualizzatore. Questo perché può influenzare il comportamento dei componenti appropriati. Per impostare le proprietà CSS documentate in questa guida di riferimento per visualizzatori, utilizza piuttosto i selettori CSS con la specificità appropriata.
* Tutti i percorsi delle risorse esterne all’interno di CSS vengono risolti in base alla posizione CSS, non in base alla posizione della pagina del visualizzatore HTML. Tieni presente questa regola quando copi il CSS predefinito in una posizione diversa. Copia anche le risorse predefinite oppure aggiorna tutti i percorsi all’interno del CSS personalizzato.
* Il formato preferito per la grafica bitmap è PNG.
* Il disegno bitmap viene assegnato agli elementi dell&#39;interfaccia utente tramite la proprietà `background-image`.
* Le proprietà `width` e `height` di un elemento dell&#39;interfaccia utente ne definiscono la dimensione logica. La dimensione della bitmap passata a `background-image` non influisce sulla dimensione logica.
* Per utilizzare l&#39;elevata densità di pixel di schermi ad alta risoluzione come Retina, specificate un disegno bitmap di dimensioni doppie rispetto a quelle dell&#39;elemento dell&#39;interfaccia utente logico. Applicare quindi la proprietà `-webkit-background-size:contain` per ridurre lo sfondo alle dimensioni dell&#39;elemento dell&#39;interfaccia utente logica.
* Per rimuovere un pulsante dall&#39;interfaccia utente, aggiungere `display:none` alla relativa classe CSS.
* Per il valore del colore supportato dagli stili CSS è possibile utilizzare vari formati. Se è necessaria la trasparenza, utilizzare il formato `rgba(R,G,B,A)`. In caso contrario, è possibile utilizzare il formato `#RRGGBB`.

## Elementi comuni dell’interfaccia utente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Di seguito è riportata la documentazione di riferimento per gli elementi dell&#39;interfaccia utente applicabile al Visualizzatore immagini video:
