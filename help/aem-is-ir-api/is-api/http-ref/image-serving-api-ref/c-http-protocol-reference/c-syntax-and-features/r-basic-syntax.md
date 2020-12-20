---
description: La sintassi di base del protocollo HTTP è la seguente.
seo-description: La sintassi di base del protocollo HTTP è la seguente.
seo-title: Sintassi di base del protocollo HTTP Image Server
solution: Experience Manager
title: Sintassi di base del protocollo HTTP Image Server
topic: Scene7 Image Serving - Image Rendering API
uuid: 3269c2f2-df0f-4b62-ae9c-a267acae8071
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# Sintassi di base del protocollo HTTP Image Server{#image-serving-http-protocol-basic-syntax}

La sintassi di base del protocollo HTTP è la seguente.

<table id="simpletable_854C20D4C42247B99D9F123543C17E7C"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> request</span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="filepath">http://<span class="varname"> server</span>/is/image[/<span class="varname"> object</span>][?<span class="varname"> modificatori</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> server  </span> </span> </p></td> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> server_address</span>[:<span class="varname"> port</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> object</span> </span> </p></td> 
  <td class="stentry"> <p>Identificatore dell'oggetto di origine (percorso immagine o voce del catalogo immagini). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificatori</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modificatore</span>*[&amp;<span class="varname"> modificatore</span>]</span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> modifier</span> </span> </p></td> 
  <td class="stentry"> <p><span class="codeph">comando|{$<span class="varname"> macro</span>$}|{.<span class="varname"> comment</span>}</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> command</span> </span> </p> </td> 
  <td class="stentry"> <p>{<span class="varname"> cmdName</span>|{$<span class="varname"> var</span>}[=<span class="varname"> value</span>] </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome di una macro di comandi. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> commento</span> </span> </p></td> 
  <td class="stentry"> <p>Stringa commento (ignorata dal server). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> cmdName</span> </span> </p></td> 
  <td class="stentry"> <p>Uno dei nomi di comandi o attributi supportati. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> var</span> </span> </p> </td> 
  <td class="stentry"> <p>Nome di una variabile personalizzata. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span> </span> </p></td> 
  <td class="stentry"> <p>Comando o valore variabile. </p></td> 
 </tr> 
</table>

*`server_address`*,  *`cmdName`*,  *`macro`* e non  *`var`* fa distinzione tra maiuscole e minuscole. Il server conserva le maiuscole e le minuscole di tutti gli altri valori stringa.

*`value`* è specifico del comando e può essere costituito da uno o più valori separati da virgole. Per informazioni dettagliate, fare riferimento alla descrizione dei singoli comandi.

## Identificatore server {#section-926ae55ddba14b8d952147a5fd701e14}

Il contesto [!DNL /is/image] principale è richiesto per tutte le richieste HTTP a Image Server.

## Decodifica HTTP {#section-20922baccd804d2d986b44ce9a183a7d}

Image Serving primi estratti *`object`* e *`modifiers`* dalla richiesta in entrata. *`object`* viene quindi separato in elementi di percorso che sono singolarmente decodificati HTTP. La stringa *`modifiers`* è separata in *`command`*= *`value`* e *`value`* viene quindi decodificata HTTP prima dell&#39;elaborazione specifica per il comando.

>[!NOTE]
>
>Salvo diversa indicazione nella documentazione, tutti i caratteri non sicuri devono essere codificati in base allo standard HTTP. Per informazioni dettagliate, consultate la specifica HTTP.

## Commenti {#section-69ef0be0f17a418c87a0eba21c2ddb00}

I commenti possono essere incorporati nelle stringhe di richiesta ovunque e sono identificati da un punto(.) subito dopo il separatore di comando (&amp;). Il commento viene terminato dall&#39;occorrenza successiva di un separatore di comando (non codificato). Questa funzione può essere utilizzata per aggiungere informazioni alla richiesta che non sono utilizzabili per Image Server, come marche temporali, ID del database, ecc.

## Consultate anche {#section-d0b836568c31454b8dbeb136e6bbe0f0}

[Tipi](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/c-data-types.md#concept-49455c12df954bb5919cdd8d5ccc85fa) di dati, specifiche  [HTTP/1.1](http://www.w3.org/Protocols/rfc2616/rfc2616.html)
