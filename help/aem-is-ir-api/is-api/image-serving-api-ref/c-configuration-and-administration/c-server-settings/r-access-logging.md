---
description: Utilizzare queste impostazioni server per l'accesso di registrazione.
solution: Experience Manager
title: Registrazione degli accessi
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: e677a617-115d-4f6e-9eb5-bdc14ad7ff24
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '674'
ht-degree: 1%

---

# Registrazione degli accessi{#access-logging}

Utilizzare queste impostazioni server per l&#39;accesso di registrazione.

Sintassi

## TC::directory - Cartella file di registro {#section-5d9e2168d4504bbe9868b7d6051c9d67}

Cartella in cui è memorizzato [!DNL Platform Server] scrive i file di registro. Può essere un percorso assoluto o un percorso relativo a *`install_folder`*. Il valore predefinito è [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>È necessario creare la nuova cartella prima di modificare questa impostazione. Se Image Server è installato per l&#39;esecuzione con un account utente diverso da root, verificare che la cartella disponga dei privilegi di accesso in lettura e scrittura corretti.

## TC::maxDays - Numero di giorni per la conservazione dei file di registro {#section-45cbecffc5694c87b7d5c176a44a4885}

Il numero di file di registro dei giorni deve essere mantenuto. I nuovi file di registro vengono creati ogni giorno a mezzanotte. A questo punto, il server eliminerà tutti i file nella cartella dei file di registro che sono stati creati da un numero di giorni superiore a quello specificato, inclusi quelli scritti dal server immagini o dal server di rendering. Il valore predefinito è 10.

## TC::prefix - Nome file log di accesso {#section-1003856323b844049632710a5a056aa7}

Prefisso del nome del file in cui vengono scritti i dati del log degli accessi. La data e il suffisso del file ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]) alla stringa specificata. Il nome del file di log degli accessi deve essere diverso da quello del file di log di traccia. Il valore predefinito è &quot; `access-`&quot;.

## TC::pattern - Schema log degli accessi {#section-22775ea85cee444d8a7d7336a3b1feef}

Specifica il pattern di dati per [!DNL Platform Server] accedere ai record del registro. La stringa di pattern specifica le variabili che vengono sostituite con i valori corrispondenti. Tutti gli altri caratteri nella stringa pattern vengono trasferiti letteralmente nel record di registro.

Per utilizzare l&#39;utilità di riscaldamento della cache, è necessario utilizzare gli spazi come separatori di campo. Il [!DNL Platform Server] sostituisce tutti gli spazi e i caratteri &#39;%&#39; nei valori dei campi con `%20` e `%25`, rispettivamente.

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
   <td> <p>Numero di byte di risposta escluse le intestazioni HTTP oppure "" se zero. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Numero di byte di risposta escluse le intestazioni HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>Tempo di elaborazione delle richieste in millisecondi. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I </span> </p> </td> 
   <td> <p>id thread (per riferimenti incrociati a voci di registro di debug/errori). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>data e ora, formattate come <span class="codeph"> <span class="varname"> aaaa </span>- <span class="varname"> MM </span>- <span class="varname"> gg </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> SSS </span> offset </span> </p> <p> ( <span class="varname"> SSS </span> sono msec, <span class="varname"> offset </span> è l’offset orario GMT); il valore temporale viene acquisito quando la risposta viene inviata al client. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %m </span> </p> </td> 
   <td> <p>Metodo di richiesta ( <span class="codeph"> GET </span>, <span class="codeph"> POST </span>e così via). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %O </span> </p> </td> 
   <td> <p>Sovrapposizione delle richieste (numero di richieste elaborate contemporaneamente). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %p </span> </p> </td> 
   <td> <p>Porta locale su cui è stata ricevuta la richiesta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q </span> </p> </td> 
   <td> <p>Stringa di query (preceduta da un "?" se esiste). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %r </span> </p> </td> 
   <td> <p>Prima riga della richiesta (metodo di richiesta, URI, versione HTTP). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R </span> </p> </td> 
   <td> <p>Uguale a <span class="codeph"> %r </span>, ma applica una codifica HTTP limitata all’URI per evitare problemi di analisi del registro. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %s </span> </p> </td> 
   <td> <p>Codice stato risposta HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %S </span> </p> </td> 
   <td> <p>ID sessione utente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %t </span> </p> </td> 
   <td> <p>Data e ora, nel formato di registro comune. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %u </span> </p> </td> 
   <td> <p>Utente remoto autenticato (se presente), altrimenti "". </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %U </span> </p> </td> 
   <td> <p>Percorso URI. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %v </span> </p> </td> 
   <td> <p>Nome server locale. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %T </span> </p> </td> 
   <td> <p>Tempo di elaborazione della richiesta in secondi. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheKey}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] chiave cache (nome/cartella file cache). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r </span> </p> </td> 
   <td> <p>[!DNL Platform Server] parola chiave di gestione cache: <span class="codeph"> { RIUTILIZZATO | CREATO | AGGIORNATO | REMOTO | CREATO_IN_REMOTO | AGGIORNATO_IN_REMOTO | CACHE_REMOTA | CONVALIDATO | IGNORATO | NON DEFINITO } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r </span> </p> </td> 
   <td> <p>Il tipo MIME di risposta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>Contesto di destinazione se si verifica un inoltro del contesto. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r </span> </p> </td> 
   <td> <p>Il <span class="codeph"> etag </span> valore dell’intestazione di risposta (firma MD5 dei dati di risposta). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r </span> </p> </td> 
   <td> <p>Messaggio di errore </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r </span> </p> </td> 
   <td> <p>Tempo impiegato per recuperare la voce della cache o i dati dal server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r </span> </p> </td> 
   <td> <p>Tempo impiegato per l'analisi delle richieste e la ricerca nel catalogo immagini. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r </span> </p> </td> 
   <td> <p>Indica se la richiesta ha tentato o meno di accedere in base al percorso all'esterno del sistema di catalogo. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r </span> </p> </td> 
   <td> <p>Indirizzo IP del server peer nel cluster di cache che ha recapitato la voce della cache o "-" se <span class="codeph"> CacheUse </span> non è né <span class="codeph"> REMOTE_CREATED </span> né <span class="codeph"> AGGIORNATO_IN_REMOTO </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r </span> </p> </td> 
   <td> <p>Categoria errore: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=nessun errore. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=immagine/e non trovata/e sul server. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=Errore di utilizzo del protocollo IS o errore di contenuto diverso da 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=altro errore del server. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=richiesta rifiutata a causa di un sovraccarico temporaneo del server. </p> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ReqType}r </span> </p> </td> 
   <td> <p>Il valore maiuscolo di <span class="codeph"> req= </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{RootId}r </span> </p> </td> 
   <td> <p>ID principale del catalogo principale della richiesta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{SendTime}r </span> </p> </td> 
   <td> <p>Il tempo necessario [!DNL Platform Server] per inviare una risposta dopo la scrittura dei dati nel flusso di output. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r </span> </p> </td> 
   <td> <p>Mi piace <span class="codeph"> %B </span>, ma include i valori per le risposte 304 (non modificate). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformedUrl}r </span> </p> </td> 
   <td> <p>L’URL finale dopo tutte le trasformazioni del set di regole. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpRequestHeader </span>}i </span> </p> </td> 
   <td> <p>Il valore dell’intestazione di richiesta HTTP specificata. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ <span class="varname"> httpResponseHeader </span>} </span> </p> </td> 
   <td> <p>Il valore dell’intestazione di risposta HTTP specificata. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il valore predefinito è `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
