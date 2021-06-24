---
description: Utilizza queste impostazioni del server per accedere alla registrazione.
solution: Experience Manager
title: Registrazione degli accessi
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 2%

---

# Registrazione degli accessi{#access-logging}

Utilizza queste impostazioni del server per accedere alla registrazione.

Sintassi

## TC::directory - Cartella file di registro {#section-5d9e2168d4504bbe9868b7d6051c9d67}

La cartella in cui il server Platform scrive i file di registro. Può essere un percorso assoluto o un percorso relativo a *`install_folder`*. Il valore predefinito è [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>È necessario creare la nuova cartella prima di modificare questa impostazione. Assicurati che la cartella disponga dei privilegi di accesso in lettura/scrittura corretti se Image Server è installato per l&#39;esecuzione in un account utente diverso dalla radice.

## TC::maxDays - Numero di giorni per mantenere i file di registro {#section-45cbecffc5694c87b7d5c176a44a4885}

È necessario mantenere il numero di giorni di file di registro. I nuovi file di registro vengono creati ogni giorno a mezzanotte. Al momento, il server eliminerà tutti i file presenti nella cartella del file di registro che sono più vecchi del numero specificato di giorni, inclusi quelli scritti dal server di immagini o dal server di rendering. Il valore predefinito è 10.

## TC::prefisso - Nome file di log di accesso {#section-1003856323b844049632710a5a056aa7}

Prefisso nome per il file in cui vengono scritti i dati del registro di accesso. Alla stringa specificata vengono aggiunte la data e il suffisso del file ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]). Il nome del file di log di accesso deve essere diverso da quello del file di log di traccia. Il valore predefinito è &quot; `access-`&quot;.

## TC::pattern - Access Log Pattern {#section-22775ea85cee444d8a7d7336a3b1feef}

Specifica il pattern di dati per i record di log di accesso di Platform Server. La stringa del pattern specifica le variabili che vengono sostituite con i relativi valori corrispondenti. Tutti gli altri caratteri nella stringa di pattern vengono letteralmente trasferiti nel record di log.

Per utilizzare l&#39;utilità di riscaldamento della cache, gli spazi devono essere utilizzati come separatori di campo. Il server della piattaforma sostituisce tutti gli spazi e i caratteri &#39;%&#39; nei valori dei campi rispettivamente con `%20` e `%25`.

Sono supportate le seguenti variabili di pattern:

<table id="table_7A07AFF34B5040A5B30F5735CFE9428F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Pattern</b> </th> 
   <th class="entry"> <b>Descrizione</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> %a </span> </p> </td> 
   <td> <p>Indirizzo IP remoto. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %A </span> </p> </td> 
   <td> <p>Indirizzo IP locale. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %b </span> </p> </td> 
   <td> <p>Numero di byte di risposta escludendo le intestazioni HTTP o ' ' se zero. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Numero di byte di risposta escludendo le intestazioni HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>Tempo di elaborazione della richiesta in millisecondi. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I  </span> </p> </td> 
   <td> <p>id thread (per riferimenti incrociati alle voci di registro debug/errore). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>data e ora, formattate come <span class="codeph"> <span class="varname"> aaaa </span>- <span class="varname"> MM </span>- <span class="varname"> gg </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> Offset SSS  </span>   </span> </p> <p> ( <span class="varname"> SSS </span> sono msec, <span class="varname"> offset </span> è l'offset orario GMT); il valore temporale viene acquisito quando la risposta viene inviata al client. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>Metodo di richiesta ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span> e così via). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O  </span> </p> </td> 
   <td> <p>Sovrapposizione delle richieste (numero di richieste elaborate contemporaneamente). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p  </span> </p> </td> 
   <td> <p>Porta locale in cui è stata ricevuta la richiesta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q  </span> </p> </td> 
   <td> <p>Stringa query (anteposta a '?' se esiste). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %l </span> </p> </td> 
   <td> <p>Prima riga della richiesta (metodo di richiesta, URI, versione HTTP). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R  </span> </p> </td> 
   <td> <p>Come <span class="codeph"> %r </span>, ma applica una codifica HTTP limitata all’URI per evitare problemi di analisi del registro. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s  </span> </p> </td> 
   <td> <p>Codice di stato della risposta HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S  </span> </p> </td> 
   <td> <p>ID sessione utente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t  </span> </p> </td> 
   <td> <p>Data e ora, in formato registro comune. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u  </span> </p> </td> 
   <td> <p>Utente remoto autenticato (se presente), else ''. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U  </span> </p> </td> 
   <td> <p>Percorso URI. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v  </span> </p> </td> 
   <td> <p>Nome server locale. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T  </span> </p> </td> 
   <td> <p>Richiedi tempo di elaborazione in secondi. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r  </span> </p> </td> 
   <td> <p>Chiave della cache del server di Platform (cartella/nome del file della cache). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r  </span> </p> </td> 
   <td> <p>Parola chiave di gestione della cache del server della piattaforma: <span class="codeph"> { REUSED | CREATO | AGGIORNATO | REMOTO | REMOTE_CREATED | REMOTE_AGGIORNATO | REMOTE_CACHE | CONVALIDATO | IGNORATO | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r  </span> </p> </td> 
   <td> <p>Il tipo MIME della risposta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>Il contesto di destinazione in caso di inoltro del contesto. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r  </span> </p> </td> 
   <td> <p>Valore dell'intestazione di risposta <span class="codeph"> etag </span> (firma MD5 dei dati di risposta). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r  </span> </p> </td> 
   <td> <p>Messaggio di errore. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r  </span> </p> </td> 
   <td> <p>Tempo impiegato per recuperare la voce della cache o i dati da Image Server. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r  </span> </p> </td> 
   <td> <p>Tempo impiegato per l’analisi delle richieste e la ricerca nel catalogo delle immagini. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r  </span> </p> </td> 
   <td> <p>Indica se questa richiesta ha tentato o meno un accesso basato su percorsi all'esterno del sistema di catalogo. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r  </span> </p> </td> 
   <td> <p>Indirizzo IP del server peer nel cluster di cache che ha consegnato la voce di cache o "-" se <span class="codeph"> CacheUse </span> non è <span class="codeph"> REMOTE_CREATED </span> né <span class="codeph"> REMOTE_UPDATED </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r  </span> </p> </td> 
   <td> <p>Categoria errore: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=nessun errore. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=immagini non trovate sul server. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=Errore di utilizzo del protocollo IS o errore di contenuto diverso da 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=altro errore del server. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=richiesta rifiutata a causa di sovraccarico temporaneo del server. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r  </span> </p> </td> 
   <td> <p>Il valore maiuscolo di <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r  </span> </p> </td> 
   <td> <p>ID radice del catalogo principale della richiesta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r  </span> </p> </td> 
   <td> <p>Tempo necessario a Platform Server per inviare la risposta dopo la scrittura dei dati nel flusso di output. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r  </span> </p> </td> 
   <td> <p>Come <span class="codeph"> %B </span>, ma include valori per risposte 304 (non modificate). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformationUrl}r  </span> </p> </td> 
   <td> <p>L’URL finale dopo tutte le trasformazioni del set di regole. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpRequestHeader  </span>}i  </span> </p> </td> 
   <td> <p>Il valore dell'intestazione di richiesta HTTP specificata. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpResponseHeader  </span>}  </span> </p> </td> 
   <td> <p>Il valore dell'intestazione di risposta HTTP specificata. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il valore predefinito è `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
