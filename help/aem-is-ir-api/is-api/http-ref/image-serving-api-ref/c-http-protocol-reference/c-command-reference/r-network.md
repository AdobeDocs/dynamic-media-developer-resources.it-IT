---
title: rete
description: Scopri come utilizzare l’ottimizzazione della larghezza di banda di rete per regolare la qualità dell’immagine fornita in base alla larghezza di banda effettiva della rete.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
source-git-commit: 63c0e3b494b6d583117dad01643946900855802e
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 2%

---

# rete{#network}

L&#39;attivazione della larghezza di banda consente di regolare automaticamente la qualità dell&#39;immagine trasmessa in base all&#39;effettiva larghezza di banda della rete. In caso di larghezza di banda insufficiente, l&#39;ottimizzazione di [DPR (Device Pixel Ratio)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) viene automaticamente disattivata, anche se è già attiva.

Se lo desideri, puoi rinunciare all&#39;ottimizzazione della larghezza di banda di rete a livello di singola immagine aggiungendo `network=off` all&#39;URL dell&#39;immagine.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on|off </span> </p> </td> 
  <td class="stentry"> <p>Specifica se la larghezza di banda di rete regola la qualità dell'immagine trasmessa in base alla larghezza di banda effettiva (attivata) o se l'ottimizzazione della larghezza di banda di rete è disattivata senza alcuna regolazione della qualità dell'immagine.</p> </td> 
 </tr> 
</table>

I valori della larghezza di banda di rete si basano sui valori lato client rilevati per la rete CDN in bundle.

## Proprietà

Un attributo di richiesta. Non ha alcun effetto se le condizioni di rete sono eccellenti.

## Predefinito

`network=off`

## Esempio

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Consultate anche

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Smart Imaging](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=it)
