---
description: Utility di convalida delle immagini. Questa utilità da riga di comando verifica i file immagine per verificare che siano validi e possano essere letti senza difficoltà da Image Server.
solution: Experience Manager
title: convalida
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# convalida{#validate}

Utility di convalida delle immagini. Questa utilità da riga di comando verifica i file immagine per verificare che siano validi e possano essere letti senza difficoltà da Image Server.

Tutti i file di immagine non PTIFF devono passare la convalida prima che il file sia reso disponibile a Image Server come immagine sorgente. Le immagini PTIFF devono essere convalidate dopo operazioni di copia potenzialmente inaffidabili.

## Utilizzo {#usage}

` validate *`fileType`* [ *`opzioni`*] [ *`sourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -qualsiasi </span> </p> <p>Tipo di file di origine; è necessario specificarne almeno uno (-any consente gli stessi tipi di file di immagine supportati da IC). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> opzioni </span> </span> </p> </td> 
  <td class="stentry"> <p>Altre opzioni di comando (vedere di seguito). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile </span> </span> </p> </td> 
  <td class="stentry"> <p> File di immagine. Nessuno o più, separati da spazi. </p> </td> 
 </tr> 
</table>

## Restituisce {#section-67a7cf7c53144fbb8f24b818f4a10901}

0 in caso di esito positivo. Se si verifica un errore, viene restituito un valore diverso da zero e i dettagli dell’errore vengono inviati a `stderr`.

## Opzioni {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>Specifica un file di testo separato contenente l'elenco dei file di immagine. Un record per file. Se <span class="codeph"> -fileList </span> è incluso, <span class="varname"> sourceFile </span> non deve essere specificato. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>Abilita la verifica dell'intero file di immagine. Per impostazione predefinita, viene convalidata solo l’intestazione dell’immagine. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>Verifica la validità del profilo colore incorporato. Per impostazione predefinita, il corpo del profilo non è selezionato. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -rejected16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> Rifiuta le immagini con 16 bit per componente immagine. Sempre specificato dal server immagini durante la convalida delle immagini di origine remota. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verboso </span> </p> </td> 
  <td class="stentry"> <p> Stampa ulteriori informazioni se l'immagine non è valida. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -muto </span> </p> </td> 
  <td class="stentry"> <p>Disabilita <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> output. Viene restituito solo uno stato. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>Termina l’elaborazione quando si verifica un errore di convalida del file, anche se i file aggiuntivi non sono ancora stati convalidati. Per impostazione predefinita, l’elaborazione continua quando si verifica un errore di convalida </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version </span> </p> </td> 
  <td class="stentry"> <p>Restituisce le informazioni sulla versione di questa utility. Specifica senza altre opzioni. </p> </td> 
 </tr> 
</table>
