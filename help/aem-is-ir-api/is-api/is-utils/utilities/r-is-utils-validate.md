---
description: Utilità di convalida immagine. Questa utilità della riga di comando verifica i file immagine per assicurarsi che siano validi e che possano essere letti senza difficoltà da Image Serving.
solution: Experience Manager
title: validate
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 0%

---


# validate{#validate}

Utilità di convalida immagine. Questa utilità della riga di comando verifica i file immagine per assicurarsi che siano validi e che possano essere letti senza difficoltà da Image Serving.

Tutti i file immagine non PTIFF devono passare la convalida prima che il file sia reso disponibile ad Image Serving come immagine sorgente. Le immagini PTIFF devono essere convalidate dopo operazioni di copia potenzialmente inaffidabili.

## Utilizzo {#usage}

` validate *``* [ *``*] [ *`fileTypeoptionssourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any  </span> </p> <p>Tipo di file di origine; è necessario specificarne almeno uno (-any consente gli stessi tipi di file immagine supportati da IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> options  </span> </span> </p> </td> 
  <td class="stentry"> <p>Altre opzioni di comando (vedere di seguito). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> File immagine. Nessuno o più, separati da spazi. </p> </td> 
 </tr> 
</table>

## Restituisce {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 in caso di esito positivo. Se si verifica un errore, viene restituito un valore diverso da zero e i dettagli dell&#39;errore vengono inviati a `stderr`.

## Opzioni {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>Specifica un file di testo separato contenente l’elenco dei file di immagine. Un record per file. Se <span class="codeph"> -fileList </span> è incluso, <span class="varname"> sourceFile </span> non deve essere specificato. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>Abilita la verifica dell'intero file immagine. Per impostazione predefinita, viene convalidata solo l’intestazione dell’immagine. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>Verifica la validità del profilo colore incorporato. Per impostazione predefinita, il corpo del profilo non è selezionato. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -deny16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> Rifiuta le immagini con 16 bit per componente immagine. Sempre specificato dal server immagini quando convalida le immagini di origine remota. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verboso  </span> </p> </td> 
  <td class="stentry"> <p> Stampa ulteriori informazioni se l'immagine non è valida. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silenzioso  </span> </p> </td> 
  <td class="stentry"> <p>Disabilita l'output <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>. Viene restituito solo uno stato. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>Termina l’elaborazione quando si verifica un errore di convalida del file, anche se i file aggiuntivi devono ancora essere convalidati. Per impostazione predefinita, l’elaborazione continua quando si verifica un errore di convalida </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  </span> </p> </td> 
  <td class="stentry"> <p>Restituisce le informazioni sulla versione per questa utility. Specifica senza altre opzioni. </p> </td> 
 </tr> 
</table>

