---
description: Utilizzate queste impostazioni del server per l'accesso all'accesso all'accesso.
seo-description: Utilizzate queste impostazioni del server per l'accesso all'accesso all'accesso.
seo-title: Accesso
solution: Experience Manager
title: Accesso
topic: Scene7 Image Serving - Image Rendering API
uuid: ea7d5d39-3f0a-45f0-bc28-6828a9c9da50
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 2%

---


# Accesso{#access-logging}

Utilizzate queste impostazioni del server per l&#39;accesso all&#39;accesso all&#39;accesso.

Sintassi

## TC::directory - Cartella file di registro {#section-5d9e2168d4504bbe9868b7d6051c9d67}

La cartella in cui il server piattaforma scrive i file di registro. Può trattarsi di un percorso assoluto o di un percorso relativo a *`install_folder`*. Il valore predefinito è [!DNL  *`install_folder`*/logs].

>[!NOTE]
>
>Prima di modificare questa impostazione è necessario creare la nuova cartella. Se Image Server è installato per essere eseguito con un account utente diverso da root, verificate che la cartella disponga dei privilegi di accesso in lettura/scrittura corretti.

## TC::maxDays - Numero di giorni per mantenere i file di registro {#section-45cbecffc5694c87b7d5c176a44a4885}

È necessario mantenere il numero di giorni di file di registro. I nuovi file di registro vengono creati ogni giorno a mezzanotte. Al momento, il server elimina tutti i file presenti nella cartella del file di registro che hanno una durata superiore al numero specificato di giorni, inclusi quelli scritti dal server immagini o dal server di rendering. Il valore predefinito è 10.

## TC::prefix - Nome file di registro di accesso {#section-1003856323b844049632710a5a056aa7}

Prefisso nome per il file in cui vengono scritti i dati del registro di accesso. Alla stringa specificata vengono aggiunti la data e il suffisso del file ( [!DNL  *`yyyy`*-*`mm`*-*`dd`*.log]). Il nome del file di registro di accesso deve essere diverso da quello del file di registro di traccia. Il valore predefinito è &quot; `access-`&quot;.

## TC::pattern - Access Log Pattern {#section-22775ea85cee444d8a7d7336a3b1feef}

Specifica il pattern di dati per i record di registro di accesso di Platform Server. La stringa pattern specifica le variabili che vengono sostituite con i valori corrispondenti. Tutti gli altri caratteri nella stringa del pattern vengono letteralmente trasferiti nel record di registro.

Per utilizzare l&#39;utilità di riscaldamento della cache, gli spazi devono essere utilizzati come separatori di campo. Il server piattaforme sostituisce tutti gli spazi e i caratteri &#39;%&#39; nei valori dei campi con `%20` e `%25`, rispettivamente.

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
   <td> <p>Numero di byte di risposta escludendo le intestazioni HTTP oppure '' se zero. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %B </span> </p> </td> 
   <td> <p>Numero di byte di risposta escluse le intestazioni HTTP. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %D </span> </p> </td> 
   <td> <p>Richiedi tempo di elaborazione in millisecondi. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %I  </span> </p> </td> 
   <td> <p>id thread (per i riferimenti incrociati alle voci del registro di debug/errori). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %G </span> </p> </td> 
   <td> <p>data e ora, formattate come <span class="codeph"> <span class="varname"> aaaa </span>- <span class="varname"> MM </span>- <span class="varname"> gg </span> <span class="varname"> HH </span>: <span class="varname"> mm </span>: <span class="varname"> ss </span>. <span class="varname"> SSS  </span> offset  </span> </p> <p> ( <span class="varname"> SSS </span> sono msec, <span class="varname"> offset </span> è l'offset orario GMT); il valore temporale viene acquisito quando la risposta viene inviata al client. </p> </td> 
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
   <td> <p>Porta locale su cui è stata ricevuta la richiesta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %q  </span> </p> </td> 
   <td> <p>Stringa query (preceduta da '?' se esiste). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %l </span> </p> </td> 
   <td> <p>Prima riga di richiesta (metodo di richiesta, URI, versione HTTP). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %R  </span> </p> </td> 
   <td> <p>Come <span class="codeph"> %r </span>, ma applica una codifica HTTP limitata all'URI per evitare problemi di analisi del registro. </p> </td> 
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
   <td> <p>Utente remoto che è stato autenticato (se presente), else ''. </p> </td> 
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
   <td> <p>Chiave cache del server piattaforma (cartella/nome del file della cache). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{CacheUse}r  </span> </p> </td> 
   <td> <p>Parola chiave di gestione cache server piattaforma: <span class="codeph"> { REUSED | CREATO | AGGIORNATO | REMOTE | REMOTE_CREATED | REMOTE_UPDATED | REMOTE_CACHE | CONVALIDATO | IGNORATO | UNDEFINED } </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ContentType}r  </span> </p> </td> 
   <td> <p>Il tipo MIME della risposta. </p> </td> 
  </tr> 
  <tr> 
   <td> <p>%{Context}r </p> </td> 
   <td> <p>Contesto di destinazione se si verifica un inoltro del contesto. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Digest}r  </span> </p> </td> 
   <td> <p>Valore dell'intestazione di risposta <span class="codeph"> tag </span> (firma MD5 dei dati di risposta). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Exception}r  </span> </p> </td> 
   <td> <p>Messaggio di errore. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{FetchTime}r  </span> </p> </td> 
   <td> <p>Tempo impiegato per recuperare le voci della cache o i dati dal server immagini. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ParseTime}r  </span> </p> </td> 
   <td> <p>Tempo impiegato per l’analisi delle richieste e la ricerca del catalogo immagini. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PathBasedAccess}r  </span> </p> </td> 
   <td> <p>Indica se questa richiesta ha tentato o meno un accesso basato su percorso all'esterno del sistema catalogo. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{PeerServer}r  </span> </p> </td> 
   <td> <p>Indirizzo IP del server peer nel cluster di cache che ha inviato la voce della cache o '-' se <span class="codeph"> CacheUse </span> non è <span class="codeph"> REMOTE_CREATED </span> né <span class="codeph"> REMOTE_UPDATED </span>. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{ProcessingStatus}r  </span> </p> </td> 
   <td> <p>Categoria errore: </p> <p> 
     <ul id="ul_BA2A18337D374939AC9BF2424247E40F"> 
      <li id="li_0A2410F03E1A41078F8E8FDF34531810"> <p>0=nessun errore. </p> </li> 
      <li id="li_CCEE27F75BD34195895428188B2C30AA"> <p>1=immagini non trovate sul server. </p> </li> 
      <li id="li_315BBCC7B4C1443495C9C2B3F9800C1F"> <p> 2=Errore di utilizzo del protocollo IS o un errore di contenuto diverso da 1. </p> </li> 
      <li id="li_E028FFF165BD4535875F8684FCAF1859"> <p>3=altro errore del server. </p> </li> 
      <li id="li_5AFFB0EE80484885BCDACD9DF3EF58F7"> <p>4=richiesta rifiutata a causa di un sovraccarico temporaneo del server. </p> </li> 
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
   <td> <p>Tempo necessario al server piattaforma per inviare la risposta dopo la scrittura dei dati nel flusso di output. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{Size}r  </span> </p> </td> 
   <td> <p>Come <span class="codeph"> %B </span>, ma include valori per 304 risposte (non modificate). </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{TransformationUrl}r  </span> </p> </td> 
   <td> <p>L’URL finale dopo tutte le trasformazioni del ruleset. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpRequestHeader  </span>}i  </span> </p> </td> 
   <td> <p>Il valore dell'intestazione della richiesta HTTP specificata. </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> %{  <span class="varname"> httpResponseHeader  </span>}  </span> </p> </td> 
   <td> <p>Il valore dell'intestazione di risposta HTTP specificata. </p> </td> 
  </tr> 
 </tbody> 
</table>

Il valore predefinito è `"%G %a %s %{ProcessingStatus}r %{Size}r %D %{ParseTime}r %{FetchTime}r %O %{ReqType}r '%{RootId}r' %{CacheUse}r %R [%I] '%{Referer}i' %{Host}i %{X-Forwarded-For}i %{If-None-Match}i %{If-Match}i %{If-Modified-Since}i %{Digest}r %{ContentType}r %p %{Exception}r %{CacheKey}r %{PeerServer}" %{SendTime}r %{Context}r %{TransformedUrl}r %{PathBasedAccess}r.`
