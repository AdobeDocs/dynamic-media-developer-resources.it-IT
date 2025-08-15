---
title: ErrorDetail
description: Dettagli del messaggio di errore. Specifica il livello di dettaglio per i messaggi di errore restituiti tramite HTTP come valore error.message.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 4%

---

# ErrorDetail{#errordetail}

Dettagli del messaggio di errore. Specifica il livello di dettaglio per i messaggi di errore restituiti tramite HTTP come valore error.message.

## Titolo {#section-c10d75d72ee24d16a67cc8d927f1deba}

Sono consentiti i seguenti valori:

<table id="simpletable_7904444FF9F14D678F05094CA9E45664"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Solo titolo. Restituisce una breve descrizione generale dell’errore. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Breve messaggio. Riservato per uso futuro. Attualmente restituisce le stesse informazioni come 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Messaggio dettagliato. Fornisce dettagli a livello di utente sull’errore. Può includere informazioni riservate, ad esempio i percorsi dei file. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informazioni di debug complete. Se applicabile, aggiunge le tracce dello stack Java™. Le immagini di errore non includono mai le tracce dello stack e restituiscono invece informazioni di livello 2 in <span class="codeph"> $error.message</span>. </p></td> 
 </tr> 
</table>

* Il livello 0 è consigliato per i server live accessibili pubblicamente.
* Il livello 2 è consigliato per i server di staging, controllo qualità e sviluppo applicazioni.
* Le informazioni di livello 3 possono essere utili quando si segnalano problemi al supporto tecnico Dynamic Media.

## Proprietà {#section-f03f9a8edd6a4d99aff38fbec41c4b80}

Il valore enumerato deve essere 0, 1, 2 o 3.

## Predefinito {#section-5e78d550050840cc9a1de811c581b94f}

Ereditato da `default::ErrorDetail` se non specificato o se vuoto.

## Consultate anche {#section-474e71922d194c7ca06f2aad3b30e025}

[attribute::ErrorImage](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-errorimage.md#reference-b58bdaba96074c52802ca8dc54bfe2f0)
