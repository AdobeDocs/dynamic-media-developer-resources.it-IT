---
description: Modalità di ricampionamento. Scegli l’algoritmo di ricampionamento e/o interpolazione da utilizzare per il ridimensionamento dei dati immagine. Si applica anche alla rotazione dei livelli di testo e al ridimensionamento delle immagini composite durante la trasformazione della vista.
solution: Experience Manager
title: resMode
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '225'
ht-degree: 16%

---


# resMode{#resmode}

Modalità di ricampionamento. Scegli l’algoritmo di ricampionamento e/o interpolazione da utilizzare per il ridimensionamento dei dati immagine. Si applica anche alla rotazione dei livelli di testo e al ridimensionamento delle immagini composite durante la trasformazione della vista.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin  </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l'interpolazione bi-lineare standard. È il metodo di ricampionamento più veloce; possono essere visibili alcuni artefatti di alias. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub  </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l'interpolazione bi-cubica. Maggiore utilizzo della CPU rispetto all'interpolazione bilineare, ma produrrà immagini più nitide con artefatti di aliasing meno evidenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> diesis2  </span> </p> </td> 
   <td colname="col2"> <p>come algoritmo di interpolazione viene utilizzata una funzione Lanczos Window modificata. I risultati possono essere leggermente più nitidu dell’opzione bicubica, ma richiede un utilizzo maggiore della CPU. <span class="codeph"> diesis  </span> è stato sostituito da  <span class="codeph"> Sharp2  </span>, che ha una probabilità minore di causare artefatti di aliasing (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vescovo  </span> </p> </td> 
   <td colname="col2"> <p>Seleziona il ricampionamento predefinito di Photoshop per ridurre le dimensioni dell'immagine, detto "bicubic sharper" in Adobe Photoshop. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-a171bacf4ddf43c782e46b86a16d443e}

Attributo di richiesta. Si applica a tutte le operazioni di ridimensionamento coinvolte nella creazione dell&#39;immagine di risposta finale, inclusa la scala dei livelli.

## Predefinito {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Esempio {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Recupera un rendering di qualità migliore di un’immagine a livelli memorizzata in un catalogo di immagini. L&#39;immagine potrebbe includere del testo. Prevediamo di elaborare ulteriormente in un&#39;applicazione di modifica delle immagini, e quindi richiediamo un canale alfa con l&#39;immagine.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Consultate anche {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attributo::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
