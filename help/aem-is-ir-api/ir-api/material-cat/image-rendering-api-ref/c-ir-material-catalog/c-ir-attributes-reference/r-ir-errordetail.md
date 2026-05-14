---
title: ErrorDetail
description: Dettagli del messaggio di errore. Specifica il livello di dettaglio per i messaggi di errore restituiti tramite HTTP come valore error.message.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 39d7fc44-7605-4f93-b2f9-0a6e8bc76ec7
TQID: 'https://experienceleague.adobe.com/34sgN8GefR-rkAcikbnE3p3Yh6-1xJXEMfEg6Q74yLM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 176
ht-degree: 3%

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
