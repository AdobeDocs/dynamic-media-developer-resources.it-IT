---
title: dpr
description: DPR (Device Pixel Ratio)&mdash;noto anche come CSS pixel ratio&mdash;è la relazione tra i pixel fisici di un dispositivo e i pixel logici.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
source-git-commit: a6e0db8238ba5f2209089c6eda7b42c42f66b25f
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 2%

---

# dpr{#dpr}

Il rapporto pixel del dispositivo (DPR, Device Pixel Ratio), noto anche come rapporto pixel CSS, è la relazione tra i pixel fisici e i pixel logici di un dispositivo. Soprattutto con l&#39;avvento degli schermi retina, la risoluzione pixel dei dispositivi mobili moderni sta crescendo a un ritmo veloce.

Attivando l’ottimizzazione del rapporto pixel del dispositivo, l’immagine viene riprodotta alla risoluzione nativa dello schermo, rendendola più nitida.

Attualmente, la densità di pixel della visualizzazione proviene dai valori di intestazione della rete CDN di Akamai.

`dpr=off|on,dprValue`

<table id="simpletable_4CB26F72A56D4515B767C303F8E8A1CF"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> disattivato </span> </span> </p> </td> 
  <td class="stentry"> <p>Disattiva l’ottimizzazione DPR a livello di singolo URL immagine. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> on, dprValue </span> </span> </p> </td> 
  <td class="stentry"> <p>Sostituisci il valore DPR rilevato da Smart Imaging con un valore personalizzato (rilevato da qualsiasi logica lato client o in altro modo). Il valore consentito per dprValue è un numero qualsiasi maggiore di 0. </p> </td> 
 </tr> 
</table>


È possibile utilizzare `dpr=on,dprValue` anche se l’impostazione DPR a livello aziendale è disattivata.

A causa dell&#39;ottimizzazione DPR, quando l&#39;immagine risultante è maggiore dell&#39;impostazione MaxPix Dynamic Medie, la larghezza MaxPix viene sempre riconosciuta mantenendo le proporzioni dell&#39;immagine.

| Dimensione immagine richiesta | Valore DPR | Dimensioni immagine consegnata |
|-|-|-|
| 816 x 500 | 1 | 816 x 500 |
| 816 x 500 | 2 | 1632 x 1000 |
| 816 x 500 | 3 | 2448 x 1500 |
| 816 x 500 | 4 | 3264 x 2000 |

I valori DPR si basano sui valori lato client rilevati per la rete CDN in bundle. Questi valori a volte sono imprecisi. IPhone5 con `dpr=2`e iPhone12 con dpr=3, entrambi mostrano `dpr=2`. Per i dispositivi ad alta risoluzione, l&#39;invio `dpr=2` è migliore dell’invio `dpr=1`. Il modo migliore per superare questa imprecisione, tuttavia, è utilizzare il DPR lato client per fornire valori accurati al 100%. E funziona per qualsiasi dispositivo, sia esso Apple o qualsiasi altro dispositivo che è stato lanciato. Consulta [Utilizzo di Smart Imaging con proporzioni pixel del dispositivo lato client](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/client-side-dpr.html?lang=en).

## Proprietà

Un attributo di richiesta. Non ha alcun effetto se `dpr` è disattivato o se `dprValue=1`.

## Predefinito

`dpr=off`


## Esempio

`https://smartimaging.scene7.com/is/image/ADBE/AdobeStock_409826521?dpr=on,3`


## Consultate anche

[bfc](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bfc.md), [rete](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-network.md), [Imaging avanzato](https://experienceleague.adobe.com/docs/experience-manager-cloud-service/content/assets/dynamicmedia/imaging-faq.html?lang=en)