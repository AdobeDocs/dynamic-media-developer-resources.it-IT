---
description: Dettagli del messaggio di errore. Specifica il livello di dettaglio per i messaggi di errore restituiti tramite HTTP come valore error.message.
solution: Experience Manager
title: ErrorDetail
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08a363d0-918d-48e9-aef0-5a8554c2708a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 4%

---

# ErrorDetail{#errordetail}

Dettagli del messaggio di errore. Specifica il livello di dettaglio per i messaggi di errore restituiti tramite HTTP come valore error.message.

Sono consentiti i seguenti valori:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Solo titolo. Restituisce una breve descrizione generale dell’errore. Consigliato per i server live a cui è possibile accedere pubblicamente. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Breve messaggio. Riservato per uso futuro. Attualmente restituisce le stesse informazioni come 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Messaggio dettagliato. Fornisce dettagli a livello di utente sull’errore. Può includere informazioni riservate, ad esempio i percorsi dei file. Consigliato per server di staging, controllo qualità e sviluppo applicazioni. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informazioni di debug complete. Se applicabile, aggiunge le tracce dello stack Java. Le immagini di errore non includono mai le tracce dello stack e restituiscono invece informazioni di livello 2 in <span class="codeph"> $error.message</span>. Queste informazioni possono essere utili quando si segnalano problemi al supporto tecnico Dynamic Medie. </p></td> 
 </tr> 
</table>

## Proprietà {#section-e167895723ca4ad4ba283d3d7b4324de}

Il valore enumerato deve essere 0, 1, 2 o 3.

## Predefinito {#section-8f27098e509945a18676aca0675c8f41}

Ereditato da `default::ErrorDetail` se non specificato o se vuoto.

## Consultate anche {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
