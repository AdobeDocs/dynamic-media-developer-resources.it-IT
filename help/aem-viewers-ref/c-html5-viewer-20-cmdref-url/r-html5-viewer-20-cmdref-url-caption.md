---
title: didascalia
description: Parametro comune a tutti i visualizzatori.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 06ce5520-944b-4ab0-8f59-67c273bd8314
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 2%

---

# didascalia{#caption}

Parametro comune a tutti i visualizzatori.

>[!NOTE]
>
>Questo comando non è applicabile al Visualizzatore immagini video.

` caption= *`file`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto della didascalia WebVTT. Image Server genera il file WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica lo stato predefinito dei sottotitoli. Abilitato è <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Questo visualizzatore supporta i sottotitoli tramite file WebVTT in hosting. I sottotitoli specificati con questo parametro si applicano al video che arriva primo nei set di file multimediali; i video successivi vengono riprodotti senza sottotitoli. I cue e le aree di sovrapposizione non sono supportati. Operatori di posizionamento dei cue supportati:

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
   <td colname="col2"> <p>prova allineamento </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sinistra|destra|centro|inizio|fine </span> </p> </td> 
   <td colname="col4"> <p> Controlla l'allineamento del testo. </p> <p>Il valore predefinito è <span class="codeph"> </span> intermedio. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>posizione testo </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di inserimento nel componente VideoPlayer per l'inizio del testo della didascalia. </p> <p>Il valore predefinito è <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>dimensione linea </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di larghezza video utilizzata per i sottotitoli. </p> <p>Il valore predefinito è <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>posizione riga </p> </td> 
   <td colname="col3"> <p> 0%-100%|intero </p> </td> 
   <td colname="col4"> <p> Determina la posizione della linea sulla pagina. </p> <p>Se viene espresso come numero intero senza segno di percentuale, si tratta del numero di righe della parte superiore in cui viene visualizzato il testo. </p> <p>Se è espresso come percentuale (il segno di percentuale è l'ultimo carattere), il testo della didascalia viene visualizzato in percentuale nell'area di visualizzazione. </p> <p>Il valore predefinito è <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Se nel file WebVTT sono presenti altre funzionalità WebVTT, queste non sono supportate, ma non interrompono la creazione dei sottotitoli.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file </span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto di sottotitoli WebVTT. Il file WebVTT è gestito da Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0|1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica lo stato predefinito dei sottotitoli. </p> <p>Abilitato è <span class="codeph"> 1 </span>. </p> </td> 
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
