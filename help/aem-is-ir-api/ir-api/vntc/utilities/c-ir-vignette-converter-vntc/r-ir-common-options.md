---
description: Le seguenti opzioni possono essere applicate indipendentemente dal tipo di sourceFile.
solution: Experience Manager
title: Opzioni comuni
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---


# Opzioni comuni{#common-options}

Le seguenti opzioni possono essere applicate indipendentemente dal tipo di sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath  <span class="varname"> string  </span> </span> </p> </td> 
  <td class="stentry"> <p>Cartella in cui devono essere inseriti i file di output (compreso il file di registro, se è specificato <span class="codeph"> -log </span>). Può essere un percorso assoluto o relativo alla directory di lavoro corrente. La gerarchia delle cartelle verrà creata se non esiste. Non si applica al file specificato con <span class="codeph"> -log </span>. Se non viene specificato, i file di output vengono scritti nella cartella in cui si trova <span class="varname"> sourceFile </span>. Se <span class="varname"> destFile </span> è specificato, verrà sempre scritto in tale posizione e <span class="codeph"> -destpath </span> si applica solo ai file di output secondari. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image  </span> </p> </td> 
  <td class="stentry"> <p>Se specificato, l'immagine (prima) di visualizzazione viene estratta dalla vignetta, da un'immagine adatta a un pannello da uno stile di armadio o dalla prima immagine di illuminazione di uno stile di rivestimento di una finestra. L'immagine estratta viene salvata come file TIFF a risoluzione piena. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Impedisce la generazione di file di destinazione. Utile per estrarre rapidamente gli attributi da <span class="varname"> sourceFile </span>. Vengono generate solo la miniatura opzionale ( <span class="codeph"> -thumbwidth </span>), l'immagine ( <span class="codeph"> -image </span>) e i file di registro ( <span class="codeph"> -log </span>). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Seleziona la codifica JPEG con perdita per RGB e i dati immagine in scala di grigio incorporati nel file di output, invece di PNG senza perdita. Le immagini con alfa (RGBA) vengono sempre salvate utilizzando la codifica PNG. <span class="varname"> ival  </span> specifica la qualità JPEG (1...100); Si consiglia 85 o superiore. Il valore predefinito è <span class="codeph"> -jpegquality 0 </span>, che seleziona la codifica PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> percorso del registro  </span> </span> </p> </td> 
  <td class="stentry"> <p>Crea un file di registro con il percorso/nome specificato I percorsi completi di tutti i file di output scritti nella cartella di destinazione vengono scritti nel file di registro, nonché alcune impostazioni aggiuntive, come informazioni sulla versione e eventuali avvisi o errori rilevati (per ulteriori informazioni, vedere <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Output </a> ). Non viene creato alcun file di registro se <span class="codeph"> -log </span> non è specificato; in questo caso, tutto l'output di testo viene scritto in <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> Festival a priorità bassa  </span> </span> </p> </td> 
  <td class="stentry"> <p>Ridurre la priorità del processo <span class="filepath"> vntc </span>. Questo può essere utilizzato in modo che <span class="filepath"> vntc </span> non prenda in mano un'intera CPU durante l'elaborazione di una vignetta. Consente al sistema operativo di dare più tempo ad altri processi, più importanti. <span class="varname"> ival  </span> specifica la percentuale di priorità inferiore (0.100). Il valore predefinito è <span class="codeph"> -lowerpriority 0 </span>, che non riduce la priorità del processo <span class="filepath"> vntc </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Specificare la quantità massima di memoria che <span class="filepath"> vntc </span> può utilizzare in byte. Quando <span class="filepath"> vntc </span> raggiunge il limite massimo di memoria, interrompe l'elaborazione e genera un errore. <span class="varname"> ival  </span> specifica il limite massimo di memoria in byte (0.. 3.758.096.384 (3,5 GB)). Quando <span class="varname"> ival </span> è 0, il limite massimo di memoria è disattivato. Il valore predefinito è <span class="codeph"> -maxmem 3221225472 </span>, il che significa un limite massimo di memoria di 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separatore "  <span class="varname"> stringa  </span>"  </span> </p> </td> 
  <td class="stentry"> <p>Specifica il separatore posizionato tra il nome del file e il suffisso dimensione/risoluzione per i nomi dei file di output generati automaticamente. Il valore predefinito è "-" se non specificato. Ignorato se è specificato <span class="varname"> destFile </span> o <span class="codeph"> -info </span> . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -affilare  <span class="varname"> Festival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Abilita la nitidezza delle immagini ricampionate (ridimensionate) durante l’elaborazione. Si applica solo alla nitidezza delle miniature in caso di file di stile archivio. </p> <p>Specificare 0 per disattivare la nitidezza (impostazione predefinita), 1 per abilitare la nitidezza normale, 2 per attivare la Mascheratura per la luminosità solo o 3 per attivare la Mascheratura per la nitidezza per ogni componente di colore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>Imposta il livello di registro. Il valore predefinito è 1, che restituisce tutti i messaggi informativi, di avviso e di errore. Imposta su 0 per disabilitare tutti i messaggi tranne i messaggi di errore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -  <span class="varname"> soglia del  </span> <span class="varname"> raggio di  </span> <span class="varname"> raggio di usm  </span> </span> </p> </td> 
  <td class="stentry"> <p>Imposta i parametri di Maschera definizione dettagli. Ignorato se <span class="codeph"> -sharpen </span> è impostato su 0 o 1; obbligatorio se <span class="codeph"> -sharpen </span> è impostato su 2 o 3. <span class="varname"> amount  </span> è un valore reale compreso nell'intervallo 0.0...500.0,  <span class="varname"> radius  </span> è un valore reale nell'intervallo 0.0..10.0 e  <span class="varname"> soglia  </span> è un numero intero compreso tra 0 e 255. Per ulteriori informazioni, fare riferimento alla descrizione di <span class="codeph"> op_usm= </span> nella Guida di riferimento del protocollo Image Server . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Convalida che la vignetta specificata sia una vignetta di produzione corretta. <span class="varname"> ival  </span> rappresenta la versione minima del file della vignetta. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versione  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Versione del file di output. Se specificato, deve essere 0 o una versione di file di vignetta valida (non superiore alla versione predefinita del file). Se impostato su 0 o non specificato, il file di output viene creato utilizzando la versione più recente del file. Ignorato se è specificato <span class="codeph"> -info </span> . </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>Restituisce le informazioni sulla versione per questa utility. Specifica senza nome file e altre opzioni. </p> </td> 
 </tr> 
</table>

