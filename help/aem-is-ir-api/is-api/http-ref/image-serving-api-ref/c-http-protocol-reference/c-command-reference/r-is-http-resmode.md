---
description: Modalità di ricampionamento. Scegliete l’algoritmo di ricampionamento e/o interpolazione da usare per il ridimensionamento dei dati immagine. Si applica anche alla rotazione dei livelli di testo e al ridimensionamento delle immagini composite durante la trasformazione della vista.
seo-description: Modalità di ricampionamento. Scegliete l’algoritmo di ricampionamento e/o interpolazione da usare per il ridimensionamento dei dati immagine. Si applica anche alla rotazione dei livelli di testo e al ridimensionamento delle immagini composite durante la trasformazione della vista.
seo-title: resMode
solution: Experience Manager
title: resMode
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 8e12aa06-072c-4e7a-84e6-01437c43c57b
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 15%

---


# resMode{#resmode}

Modalità di ricampionamento. Scegliete l’algoritmo di ricampionamento e/o interpolazione da usare per il ridimensionamento dei dati immagine. Si applica anche alla rotazione dei livelli di testo e al ridimensionamento delle immagini composite durante la trasformazione della vista.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l’interpolazione bi-lineare standard. È il metodo di ricampionamento più veloce; possono essere visibili alcuni artefatti di alias. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l’interpolazione bicubica. Richiede maggiore utilizzo della CPU rispetto all’interpolazione bilineare, ma produce immagini più nitide con meno artefatti di alias. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2  </span> </p> </td> 
   <td colname="col2"> <p>come algoritmo di interpolazione viene utilizzata una funzione Lanczos Window modificata. I risultati possono essere leggermente più nitidu dell’opzione bicubica, ma richiede un utilizzo maggiore della CPU. <span class="codeph"> sharp  </span> è stato sostituito da  <span class="codeph"> sharp2  </span>, che ha una minore probabilità di causare artefatti di aliasing (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bisharp  </span> </p> </td> 
   <td colname="col2"> <p>Seleziona il ricampionamento predefinito di Photoshop per ridurre le dimensioni dell’immagine, detto "bicubico più nitido" in  Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-a171bacf4ddf43c782e46b86a16d443e}

Attributo di richiesta. Si applica a tutte le operazioni di ridimensionamento necessarie per creare l’immagine di risposta finale, incluso tutto il ridimensionamento del livello.

## Predefinito {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Esempio {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Ottenete una rappresentazione di qualità ottimale di un’immagine a più livelli memorizzata in un catalogo immagini. L&#39;immagine potrebbe includere del testo. Ci aspettiamo di elaborare ulteriormente un’applicazione di modifica delle immagini, e quindi di richiedere un canale alfa con l’immagine.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Consultate anche {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
