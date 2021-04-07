---
description: Comando URL per il visualizzatore video interattivo.
solution: Experience Manager
title: didascalia
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video interattivi
role: Sviluppatore, Business Practices
exl-id: 8eb2aa50-52b9-4b63-9789-87e492f34a22
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 10%

---

# caption{#caption}

Comando URL per il visualizzatore video interattivo.

` caption= *`file`*[,0|1]`

Il visualizzatore supporta i sottotitoli codificati tramite file WebVTT in hosting. Le aree e i suggerimenti di sovrapposizione non sono supportati. Gli operatori di posizionamento dei cue supportati includono quanto segue:

<table id="table_62D89A06EC9E4E7983D1F26A2C85A621"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chiave </p> </th> 
   <th colname="col2" class="entry"> <p>Nome </p> </th> 
   <th colname="col3" class="entry"> <p>Valore </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>allineamento testo </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sinistra|destra|mezzo|inizio|fine  </span> </p> </td> 
   <td colname="col4"> <p> Controllare l’allineamento del testo. </p> <p>Il valore predefinito è <span class="codeph"> intermedio </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>posizione testo </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di input nel componente VideoPlayer per l’inizio del testo della didascalia. </p> <p>Il valore predefinito è 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S  </span> </p> </td> 
   <td colname="col2"> <p>dimensioni linea </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di larghezza video utilizzata per le didascalie. </p> <p>Il valore predefinito è 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>posizione della linea </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Determina la posizione della linea sulla pagina. </p> <p>Se è espresso come numero intero (senza segno di percentuale), si tratta del numero di righe dall'alto in cui viene visualizzato il testo. </p> <p>Se si tratta di una percentuale (il segno di percentuale è l’ultimo carattere), il testo della didascalia viene visualizzato con una percentuale inferiore all’area di visualizzazione. </p> <p>Il valore predefinito è 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

Altre funzionalità WebVTT presenti nel file WebVTT non sono supportate, ma non devono interrompere i sottotitoli.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto della didascalia WebVTT. Distribuire il file WebVTT tramite Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica lo stato predefinito della didascalia (abilitato è <span class="codeph"> 1 </span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

Nessuno.

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=is/content/content/dam/mac/aodmarketingna/_VTT/dm-viewers-content/video/Glacier.mp4.caption.vtt,1
```
