---
description: L'utility playlog può essere utilizzata per generare anticipatamente i contenuti per la cache di risposta HTTP.
solution: Experience Manager
title: Utility 'playlog'
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# Utility &#39;playlog&#39;{#the-playlog-utility}

L&#39;utility playlog può essere utilizzata per generare anticipatamente i contenuti per la cache di risposta HTTP.

La cache di risposta HTTP Image Server esistente non è garantita utilizzabile dopo un aggiornamento della versione principale (quando cambia la prima o la seconda cifra del numero di versione). Se il server deve essere portato in tempo reale in condizioni di pieno carico dopo l&#39;aggiornamento, il server potrebbe essere sovraccaricato per gestire le prime ore di richieste di mancata cache fino a quando la cache non viene compilata ragionevolmente e la frequenza di hit della cache aumenta.

Per evitare questo picco di caricamento iniziale, l’ `playlog` utilità può essere utilizzata per pregenerare il contenuto per la cache di risposta HTTP. `playlog` estrae le richieste HTTP da un file di registro di accesso esistente e lo invia al server per generare le voci di cache. Per gli scenari di utilizzo tipici, è sufficiente riprodurre un singolo file di log di accesso contenente un valore di traffico giornaliero completo.

Oltre a attivare la cache di risposta HTTP dopo l’installazione dell’aggiornamento, l’utility viene utilizzata anche per pregenerare il contenuto della cache quando si aggiunge un nuovo server a un ambiente con bilanciamento del carico; è sufficiente riprodurre un file di registro recente da uno degli altri server.

`playlog` può essere configurato per supportare la maggior parte dei file di log di accesso generati dalle versioni precedenti di Image Server.

## Utilizzo {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p  <span class="varname"> prefisso  </span> </span> </p> </td> 
  <td class="stentry"> <p>URL principale da anteporre alle richieste estratte dal file di registro. </p> <p>Predefinito: <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n  <span class="varname"> col  </span> </span> </p> </td> 
  <td class="stentry"> <p>numero del campo (colonna) che contiene la richiesta nel record del registro; basato su 1. </p> <p>Predefinito: 16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s  <span class="varname"> separatore  </span> </span> </p> </td> 
  <td class="stentry"> <p>Separatore di campo; pattern di espressione regolare. </p> <p>Predefinito: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m  <span class="varname"> marker  </span> </span> </p> </td> 
  <td class="stentry"> <p>marcatore di richiesta; identifica nel file di log le richieste da riprodurre; pattern di espressione regolare. </p> <p>Predefinito: <span class="codeph"> Richiesta: </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> Suffisso -x  <span class="varname">   </span> </span> </p> </td> 
  <td class="stentry"> <p>Suffisso da aggiungere alla richiesta estratta dal file di registro; può essere utilizzato per separare le richieste di riproduzione dalle richieste live nei file di log; un '?' o il separatore '&amp;' viene inserito automaticamente; il suffisso può fare riferimento a qualsiasi campo di registro per posizione all’interno delle parentesi graffe, il valore predefinito corrisponde al campo firma md5. </p> <p>Predefinito: <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v  </span> </p> </td> 
  <td class="stentry"> <p>In modalità dettagliata, stampa gli URL della richiesta generati in <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p>Stampa una sinossi su <span class="codeph"> stdout </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -l </span> </p> </td> 
  <td class="stentry"> <p>request-method - metodo di richiesta HTTP da utilizzare ( <span class="codeph"> get|post|head|smart </span>). </p> <p>Predefinito: <span class="codeph"> smart </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o  </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos nel file di log per recuperare il metodo originale da. </p> <p>Predefinito: 15 </p> </td> 
 </tr> 
</table>

Per Windows, il nome del file è [!DNL playlog.bat] e su Linux è [!DNL playlog.sh].

## Esempi {#section-716e5c35e9fa4ee3a4b0687381fcea40}

L&#39;esempio seguente riproduce tutte le richieste da un file di log di accesso creato da Image Serving su Linux:

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

Il seguente comando riproduce tutte le richieste trovate in un file di log di traccia creato da Image Server su Windows:

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
