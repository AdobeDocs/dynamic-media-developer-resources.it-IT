---
description: Un proxy del server immagini può essere utilizzato per ridimensionare le immagini per i telefoni giapponesi.
seo-description: Un proxy del server immagini può essere utilizzato per ridimensionare le immagini per i telefoni giapponesi.
seo-title: Proxy del server immagini
solution: Experience Manager
title: Proxy del server immagini
topic: Scene7 Image Serving - Image Rendering API
uuid: 49aa0861-9b03-4a62-8604-67e6cb7a621f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---


# Proxy del server immagini{#image-server-proxy}

Un proxy del server immagini può essere utilizzato per ridimensionare le immagini per i telefoni giapponesi.

## Formato URL {#section-2e8c40b0547c4f99874cdf502b338940}

Il formato url per il proxy IS è molto simile alle richieste IS regolari. Eventuali modificatori IS passati al proxy vengono passati al server immagini. Puoi trovare informazioni sui modificatori IS in [HTTP Protocol Reference](../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-introduction/c-introduction.md#concept-dbbd5241bc6248ad9b9d7f6c635c311e).

`http://<server>/is-proxy/image/<company><asset>?<modifiers>`

`http://<server>/is-proxy/image/sample/chair?qlt=75`

## Elenco modificatori specifici del proxy {#section-1bff28f9cf5b4e04a31308b06176ee5f}

<table id="simpletable_40C1DFB183B54A79BCF65D51ED480CE0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> widget =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Specifica la percentuale della larghezza utilizzabile del dispositivo da utilizzare come larghezza dell'immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> heipercentuale =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Specifica la percentuale dell'altezza utilizzabile del dispositivo da utilizzare come altezza dell'immagine. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> sizepercentuale =  &lt;number&gt;</span> </p></td> 
  <td class="stentry"> <p>Specifica la percentuale della proprietà Supporti incorporati limite di memoria del dispositivo a cui limitare la dimensione della risposta. Ciò si applica solo alle risposte jpg. La qualità dell'immagine viene ridotta finché la dimensione della risposta non rientra nella percentuale specificata. </p></td> 
 </tr> 
</table>

## Limite di memoria dell&#39;immagine incorporata {#section-52f7c69ed8a341ceabf92ceee19b0f36}

Se il dispositivo ha un limite alle dimensioni delle immagini che possono essere incorporate in una pagina Web, le dimensioni delle immagini saranno limitate a tale dimensione, purché il formato di risposta sia jpg. Il proxy limita le risposte a 500 MB se il dispositivo non ha alcun limite.

## Elaborazione back-end {#section-bdf7c294b6824de9969c97fc1f8aa6d3}

Il proxy scarica, verifica e carica il file di dati Device Atlas una volta al giorno. La verifica estrae proprietà diverse per dispositivi diversi e le confronta con valori previsti prima di accettare i nuovi dati.
