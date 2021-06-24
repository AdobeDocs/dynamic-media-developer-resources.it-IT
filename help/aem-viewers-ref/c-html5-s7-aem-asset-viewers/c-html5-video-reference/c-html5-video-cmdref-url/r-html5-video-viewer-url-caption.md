---
description: Comando URL per il visualizzatore video.
solution: Experience Manager
title: didascalia
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Video
role: Developer,Business Practitioner
exl-id: a9af3335-ae18-4399-9014-47ec0306a087
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 10%

---

# didascalia{#caption}

Comando URL per il visualizzatore video.

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
   <td colname="col1"> <p> A </p> </td> 
   <td colname="col2"> <p>allineamento testo </p> </td> 
   <td colname="col3"> <p><span class="codeph"> sinistra|destra|mezzo|inizio|fine</span> </p> </td> 
   <td colname="col4"> <p> Controllare l’allineamento del testo. </p> <p>Il valore predefinito è <span class="codeph"> middle</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>posizione testo </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di input nel componente VideoPlayer per l’inizio del testo della didascalia. </p> <p>Il valore predefinito è 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>dimensioni linea </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di larghezza video utilizzata per le didascalie. </p> <p>Il valore predefinito è 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
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
   <td colname="col1"> <p><span class="codeph"><span class="varname"> file</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto della didascalia WebVTT. Distribuire il file WebVTT tramite ImageServing. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p> Specifica lo stato predefinito della didascalia (abilitato è <span class="codeph"> 1</span>). </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-f42369774e2740dcb399626a0e4e930e}

Facoltativo.

## Predefinito {#section-d016470e92a74f98a18c4ab3489410a5}

Nessuno.

## Esempio {#section-7621c8ebd4144bc08a537d01bd9c3f2f}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
