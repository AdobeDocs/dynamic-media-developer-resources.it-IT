---
description: URL per il visualizzatore video.
seo-description: URL per il visualizzatore video.
seo-title: didascalia
solution: Experience Manager
title: didascalia
topic: Dynamic media
uuid: 670d83c2-bfc5-411a-8581-5103a62aa8cf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 10%

---


# caption{#caption}

URL per il visualizzatore video.

` caption= *`file`*[,0|1]`

Il visualizzatore supporta i sottotitoli codificati nei file WebVTT ospitati. Le aree e i suggerimenti sovrapposti non sono supportati. Gli operatori di posizionamento dei cue supportati includono quanto segue:

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
   <td colname="col2"> <p>text, align </p> </td> 
   <td colname="col3"> <p><span class="codeph"> sinistra|destra|centro|inizio|fine</span> </p> </td> 
   <td colname="col4"> <p> Controllare l'allineamento del testo. </p> <p>Il valore predefinito è <span class="codeph"> mid</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>posizione testo </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di inserimento nel componente VideoPlayer per l’inizio del testo della didascalia. </p> <p>Il valore predefinito è 0%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>dimensione linea </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di larghezza video utilizzata per le didascalie. </p> <p>Il valore predefinito è 100%. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>posizione linea </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Determina la posizione della linea sulla pagina. </p> <p>Se viene espresso come numero intero (nessun segno percentuale), corrisponde al numero di righe dall'alto in cui viene visualizzato il testo. </p> <p>Se è una percentuale (il segno percentuale è l'ultimo carattere), il testo della didascalia viene visualizzato con la percentuale in basso nell'area di visualizzazione. </p> <p>Il valore predefinito è 100%. </p> </td> 
  </tr> 
 </tbody> 
</table>

Altre funzionalità WebVTT presenti nel file WebVTT non sono supportate, ma non devono interrompere i sottotitoli.

<table id="table_A5BB1C08DA4B425DBD0356C7D3693E75"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> file</span></span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto della didascalia WebVTT. Trasmissione del file WebVTT tramite ImageServer. </p> </td> 
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

