---
description: La sintassi di base del protocollo HTTP è la seguente.
solution: Experience Manager
title: Sintassi di base del protocollo HTTP Image Server
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: ac75d6d0-a71e-45a0-89ee-b952a0202793
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---

# Sintassi di base del protocollo HTTP Image Server{#image-serving-http-protocol-basic-syntax}

La sintassi di base del protocollo HTTP è la seguente:

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> richiesta</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> modificatori</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server  </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> oggetto</span> </span> </p></td> 
  <td class="stentry"> <p>Identificatore oggetto di origine (percorso immagine o voce di catalogo immagini). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificatori</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificatore</span>*[&amp;<span class="varname"> modificatore</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">comando|{$<span class="varname"> macro</span>$}|{.<span class="varname"> commento</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> command</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}[=<span class="varname"> valore</span>] </p></td> 
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
  <td class="stentry"> <p>Uno dei nomi di comando o attributo supportati.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome di una variabile personalizzata.</p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>Valore di comando o variabile. </p></td> 
 </tr> 
</table>

*`server_address`*,  *`cmdName`*,  *`macro`* e  *`var`* sono senza distinzione tra maiuscole e minuscole. Il server conserva il caso di tutti gli altri valori stringa.

*`value`* è specifico del comando e può essere costituito da uno o più valori separati da virgole. Per ulteriori informazioni, fare riferimento alla descrizione dei singoli comandi.

## Identificatore server {#section-926ae55ddba14b8d952147a5fd701e14}

Il contesto [!DNL /is/image] principale è necessario per tutte le richieste HTTP a Image Server.

## decodifica HTTP {#section-20922baccd804d2d986b44ce9a183a7d}

Image Serving estrae prima *`object`* e *`modifiers`* dalla richiesta in arrivo. *`object`* viene quindi separato in elementi di percorso che sono singolarmente decodificati tramite HTTP. La stringa *`modifiers`* è separata in coppie *`command`*= *`value`* e *`value`* viene quindi decodificata per HTTP prima dell&#39;elaborazione specifica del comando.

>[!NOTE]
>
>Se non diversamente indicato nella documentazione, tutti i caratteri non sicuri devono essere codificati secondo lo standard HTTP. Per ulteriori informazioni, consulta le specifiche HTTP .

## Commenti {#section-69ef0be0f17a418c87a0eba21c2ddb00}

I commenti possono essere incorporati nelle stringhe di richiesta ovunque e sono identificati da un punto(.) subito dopo il separatore dei comandi (&amp;). Il commento viene terminato dall&#39;occorrenza successiva di un separatore di comando (non codificato). Questa funzione può essere utilizzata per aggiungere informazioni alla richiesta che non sono per l’uso di Image Serving, ad esempio timestamp e ID del database.

## Consultate anche {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Tipi](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa) di dati, specifiche  [HTTP/1.1](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
