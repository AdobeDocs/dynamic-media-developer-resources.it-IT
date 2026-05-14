---
title: rete
description: Scopri come utilizzare l’ottimizzazione della larghezza di banda di rete per regolare la qualità dell’immagine fornita in base alla larghezza di banda effettiva della rete.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7df6eeed-1856-40e1-bd5d-8f06efc7f700
TQID: 'https://experienceleague.adobe.com/9odHf3s93xaQyc1WSkXGamAgoQP070p7ItB9HhyT-dQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 162
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
