---
description: Parametro comune a tutti i visualizzatori.
seo-description: Parametro comune a tutti i visualizzatori.
seo-title: didascalia
solution: Experience Manager
title: didascalia
topic: Dynamic media
uuid: e5a715c4-9b5b-48fc-8228-5e7416e2b71a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# caption{#caption}

Parametro comune a tutti i visualizzatori.

>[!NOTE]
>
>Questo comando non si applica al visualizzatore di immagini video.

` caption= *`file`*[,0|1]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file </span></span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto della didascalia WebVTT. Image Server distribuisce il file WebVTT. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 0 | 1 </span> </p> </td> 
   <td colname="col2"> <p> Specifica lo stato predefinito della didascalia. Abilitato è <span class="codeph"> 1 </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Questo visualizzatore supporta i sottotitoli codificati mediante i file WebVTT ospitati. Le didascalie specificate con questo parametro si applicano al video che compare per primo nei set di file multimediali; i video successivi vengono riprodotti senza didascalie. Le aree e i suggerimenti sovrapposti non sono supportati. Operatori di posizionamento dei cue supportati:

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
   <td colname="col2"> <p>test align </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> sinistra|destra|centro|inizio|fine </span> </p> </td> 
   <td colname="col4"> <p> Controlla l’allineamento del testo. </p> <p>Il valore predefinito è <span class="codeph"> centrale </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> T </span> </p> </td> 
   <td colname="col2"> <p>posizione testo </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di inserimento nel componente VideoPlayer per l’inizio del testo della didascalia. </p> <p>Default is <span class="codeph"> 0% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> S </span> </p> </td> 
   <td colname="col2"> <p>dimensione linea </p> </td> 
   <td colname="col3"> <p> 0%-100% </p> </td> 
   <td colname="col4"> <p> Percentuale di larghezza video utilizzata per le didascalie. </p> <p>Default is <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> L </span> </p> </td> 
   <td colname="col2"> <p>posizione linea </p> </td> 
   <td colname="col3"> <p> 0%-100%|integer </p> </td> 
   <td colname="col4"> <p> Determina la posizione della linea sulla pagina. </p> <p>Se viene espresso come numero intero senza segno di percentuale, corrisponde al numero di righe dall'alto in cui viene visualizzato il testo. </p> <p>Se viene espresso come percentuale, il segno di percentuale è l'ultimo carattere, il testo della didascalia viene visualizzato con una percentuale in basso nell'area di visualizzazione. </p> <p>Default is <span class="codeph"> 100% </span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Tenere presente che se esistono altre funzionalità WebVTT presenti nel file WebVTT, non sono supportate; tuttavia, i sottotitoli non verranno interrotti.

<table id="table_CB7B4DFC6B654AECA1AF6594E3FD5C46"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> file </span></span> </p> </td> 
   <td colname="col2"> <p> Specifica un URL o un percorso per il contenuto di sottotitoli WebVTT. Il file WebVTT è gestito da Image Server. </p> </td> 
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

