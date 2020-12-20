---
description: Le seguenti opzioni possono essere applicate indipendentemente dal tipo di sourceFile.
seo-description: Le seguenti opzioni possono essere applicate indipendentemente dal tipo di sourceFile.
seo-title: Opzioni comuni
solution: Experience Manager
title: Opzioni comuni
topic: Scene7 Image Serving - Image Rendering API
uuid: fdf09873-4102-4ed6-a315-a87cba5c44c7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '670'
ht-degree: 0%

---


# Opzioni comuni{#common-options}

Le seguenti opzioni possono essere applicate indipendentemente dal tipo di sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath,  <span class="varname"> stringa  </span> </span> </p> </td> 
  <td class="stentry"> <p>Cartella in cui devono essere inseriti i file di output (incluso il file di registro, se è specificato <span class="codeph"> -log </span>). Può essere un percorso assoluto o relativo alla directory di lavoro corrente. La gerarchia delle cartelle verrà creata se non esiste. Non si applica al file specificato con <span class="codeph"> -log </span>. Se non viene specificato, i file di output vengono scritti nella cartella in cui si trova <span class="varname"> sourceFile </span>. Se <span class="varname"> destFile </span> è specificato, sarà sempre scritto in quella posizione, e <span class="codeph"> -destpath </span> si applica solo ai file di output secondari. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -image  </span> </p> </td> 
  <td class="stentry"> <p>Se specificato, la (prima) immagine di visualizzazione viene estratta dalla vignettatura, un’immagine di pannello adatta da uno stile di cabinet o la prima immagine di illuminazione di uno stile di copertura della finestra. L’immagine estratta viene salvata come file TIFF a risoluzione completa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Impedisce la generazione dei file di destinazione. Utile per estrarre rapidamente gli attributi da <span class="varname"> sourceFile </span>. Vengono generati solo le miniature facoltative ( <span class="codeph"> -thumbnail </span>), le immagini ( <span class="codeph"> -image </span>) e i file di registro ( <span class="codeph"> -log </span>). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Seleziona la codifica JPEG con perdita di dati per RGB e i dati immagine in scala di grigio incorporati nel file di output, invece del file PNG senza perdita di dati. Le immagini con alfa (RGBA) vengono sempre salvate con la codifica PNG. <span class="varname"> ival  </span> specifica la qualità JPEG (1...100); Si consiglia 85 o superiore. Il valore predefinito è <span class="codeph"> -jpegquality 0 </span>, che seleziona la codifica PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log  <span class="varname"> path  </span> </span> </p> </td> 
  <td class="stentry"> <p>Crea un file di registro con il percorso/nome specificato. I percorsi completi di tutti i file di output scritti nella cartella di destinazione vengono scritti nel file di registro, nonché alcune impostazioni aggiuntive, come informazioni sulla versione e eventuali avvertenze o errori riscontrati (vedere <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> Output </a> per i dettagli). Non viene creato alcun file di registro se <span class="codeph"> -log </span> non è specificato; in questo caso, tutto l'output di testo viene scritto in <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> Festival con priorità inferiore  </span> </span> </p> </td> 
  <td class="stentry"> <p>Ridurre la priorità del processo <span class="filepath"> vntc </span>. Questo può essere utilizzato in modo che <span class="filepath"> vntc </span> non occupi un'intera CPU durante l'elaborazione di una vignettatura. Consente al sistema operativo di dare più tempo ad altri, più importanti, processi. <span class="varname"> ival  </span> specifica la percentuale di priorità inferiore (0.100). Il valore predefinito è <span class="codeph"> -lowerpriority 0 </span>, che non riduce la priorità del processo <span class="filepath"> vntc </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Specificate la quantità massima di memoria che <span class="filepath"> vntc </span> può utilizzare in byte. Quando <span class="filepath"> vntc </span> raggiunge il limite massimo di memoria, l'elaborazione si interrompe e si verifica un errore. <span class="varname"> ival  </span> specifica il limite massimo di memoria in byte (0.. 3.758.096.384 (3,5 GB). Quando <span class="varname"> ival </span> è 0, il limite massimo di memoria è disattivato. Il valore predefinito è <span class="codeph"> -maxmem 3221225472 </span>, ovvero un limite massimo di memoria di 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator "  <span class="varname"> string  </span>"  </span> </p> </td> 
  <td class="stentry"> <p>Specifica il separatore posizionato tra il nome del file e il suffisso dimensione/risoluzione per i nomi dei file di output generati automaticamente. Se non viene specificato, il valore predefinito è "-". Ignorato se è specificato <span class="varname"> destFile </span> o <span class="codeph"> -info </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -sharpen  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Abilita la nitidezza delle immagini ricampionate (ridimensionate) durante l’elaborazione. Si applica solo alla nitidezza delle miniature nel caso di file di stile cabinet. </p> <p>Specificate 0 per disattivare la nitidezza (impostazione predefinita), 1 per attivare la nitidezza normale, 2 per attivare la maschera di contrasto solo per la luminosità, 3 per attivare la maschera di contrasto per ciascun componente di colore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>Imposta il livello di registro. Il valore predefinito è 1, che genera tutti i messaggi informativi, di avviso e di errore. Impostare su 0 per disabilitare tutti i messaggi tranne quelli di errore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - <span class="varname"> soglia  </span> <span class="varname"> raggio  </span> <span class="varname"> raggio importo usm  </span> </span> </p> </td> 
  <td class="stentry"> <p>Imposta i parametri di maschera di contrasto. Ignorato se <span class="codeph"> -sharpen </span> è impostato su 0 o 1; obbligatorio se <span class="codeph"> -sharpen </span> è impostato su 2 o 3. <span class="varname"> amount  </span> è un valore reale compreso nell'intervallo 0.0...500.0,  <span class="varname"> radius  </span> è un valore reale nell'intervallo 0.0...10.0, e  <span class="varname"> threshold  </span> è un numero intero compreso tra 0 e 255. Per ulteriori informazioni, fare riferimento alla descrizione di <span class="codeph"> op_usm= </span> nella Guida di riferimento del protocollo Image Server. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Convalidare che la vignettatura specificata sia una vignettatura di produzione corretta. <span class="varname"> ival  </span> rappresenta la versione minima del file della vignettatura. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>Versione del file per il file di output. Se specificato, deve essere 0 o una versione di file di vignettatura valida (non superiore alla versione predefinita del file). Se impostato su 0 o non specificato, il file di output viene creato utilizzando la versione del file più recente. Ignorato se è specificato <span class="codeph"> -info </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>Restituisce le informazioni sulla versione per questa utility. Specificate senza nome file e altre opzioni. </p> </td> 
 </tr> 
</table>

