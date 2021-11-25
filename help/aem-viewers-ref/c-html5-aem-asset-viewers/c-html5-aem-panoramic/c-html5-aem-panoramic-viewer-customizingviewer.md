---
title: Personalizzazione del visualizzatore panoramico
description: Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni del comportamento per il visualizzatore panoramico vengono effettuate creando un CSS personalizzato.
keywords: reattivo
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# Personalizzazione del visualizzatore video360{#customizing-video-viewer}

Tutte le personalizzazioni visive e la maggior parte delle personalizzazioni del comportamento vengono effettuate creando un CSS personalizzato.

Il flusso di lavoro consigliato consiste nell’accettare il file CSS predefinito per il visualizzatore appropriato, copiarlo in un percorso diverso, personalizzarlo e specificare il percorso del file personalizzato nella `style=` comando.

I file CSS predefiniti si trovano nel seguente percorso:

`<s7viewers_root>/html5/PanoramicViewer.css`

Il file CSS personalizzato deve contenere le stesse dichiarazioni di classe di quella predefinita. Se una dichiarazione di classe viene omessa, il visualizzatore non funziona correttamente perché non fornisce stili predefiniti incorporati per gli elementi dell’interfaccia utente.

Il modo alternativo per fornire regole CSS personalizzate consiste nell’utilizzare stili incorporati direttamente sulla pagina web o in una delle regole CSS esterne collegate.

Quando crei CSS personalizzati, ricorda che il visualizzatore assegna `.s7panoramicviewer` all&#39;elemento DOM contenitore. Se utilizzi un file CSS esterno passato con `style=` comando, utilizza `.s7panoramicviewer` Classe come classe padre nel selettore discendente per le regole CSS. Se stai utilizzando stili incorporati nella pagina web, qualifica inoltre questo selettore con un ID dell’elemento DOM del contenitore come segue:

`#<containerId>.s7panoramicviewer.`


## Note generali sullo stile e consigli {#section-95855dccbbc444e79970f1aaa3260b7b}

* Tutti i percorsi delle risorse esterne all’interno dei CSS vengono risolti rispetto alla posizione CSS, non alla posizione della pagina HTML del visualizzatore. Tieni presente questo aspetto quando copi il CSS predefinito in una posizione diversa: potrebbe essere necessario copiare anche le risorse predefinite o aggiornare i percorsi all’interno del CSS personalizzato.
* È possibile utilizzare vari formati per il valore del colore supportato da CSS. Se la trasparenza è necessaria, `rgba(R,G,B,A)` Il formato è consigliato. In caso contrario, la trasparenza non è necessaria `#RRGGBB` può essere utilizzato.

Quando personalizzi l’interfaccia utente del visualizzatore con CSS, utilizza `!IMPORTANT` La regola non è supportata per gli elementi del visualizzatore di stili. In particolare, `!IMPORTANT` Questa regola non deve essere utilizzata per sostituire uno stile predefinito o di esecuzione fornito dal visualizzatore o dall’SDK del visualizzatore in quanto potrebbe influenzare il comportamento corretto dei componenti. Al contrario, i selettori CSS con specificità corretta devono essere utilizzati per impostare le proprietà CSS documentate in questa guida di riferimento.

## CSS per visualizzatore panoramico {#section-9b6d8d601cb441d08214dada7bb4eddc}

**Area visualizzatore principale**
L&#39;area di visualizzazione principale è l&#39;area occupata dall&#39;immagine panoramica.  In genere viene impostato per adattarsi alla schermata del dispositivo disponibile quando non viene specificata alcuna dimensione.

L’aspetto dell’area di visualizzazione è controllato con il selettore di classe CSS:
`.s7panoramicviewer`

Le proprietà CSS applicabili includono:

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> la larghezza del visualizzatore; </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> l’altezza del visualizzatore; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: Impostare un visualizzatore con dimensioni 1024 x 512 pixel

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**Vista panoramica**
La vista principale è costituita dall’immagine panoramica.

L’aspetto della vista principale è controllato con il selettore di classe CSS:
`.s7panoramicviewer .s7panoramicview`

Le proprietà CSS applicabili includono:
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> colore di sfondo </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> colore di sfondo della vista principale; </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

Esempio: Per rendere trasparente la vista principale:

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
