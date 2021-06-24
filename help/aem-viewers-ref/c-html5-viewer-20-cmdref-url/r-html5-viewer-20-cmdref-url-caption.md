---
description: Parametro comune a tutti i visualizzatori.
solution: Experience Manager
title: didascalia
feature: Dynamic Media Classic,Visualizzatori,SDK/API
role: Developer,Business Practitioner
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 5%

---

# didascalia{#caption}

Parametro comune a tutti i visualizzatori.

>[!NOTE]
>
>Questo comando non si applica al visualizzatore di immagini video.

` caption= *`file`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto della didascalia WebVTT. Image Server serve il file WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica lo stato predefinito della didascalia. Abilitato è <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Questo visualizzatore supporta i sottotitoli codificati tramite file WebVTT in hosting. I sottotitoli specificati con questo parametro si applicano al video che compare per primo nei set di file multimediali; i video successivi vengono riprodotti senza didascalie. Le aree e i suggerimenti di sovrapposizione non sono supportati. Operatori di posizionamento dei cue supportati:

<table id="table_E752D7D8C1AA40C6B8A7057D2BB379C1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Chiave </p> </th> 
   <th colname="col2" class="entry"> <p>Nome </p> </th> 
   <th colname="col3" class="entry"> <p>Valori </p> </th> 
   <th colname="col4" class="entry"> <p>Descrizione </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> A </span> </p> </td> 
   <td colname="col2"> <p>allineamento del test </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sinistra|destra|mezzo|inizio|fine  </span> </p> </td> 
   <td colname="col4"> <p> Controlla l’allineamento del testo. </p> <p>Il valore predefinito è <span class="codeph"> intermedio </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>posizione testo </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di input nel componente VideoPlayer per l’inizio del testo della didascalia. </p> <p>Il valore predefinito è <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S  </span> </p> </td> 
   <td colname="col2"> <p>dimensioni linea </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di larghezza video utilizzata per le didascalie. </p> <p>Il valore predefinito è <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>posizione della linea </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Determina la posizione della linea sulla pagina. </p> <p>Se è espresso come numero intero senza segno di percentuale, si tratta del numero di righe dall'alto in cui viene visualizzato il testo. </p> <p>Se è espresso come percentuale, il segno di percentuale è l’ultimo carattere, il testo della didascalia viene visualizzato in modo che la percentuale scenda nell’area di visualizzazione. </p> <p>Il valore predefinito è <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Tieni presente che se nel file WebVTT sono presenti altre funzionalità WebVTT, queste non sono supportate; tuttavia, non interromperanno il sottotitolo.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file  </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto della didascalia WebVTT. Il file WebVTT viene gestito da Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica lo stato predefinito della didascalia. </p> <p>Abilitato è <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-10ee45d637134e0fbcd943c62578cb78}

Facoltativo.

## Predefinito {#section-d411e450028c460392cb8508f8ccc5d9}

Nessuno.

## Esempio {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
caption=Scene7SharedAssets/adobe_qbc_final_cc,1
```
