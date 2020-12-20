---
description: L'utility playlog può essere utilizzata per generare preventivamente il contenuto per la cache delle risposte HTTP.
seo-description: L'utility playlog può essere utilizzata per generare preventivamente il contenuto per la cache delle risposte HTTP.
seo-title: L'utilità 'playlog'
solution: Experience Manager
title: L'utilità 'playlog'
topic: Scene7 Image Serving - Image Rendering API
uuid: 9044515e-7cfb-4e86-9ac4-e071b60f38d1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 0%

---


# Utility &#39;playlog&#39;{#the-playlog-utility}

L&#39;utility playlog può essere utilizzata per generare preventivamente il contenuto per la cache delle risposte HTTP.

La cache delle risposte HTTP Image Server esistente non è garantita e può essere utilizzata dopo un aggiornamento della versione principale (quando cambia la prima o la seconda cifra del numero di versione). Se il server deve essere portato live in condizioni di pieno carico dopo l&#39;aggiornamento, il server potrebbe essere sovraccarico nel gestire le prime ore di richieste di cache non riuscite fino a quando la cache non viene popolata in modo ragionevole e il tasso di hit della cache aumenta.

Per evitare questo picco di caricamento iniziale, l&#39;utility `playlog` può essere utilizzata per generare preventivamente il contenuto per la cache delle risposte HTTP. `playlog` estrae le richieste HTTP da un file di registro di accesso esistente e le invia al server per generare le voci della cache. Per gli scenari di utilizzo tipici, è sufficiente riprodurre un singolo file di registro di accesso contenente il valore del traffico di un giorno intero.

Oltre a attivare la cache delle risposte HTTP dopo l’installazione dell’aggiornamento, l’utility viene utilizzata anche per pregenerare il contenuto della cache quando si aggiunge un nuovo server a un ambiente con bilanciamento del carico; è sufficiente riprodurre un file di registro recente da uno degli altri server.

`playlog` può essere configurato per supportare la maggior parte dei file di registro di accesso generati dalle versioni precedenti di Image Server.

## Utilizzo {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p  <span class="varname"> prefix  </span> </span> </p> </td> 
  <td class="stentry"> <p>URL principale per anteporre alle richieste estratte dal file di registro. </p> <p>Predefinito: <span class="filepath"> http://localhost:8080/is </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>Numero del campo (colonna) che contiene la richiesta nel record del registro; Basato su 1. </p> <p>Predefinito: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s  <span class="varname"> separatore  </span> </span> </p> </td> 
  <td class="stentry"> <p>separatore di campo; pattern di espressione regolare. </p> <p>Predefinito: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m  <span class="varname"> marker  </span> </span> </p> </td> 
  <td class="stentry"> <p>Indicatore della richiesta; identifica nel file di registro le richieste da riprodurre; pattern di espressione regolare. </p> <p>Predefinito: <span class="codeph"> Richiesta: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x  <span class="varname"> suffisso  </span> </span> </p> </td> 
  <td class="stentry"> <p>Suffisso da aggiungere alla richiesta estratta dal file di registro; può essere utilizzato per separare le richieste di riproduzione dalle richieste live nei file di registro; un '?' o il separatore '&amp;' viene inserito automaticamente; il suffisso può fare riferimento a qualsiasi campo di registro per posizione all’interno delle parentesi graffe; il valore predefinito corrisponde al campo firma md5. </p> <p>Predefinito: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v  </span> </p> </td> 
  <td class="stentry"> <p>In modalità dettagliata, stampa gli URL di richiesta generati su <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p>Stampare una sinossi su <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -l </span> </p> </td> 
  <td class="stentry"> <p>request-method - Metodo di richiesta HTTP da utilizzare ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Predefinito: <span class="codeph"> smart </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o  </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos nel file di registro per acquisire il metodo originale. </p> <p>Predefinito: 15 </p> </td> 
 </tr> 
</table>

Per Windows, il nome del file è [!DNL playlog.bat] e in Linux è [!DNL playlog.sh].

## Esempi {#section-716e5c35e9fa4ee3a4b0687381fcea40}

L&#39;esempio seguente riproduce tutte le richieste provenienti da un file di registro di accesso creato da Image Server su Linux:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

Il seguente comando riproduce tutte le richieste rilevate in un file di registro di traccia creato da Image Server in Windows:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
