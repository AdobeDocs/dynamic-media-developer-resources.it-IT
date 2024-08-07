---
description: È possibile utilizzare un proxy server immagini per ridimensionare le immagini per i telefoni giapponesi.
solution: Experience Manager
title: Proxy server immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0389a4af-a412-42eb-b7b4-716e47d623a0
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---

# Proxy server immagini{#image-server-proxy}

È possibile utilizzare un proxy server immagini per ridimensionare le immagini per i telefoni giapponesi.

## Formato URL {#section-2e8c40b0547c4f99874cdf502b338940}

Il formato dell’URL per il proxy IS è molto simile alle normali richieste IS. Tutti i modificatori IS passati al proxy vengono trasmessi al server immagini. Puoi trovare informazioni sui modificatori IS in [Riferimento protocollo HTTP](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Elenco modificatori specifici del proxy {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widpercent = &lt;numero&gt;</span> </p></td> 
  <td class="stentry"> <p>Specifica la percentuale della larghezza utilizzabile del dispositivo da utilizzare come larghezza dell'immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercent = &lt;numero&gt;</span> </p></td> 
  <td class="stentry"> <p>Specifica la percentuale dell'altezza utilizzabile del dispositivo da utilizzare come altezza dell'immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercent = &lt;numero&gt;</span> </p></td> 
  <td class="stentry"> <p>Specifica la percentuale della proprietà del supporto incorporato con limite di memoria del dispositivo a cui limitare la dimensione della risposta. Questo vale solo per le risposte jpg. La qualità dell’immagine viene ridotta finché la dimensione della risposta non rientra nella percentuale specificata. </p></td> 
 </tr> 
</table>

## Limite di memoria immagine incorporata {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Se il dispositivo ha un limite alle dimensioni delle immagini che possono essere incorporate in una pagina web, le dimensioni dell’immagine sono limitate a tali dimensioni purché il formato della risposta sia jpg. Il proxy limita le risposte a 500 MB se il dispositivo non ha alcun limite.

## Elaborazione back-end {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

Il proxy scarica, verifica e carica il file di dati Device Atlas una volta al giorno. La verifica estrae proprietà diverse per dispositivi diversi e le confronta con i valori previsti prima di accettare i nuovi dati.
