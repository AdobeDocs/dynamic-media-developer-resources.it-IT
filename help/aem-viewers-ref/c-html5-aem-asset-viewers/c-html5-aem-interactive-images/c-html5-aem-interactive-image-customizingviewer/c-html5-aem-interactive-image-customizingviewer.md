---
description: Per personalizzare l’aspetto e la maggior parte dei comportamenti per il visualizzatore immagini interattivo, dovete creare un CSS personalizzato.
keywords: responsive
seo-description: Per personalizzare l’aspetto e la maggior parte dei comportamenti per il visualizzatore immagini interattivo, dovete creare un CSS personalizzato.
seo-title: Personalizzazione del visualizzatore di immagini interattivo
solution: Experience Manager
title: Personalizzazione del visualizzatore di immagini interattivo
topic: Dynamic media
uuid: 19868e4e-c2c9-41e0-82a6-20884a9454a4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Personalizzazione del visualizzatore di immagini interattivo{#customizing-interactive-image-viewer}

Per personalizzare l’aspetto e la maggior parte dei comportamenti per il visualizzatore immagini interattivo, dovete creare un CSS personalizzato.

Il flusso di lavoro consigliato consiste nell&#39;acquisire il file CSS predefinito per il visualizzatore appropriato, copiarlo in un percorso diverso, personalizzarlo e specificare la posizione del file personalizzato nel `style=` comando.

I file CSS predefiniti si trovano nella posizione seguente:

`<s7viewers_root>/etc/dam/viewers/s7viewers/html5/InteractiveImage.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quella predefinita. Se viene omessa una dichiarazione di classe, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell&#39;interfaccia utente.

In alternativa, per fornire regole CSS personalizzate potete utilizzare gli stili incorporati direttamente sulla pagina Web o in una delle regole CSS esterne collegate.

Quando create CSS personalizzato, tenete presente che il visualizzatore assegna la `.s7interactiveimage` classe al relativo elemento DOM contenitore. Se utilizzate un file CSS esterno passato con il `style=` comando, utilizzate la `.s7interactiveimage` classe come classe principale nel selettore discendente per le regole CSS. Se aggiungete stili incorporati nella pagina Web, qualificate anche questo selettore con un ID dell’elemento DOM contenitore come segue:

`#<containerId>.s7interactiveimage`

## Creazione di CSS reattivi {#section-0bb49aca42d242d9b01879d5ba59d33b}

È possibile impostare come destinazione dispositivi e dimensioni di incorporazione diverse nei CSS per rendere diversa la visualizzazione dei contenuti, a seconda del dispositivo dell&#39;utente o di un particolare layout di pagina Web. Ciò include, ma non è limitato a, layout diversi, dimensioni degli elementi dell&#39;interfaccia utente e risoluzione dell&#39;immagine.

Il visualizzatore supporta due metodi per creare CSS reattivo: Marcatori CSS e query multimediali CSS standard. Potete utilizzarli in modo indipendente o insieme.

**Marcatori CSS**

Per facilitare la creazione di CSS reattivi, il visualizzatore supporta i marcatori CSS. Si tratta di classi CSS speciali che vengono assegnate dinamicamente all&#39;elemento contenitore del visualizzatore di livello principale. Sono basati sulle dimensioni del visualizzatore runtime e sul tipo di input utilizzato sul dispositivo corrente.

Il primo gruppo di marcatori CSS contiene `.s7size_large`, `.s7size_medium`e `.s7size_small` classi. Vengono applicate in base all&#39;area di runtime del contenitore del visualizzatore. Ad esempio, se l’area del visualizzatore è uguale o maggiore delle dimensioni di un monitor desktop comune, utilizzate `.s7size_large`. Se l&#39;area è vicina a un dispositivo tablet comune, assegnare `.s7size_medium`. Per aree simili agli schermi dei telefoni cellulari, utilizzare `.s7size_small`. Lo scopo principale di questi marcatori CSS è quello di creare layout di interfaccia utente diversi per schermi e dimensioni di visualizzatore diversi.

Il secondo gruppo di marcatori CSS contiene `.s7mouseinput` e `.s7touchinput`. Il marcatore CSS `.s7touchinput` è impostato se il dispositivo corrente è in grado di inviare un segnale di ingresso touch. In caso contrario `.s7mouseinput` viene utilizzato. Questi marcatori sono destinati principalmente alla creazione di elementi di input dell&#39;interfaccia utente con diverse dimensioni di schermo per diversi tipi di input, perché normalmente l&#39;input tocco richiede elementi più grandi.

Il seguente file CSS di esempio imposta la dimensione del pulsante di zoom su 28x28 pixel nei sistemi con input del mouse e su 56x56 pixel nei dispositivi di input touch. Se il visualizzatore è ancora più piccolo, viene impostato su 20 x 20 pixel.

```
.s7interactiveimage.s7mouseinput .s7imagemapeffect .s7icon { 
    width:28px; 
    height:28px; 
} 
.s7interactiveimage.s7touchinput .s7imagemapeffect .s7icon { 
    width:56px; 
    height:56px; 
} 
.s7interactiveimage.s7size_small .s7imagemapeffect .s7icon { 
    width:20px; 
    height:20px; 
}
```

Per i dispositivi con densità di pixel diversa è necessario utilizzare le media query CSS. Il seguente blocco di query per file multimediali contiene CSS specifico per le schermate ad alta densità:

```
@media screen and (-webkit-min-device-pixel-ratio: 1.5) 
{ 
}
```

L&#39;utilizzo dei marcatori CSS è il modo più flessibile per creare CSS reattivo, in quanto consente di impostare come destinazione non solo la dimensione dello schermo del dispositivo, ma anche la dimensione effettiva del visualizzatore, il che è utile per i layout di progettazione reattivi.

Potete usare il file CSS del visualizzatore predefinito come esempio di approccio basato su marcatori CSS.

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

Molti elementi dell’interfaccia utente del visualizzatore sono formattati utilizzando immagini bitmap e hanno più di un diverso stato visivo. Un buon esempio è rappresentato da un pulsante con almeno tre stati diversi: `up`, `over`, e `down`. A ogni stato è assegnata una propria immagine bitmap.

Con un approccio classico allo stile, il CSS avrebbe un riferimento separato al singolo file di immagine sul server per ogni stato dell&#39;elemento dell&#39;interfaccia utente. Di seguito è riportato un esempio di CSS per lo stile di un pulsante di zoom in:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_over_touch.png); 
}
```

Lo svantaggio di questo approccio è che l&#39;utente finale si trova in una situazione di sfarfallio o ritardo nella risposta dell&#39;interfaccia utente quando l&#39;elemento viene interagito per la prima volta. Questa azione si verifica perché la grafica dell&#39;immagine per il nuovo stato dell&#39;elemento non è ancora stata scaricata. Inoltre, questo approccio potrebbe avere un lieve impatto negativo sulle prestazioni a causa di un aumento del numero di chiamate HTTP al server.

Gli spriti CSS sono un approccio diverso in cui la grafica immagine per tutti gli stati degli elementi viene combinata in un singolo file PNG denominato &quot;sprite&quot;. Tale &quot;sprite&quot; contiene tutti gli stati visivi per l&#39;elemento specificato posizionato uno dopo l&#39;altro. Quando si formatta un elemento dell&#39;interfaccia utente con sprite, viene fatto riferimento alla stessa immagine sprite per tutti gli stati diversi del CSS. Inoltre, la `background-position` proprietà viene utilizzata per ogni stato per specificare quale parte dell&#39;immagine &quot;sprite&quot; viene utilizzata. Potete strutturare un&#39;immagine &quot;sprite&quot; in qualsiasi modo appropriato. In genere, i visualizzatori possono sovrapporsi verticalmente.

Di seguito è riportato un esempio basato su &quot;sprite&quot; in cui viene formattato in precedenza lo stesso pulsante di zoom in:

```
.s7interactiveimage .s7imagemapeffect .s7icon { 
background-image: url(images/v2/imagemap/ImageMapEffect_icon1_light_up_touch.png); 
background-position: -0px -56px; width: 56px; height: 56px; 
} 
.s7interactiveimage .s7imagemapeffect .s7icon:hover { 
background-position: -0px -0px; width: 56px; height: 56px; 
}
```

## Note generali di stile e consigli {#section-95855dccbbc444e79970f1aaa3260b7b}

* Quando personalizzate l&#39;interfaccia utente del visualizzatore con CSS, l&#39;uso della `!IMPORTANT` regola non è supportato per gli elementi del visualizzatore di stile. In particolare, `!IMPORTANT` la regola non deve essere utilizzata per ignorare eventuali stili predefiniti o runtime forniti dall’SDK del visualizzatore o del visualizzatore. Questo può influenzare il comportamento dei componenti appropriati. Al contrario, utilizzate i selettori CSS con la specifica appropriata per impostare le proprietà CSS documentate in questa guida di riferimento dei visualizzatori.
* Tutti i percorsi delle risorse esterne all&#39;interno di CSS vengono risolti rispetto al percorso CSS, non al percorso della pagina HTML del visualizzatore. Tenete presente questa regola quando copiate il CSS predefinito in un percorso diverso. Potete copiare anche le risorse predefinite oppure aggiornare tutti i percorsi all&#39;interno del CSS personalizzato.
* Il formato preferito per la grafica bitmap è PNG.
* La grafica bitmap viene assegnata agli elementi dell&#39;interfaccia utente tramite la `background-image` proprietà .
* Le dimensioni logiche `width` e `height` le proprietà di un elemento dell&#39;interfaccia utente sono definite. Le dimensioni dell’elemento bitmap passato non `background-image` influiscono sulle sue dimensioni logiche.
* Per utilizzare l&#39;alta densità di pixel di schermi ad alta risoluzione come Retina, specificate immagini bitmap il doppio delle dimensioni dell&#39;elemento logico dell&#39;interfaccia utente. Quindi, applicate la `-webkit-background-size:contain` proprietà per ridimensionare lo sfondo fino alla dimensione logica dell&#39;elemento dell&#39;interfaccia utente.
* Per rimuovere un pulsante dall&#39;interfaccia utente, aggiungete `display:none` alla classe CSS corrispondente.
* Potete usare vari formati per il valore del colore supportato da CSS. Se avete bisogno di trasparenza, usate il formato `rgba(R,G,B,A)`. In caso contrario, è possibile utilizzare il formato `#RRGGBB`.

## Elementi comuni dell&#39;interfaccia utente {#section-d6330c9be8c444aa9b2a07886e3dbc2a}

Di seguito è riportata la documentazione di riferimento degli elementi dell’interfaccia utente applicata al visualizzatore di immagini video:
