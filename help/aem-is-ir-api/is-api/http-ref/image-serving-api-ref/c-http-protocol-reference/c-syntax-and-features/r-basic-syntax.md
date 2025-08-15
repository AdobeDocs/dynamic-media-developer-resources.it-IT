---
description: La sintassi di base del protocollo HTTP è la seguente.
solution: Experience Manager
title: Sintassi di base del protocollo HTTP Image Server
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 191d3e7cc4cd370e1e1b6ca5d7e27acd3ded7b6c
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# Sintassi di base del protocollo HTTP Image Server{#image-serving-http-protocol-basic-syntax}

La sintassi di base del protocollo HTTP è la seguente:

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> richiesta</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> oggetto</span>][?<span class="varname"> modificatori</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> indirizzo_server</span>[:<span class="varname"> porta</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> oggetto</span> </span> </p></td> 
  <td class="stentry"> <p>Identificatore oggetto Source (percorso immagine o voce catalogo immagini). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificatori</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificatore</span>*[&amp;<span class="varname"> modificatore</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Modificatore <span class="codeph"> <span class="varname"></span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">comando|{$<span class="varname"> macro</span>$}|{.<span class="varname"> commento</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> comando</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome di una macro di comando.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> commento</span> </span> </p></td> 
  <td class="stentry"> <p>Stringa di commento (ignorata dal server).</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>Uno dei nomi di comando o di attributo supportati.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome di una variabile personalizzata.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> valore</span> </span> </p></td> 
  <td class="stentry"> <p>Valore del comando o della variabile. </p></td> 
 </tr> 
</table>

*`server_address`*, *`cmdName`*, *`macro`* e *`var`* non distinguono tra maiuscole e minuscole. Il server mantiene le maiuscole e minuscole di tutti gli altri valori stringa.

*`value`* è specifico del comando e può essere costituito da uno o più valori separati da virgole. Per ulteriori informazioni, consultare la descrizione dei singoli comandi.

## Identificatore server {#section-926ae55ddba14b8d952147a5fd701e14}

Il contesto radice [!DNL /is/image] è obbligatorio per tutte le richieste HTTP a Image Server.

## Decodifica HTTP {#section-20922baccd804d2d986b44ce9a183a7d}

Image Server estrae prima *`object`* e *`modifiers`* dalla richiesta in ingresso. *`object`* viene quindi separato in elementi percorso che vengono singolarmente decodificati tramite HTTP. La stringa *`modifiers`* è separata in *`command`*= *`value`* coppie e *`value`* viene quindi decodificato HTTP prima dell&#39;elaborazione specifica del comando.

>[!NOTE]
>
>Salvo diversa indicazione nella documentazione, tutti i caratteri potenzialmente pericolosi devono essere codificati in base allo standard HTTP. Per ulteriori informazioni, consulta la specifica HTTP.

## Commenti {#section-69ef0be0f17a418c87a0eba21c2ddb00}

I commenti possono essere incorporati nelle stringhe di richiesta ovunque e sono identificati da un punto (.) immediatamente successivo al separatore di comando (&amp;). Il commento viene terminato dall&#39;occorrenza successiva di un separatore di comando (non codificato). Questa funzione può essere utilizzata per aggiungere informazioni alla richiesta che non sono destinate all’utilizzo in Image Server, ad esempio timestamp e ID di database.

## Consultate anche {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Tipi di dati](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa), [Specifica HTTP/1.1](https://www.w3.org/Protocols/rfc2616/rfc2616.html)
