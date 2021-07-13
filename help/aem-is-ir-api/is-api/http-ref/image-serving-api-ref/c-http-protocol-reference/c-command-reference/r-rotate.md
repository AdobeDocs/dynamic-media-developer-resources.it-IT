---
description: Ruota immagine. Ruota il livello dell’immagine, del testo o del colore solido in base all’angolo specificato.
solution: Experience Manager
title: rotate
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 9f1b2d6f-4e67-4530-9ec6-870b97687ce0
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 3%

---

# ruotare{#rotate}

Ruota immagine. Ruota il livello dell’immagine, del testo o del colore solido in base all’angolo specificato.

`rotate= *`angolo`*`

<table id="simpletable_5531ED4C2099411DB404657E12B05314"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> angolo</span> </p> </td> 
  <td class="stentry"> <p>Angolo di rotazione in gradi (reale). </p></td> 
 </tr> 
</table>

Gli angoli positivi ruotano in senso orario. Il punto di ancoraggio del livello ( `anchor=` o `catalog::Anchor`) funge da centro di rotazione. Il rettangolo di livello viene ingrandito e montato intorno ai dati ruotati in base alle necessità per evitare il ritaglio. La rotazione viene applicata dopo aver riempito l&#39;area di sfondo del livello con `color=`. `bgColor=` può essere utilizzato per aggiungere colore di sfondo al rettangolo di delimitazione dopo la rotazione.

## Proprietà {#section-8b5a9bb9062f48dbb8d4e9953ff39e39}

Livello, comando. Si applica al livello corrente o al livello 0 se `layer=comp`. Ignorato dai livelli di effetto.

## Predefinito {#section-69475db636124a8a85f132b6d49bd592}

`rotate=0`, senza rotazione.

## Esempio {#section-e8ab3ba8a8624b43aeaaa8f089fc2f00}

Posiziona un’etichetta &quot;In vendita&quot; vicino all’angolo in alto a sinistra delle immagini in un catalogo di immagini. L&#39;immagine dell&#39;etichetta è già dimensionata correttamente per la visualizzazione 300x300 e deve essere ruotata di 30 gradi a sinistra. Riempire la casella di testo con un colore bianco e semi-opaco per migliorare l&#39;etichetta.

`http:// *`server`*/myRootId/myImageId?scl=1&size=300,300&origin=-0.5,-0.5 &layer=1&src=labelImage&origin=-0.5,-0.5&rotate=-30&color=ffffff40`

Applichiamo `size=` al livello 0 per impostare le dimensioni della visualizzazione, anziché utilizzare `wid=` e `hei=`. Questo consente di ridimensionare `myImageId` senza modificare le dimensioni finali di `labelImage`. Occorre inoltre specificare `scl=1`, altrimenti l&#39;immagine composita potrebbe essere ridimensionata a `attribute::DefaultPix` (a meno che non sia impostata su 0,0). `color=` aggiunge il colore di sfondo semi-opaco alla casella di testo prima della rotazione.

L’origine di entrambi i livelli viene impostata sugli angoli in alto a sinistra, per ottenere l’allineamento desiderato. Il punto di origine del livello 1 si applica a `labelImage`dopo la rotazione.

Per un esempio di testo ruotato, vedere l&#39;esempio A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e) .[

## Consultate anche {#section-c371ee0845994b7382c02e782d1bc595}

[anchor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-anchor.md#reference-6661e548ab284b82828d8d94c8ddeb7c) ,  [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab),  [color=](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)
