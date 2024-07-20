---
title: Personalizzazione del visualizzatore panoramico
description: Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni comportamentali per il visualizzatore panoramico vengono eseguite creando un CSS personalizzato.
keywords: responsive
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# Personalizzazione del visualizzatore Video360{#customizing-video-viewer}

Tutta la personalizzazione visiva e la maggior parte della personalizzazione dei comportamenti viene eseguita creando un CSS personalizzato.

Il flusso di lavoro suggerito consiste nel prendere il file CSS predefinito per il visualizzatore appropriato, copiarlo in una posizione diversa, personalizzarlo e specificare la posizione del file personalizzato nel comando `style=`.

I file CSS predefiniti si trovano nella posizione seguente:

`<s7viewers_root>/html5/PanoramicViewer.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quello predefinito. Se viene omessa una dichiarazione di classe, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell&#39;interfaccia utente.

Un modo alternativo di fornire regole CSS personalizzate consiste nell’utilizzare gli stili incorporati direttamente nella pagina web o in una delle regole CSS esterne collegate.

Durante la creazione di CSS personalizzati, ricorda che il visualizzatore assegna la classe `.s7panoramicviewer` al suo elemento DOM contenitore. Se si utilizza un file CSS esterno passato con il comando `style=`, utilizzare la classe `.s7panoramicviewer` come classe padre nel selettore discendente per le regole CSS. Se stai utilizzando stili incorporati nella pagina web, qualifica inoltre questo selettore con un ID dell’elemento DOM del contenitore come segue:

`#<containerId>.s7panoramicviewer.`


## Note generali sullo stile e consigli {#section-95855dccbbc444e79970f1aaa3260b7b}

* Tutti i percorsi delle risorse esterne all’interno di CSS vengono risolti in base alla posizione CSS, non in base alla posizione della pagina del visualizzatore HTML. Tieni presente questo aspetto durante la copia del CSS predefinito in una posizione diversa: potrebbe essere necessario copiare anche le risorse predefinite o aggiornare i percorsi all’interno del CSS personalizzato.
* Puoi utilizzare vari formati per il valore del colore supportato dai CSS. Se è necessaria la trasparenza, viene suggerito il formato `rgba(R,G,B,A)`. In caso contrario, non è richiesta la trasparenza `#RRGGBB`.

Quando si personalizza l&#39;interfaccia utente del visualizzatore con CSS, l&#39;utilizzo della regola `!IMPORTANT` non è supportato per gli elementi visualizzatore di stile. In particolare, la regola `!IMPORTANT` non deve essere utilizzata per ignorare eventuali stili predefiniti o di runtime forniti dal visualizzatore o dall&#39;SDK del visualizzatore, in quanto potrebbero influenzare il comportamento corretto dei componenti. Per impostare le proprietà CSS documentate in questa guida di riferimento, è invece necessario utilizzare i selettori CSS con la specifica appropriata.

## CSS visualizzatore panoramico {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Area visualizzatore principale**
L&#39;area di visualizzazione principale è l&#39;area occupata dall&#39;immagine panoramica.  In genere viene impostato per adattarsi allo schermo del dispositivo disponibile quando non è specificata alcuna dimensione.

L’aspetto dell’area di visualizzazione viene controllato con il selettore di classe CSS:
`.s7panoramicviewer`

Le proprietà CSS applicabili includono:

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> larghezza </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> larghezza del visualizzatore; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> altezza </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> altezza del visualizzatore; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio:
Per impostare un visualizzatore con dimensioni di 1024 x 512 pixel.

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Visualizzazione panoramica**
La vista principale è costituita dall&#39;immagine panoramica.

L’aspetto della visualizzazione principale è controllato con il selettore di classe CSS:
`.s7panoramicviewer .s7panoramicview`

Le proprietà CSS applicabili includono:
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> il colore di sfondo della visualizzazione principale; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio:
Per rendere trasparente la visualizzazione principale:

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
