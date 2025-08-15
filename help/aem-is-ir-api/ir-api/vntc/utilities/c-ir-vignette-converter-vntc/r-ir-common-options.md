---
title: Opzioni comuni
description: Le seguenti opzioni possono essere applicate indipendentemente dal tipo di sourceFile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# Opzioni comuni{#common-options}

Le seguenti opzioni possono essere applicate indipendentemente dal tipo di sourceFile.

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname"> stringa </span> </span> </p> </td> 
  <td class="stentry"> <p>Cartella in cui inserire i file di output (incluso il file di log, se <span class="codeph"> -log </span> è specificato). Può essere un percorso assoluto o relativo della directory di lavoro corrente. La gerarchia di cartelle viene creata se non esiste, ma non si applica al file specificato con <span class="codeph"> -log </span>. Se non specificato, i file di output vengono scritti nella cartella in cui si trova il file di origine <span class="varname"> di </span>. Se si specifica <span class="varname"> destFile </span>, verrà scritto sempre in tale posizione e <span class="codeph"> -destpath </span> verrà applicato solo ai file di output secondari. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -immagine </span> </p> </td> 
  <td class="stentry"> <p>Se è specificato, l'immagine della (prima) visualizzazione viene estratta dalla vignettatura, un'immagine del pannello adatta da uno stile di cabinet o la prima immagine di illuminazione di uno stile di copertura della finestra. L'immagine estratta viene salvata come file TIFF a risoluzione completa. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>Impedisce la generazione di file di destinazione. Utile per estrarre rapidamente gli attributi da un file di origine <span class="varname"> </span>. Vengono generate solo la miniatura facoltativa ( <span class="codeph"> -thumbwidth </span>), l'immagine ( <span class="codeph"> -image </span>) e i file di registro ( <span class="codeph"> -log </span>). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Seleziona la codifica JPEG con perdita di dati per RGB e dati immagine in scala di grigio incorporati nel file di output, invece di PNG senza perdita di dati. Le immagini con alfa (RGBA) vengono sempre salvate utilizzando la codifica PNG. <span class="varname"> ival </span> specifica la qualità JPEG (1...100); si consiglia 85 o superiore. Il valore predefinito è <span class="codeph"> -jpegquality 0 </span>, che seleziona la codifica PNG. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> percorso </span> </span> </p> </td> 
  <td class="stentry"> <p>Crea un file di registro con il percorso/nome specificato. I percorsi completi di tutti i file di output scritti nella cartella di destinazione vengono scritti nel file di log e alcune impostazioni aggiuntive, ad esempio le informazioni sulla versione ed eventuali avvisi o errori riscontrati (per ulteriori informazioni, vedere <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> output </a>). Nessun file di log creato se <span class="codeph"> -log </span> non è specificato; in questo caso, tutto l'output di testo viene scritto in <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - priorità più bassa <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Ridurre la priorità del processo <span class="filepath"> vntc </span>. È possibile utilizzare questo processo in modo che <span class="filepath"> vntc </span> non acquisisca un intero CPU durante l'elaborazione di una vignettatura. Consente al sistema operativo di dare più tempo ad altri processi, più importanti. <span class="varname"> ival </span> specifica la percentuale di priorità inferiore (0..100). Il valore predefinito è <span class="codeph"> -lowerpriority 0 </span>, che non riduce la priorità del processo <span class="filepath"> vntc </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Specificare la quantità massima di memoria che <span class="filepath"> vntc </span> può utilizzare in byte. Quando <span class="filepath"> vntc </span> raggiunge il limite massimo di memoria, l'elaborazione viene interrotta e viene generato un errore. Il flaconcino <span class="varname"> </span> specifica il limite massimo di memoria in byte (0.. 3.758.096.384 (3,5 GB). Quando <span class="varname"> ival </span> è 0, il limite massimo di memoria è disattivato. Il valore predefinito è <span class="codeph"> -maxmem 3221225472 </span>, ovvero un limite massimo di memoria di 3 GB. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separatore " <span class="varname"> stringa </span>" </span> </p> </td> 
  <td class="stentry"> <p>Specifica il separatore posizionato tra il nome del file e il suffisso di dimensione/risoluzione per i nomi di file di output generati automaticamente. Se non specificato, viene impostato automaticamente su "-". Ignorato se è specificato <span class="varname"> destFile </span> o <span class="codeph"> -info </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -contrasto <span class="varname"> flaconcino </span> </span> </p> </td> 
  <td class="stentry"> <p>Consente la nitidezza delle immagini ricampionate (ridimensionate) durante l'elaborazione. Applicabile solo alla nitidezza delle miniature nei file di tipo cabinet. </p> <p>Specificate 0 per disattivare la nitidezza (impostazione predefinita), 1 per attivare la nitidezza normale, 2 per attivare la maschera di contrasto solo per la luminosità o 3 per attivare la maschera di contrasto per ogni componente di colore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>Imposta il livello di registro. Il valore predefinito è 1, che restituisce tutti i messaggi informativi, di avvertenza e di errore. Imposta questo valore su 0 per disabilitare tutti i messaggi tranne quelli di errore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> importo </span> <span class="varname"> raggio </span> <span class="varname"> soglia </span> </span> </p> </td> 
  <td class="stentry"> <p>Imposta i parametri di maschera di contrasto. Ignorato se <span class="codeph"> -sharpen </span> è impostato su 0 o 1; obbligatorio se <span class="codeph"> -sharpen </span> è impostato su 2 o 3. L'importo <span class="varname"> </span> è un valore reale compreso nell'intervallo 0.0...500.0, il raggio <span class="varname"> </span> è un valore reale compreso nell'intervallo 0.0...10.0 e la soglia <span class="varname"> </span> è un numero intero compreso tra 0 e 255. Per ulteriori informazioni, consulta la descrizione di <span class="codeph"> op_usm= </span> nella documentazione di riferimento del protocollo Image Server. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Verifica che la vignettatura specificata sia una vignettatura di produzione corretta. Il flaconcino <span class="varname"> di </span> rappresenta la versione file minima della vignettatura. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versione <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>Versione del file di output. Se è specificato, deve essere 0 o una versione valida del file di vignettatura (non superiore alla versione predefinita del file). Se è impostato su 0 o non è specificato, il file di output viene creato utilizzando la versione del file più recente. Ignorato se è specificato <span class="codeph"> -info </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> - informazioni sulla versione </span> </p> </td> 
  <td class="stentry"> <p>Restituisce le informazioni sulla versione di questa utility. Specificare senza nome file e altre opzioni. </p> </td> 
 </tr> 
</table>
