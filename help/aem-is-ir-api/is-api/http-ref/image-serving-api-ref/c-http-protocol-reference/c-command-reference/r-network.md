---
title: rete
description: Scopri come utilizzare l’ottimizzazione della larghezza di banda di rete per regolare la qualità dell’immagine fornita in base alla larghezza di banda effettiva della rete.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---

# rete{#network}

L&#39;attivazione della larghezza di banda consente di regolare automaticamente la qualità dell&#39;immagine trasmessa in base all&#39;effettiva larghezza di banda della rete. Per larghezza di banda insufficiente, [DPR (Device Pixel Ratio, rapporto pixel dispositivo)](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md) l&#39;ottimizzazione viene disattivata automaticamente, anche se è già attiva.

Se lo desideri, la tua azienda può scegliere di rinunciare all&#39;ottimizzazione della larghezza di banda a livello di singola immagine aggiungendo `network=off` all&#39;URL dell&#39;immagine.

`network=on|off`

<table id="simpletable_2D23B1B282CD4216AB5BE7E7430D1B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> on|off </span> </p> </td> 
  <td class="stentry"> <p>Specifica se la larghezza di banda di rete regola la qualità dell'immagine trasmessa in base alla larghezza di banda effettiva (attivata) o se l'ottimizzazione della larghezza di banda di rete è disattivata senza alcuna regolazione della qualità dell'immagine.</p> </td> 
 </tr> 
</table>

I valori di DPR e larghezza di banda di rete si basano sui valori lato client rilevati per la rete CDN in bundle. Questi valori a volte sono imprecisi. IPhone5 con `dpr=2`, e iPhone12 con `dpr=3`, entrambi mostrano `dpr=2`. Per i dispositivi ad alta risoluzione, l&#39;invio `dpr=2` è migliore rispetto all’invio di dpr=1. Il modo migliore per superare questa imprecisione, tuttavia, è utilizzare il DPR lato client per fornire valori accurati al 100%. E funziona per qualsiasi dispositivo, sia esso Apple o qualsiasi altro dispositivo che è stato lanciato. Consulta [Utilizzo di Smart Imaging con proporzioni pixel del dispositivo lato client](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Proprietà



## Predefinito

`network=off`

## Esempio

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3&network=on`

## Consultate anche

[drp](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-dpr.md), [Imaging avanzato](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)