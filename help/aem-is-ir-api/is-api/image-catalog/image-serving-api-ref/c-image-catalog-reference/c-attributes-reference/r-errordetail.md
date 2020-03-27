---
description: Dettagli del messaggio di errore. Specifica il livello di dettaglio dei messaggi di errore restituiti tramite HTTP come valore error.message.
seo-description: Dettagli del messaggio di errore. Specifica il livello di dettaglio dei messaggi di errore restituiti tramite HTTP come valore error.message.
seo-title: ErrorDetail
solution: Experience Manager
title: ErrorDetail
topic: Scene7 Image Serving - Image Rendering API
uuid: 46ebb8c7-930e-4844-8664-ec6a63691523
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# ErrorDetail{#errordetail}

Dettagli del messaggio di errore. Specifica il livello di dettaglio dei messaggi di errore restituiti tramite HTTP come valore error.message.

Sono consentiti i seguenti valori:

<table id="simpletable_26DC72727F224F2C8E97BF26619DB68B"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p></td> 
  <td class="stentry"> <p>Solo titolo. Restituisce una breve descrizione generale dell'errore. Consigliato per i server live a cui è possibile accedere pubblicamente. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p></td> 
  <td class="stentry"> <p>Breve messaggio. Riservato per uso futuro. Attualmente restituisce le stesse informazioni di 0. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p></td> 
  <td class="stentry"> <p>Messaggio dettagliato. Fornisce informazioni dettagliate a livello di utente sull'errore. Può includere informazioni riservate, ad esempio percorsi di file. Consigliato per server di pre-produzione, controllo qualità e sviluppo di applicazioni. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p></td> 
  <td class="stentry"> <p>Informazioni di debug complete. Aggiunge tracce stack Java quando applicabile. Le immagini di errore non includono mai tracce di stack e restituiscono invece informazioni di livello 2 in <span class="codeph"> $error.message</span>. Queste informazioni possono essere utili per segnalare problemi al supporto tecnico di Scene7. </p></td> 
 </tr> 
</table>

## Proprietà {#section-e167895723ca4ad4ba283d3d7b4324de}

Il valore enumerato deve essere 0, 1, 2 o 3.

## Predefinito {#section-8f27098e509945a18676aca0675c8f41}

Ereditato da `default::ErrorDetail` se non specificato o se vuoto.

## Consultate anche {#section-5451b0525ed74121950bfc34726c3970}

[attribute::ErrorImage](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-errorimage.md#reference-c494d5d8b2584fe3800f35baabd0292c)
