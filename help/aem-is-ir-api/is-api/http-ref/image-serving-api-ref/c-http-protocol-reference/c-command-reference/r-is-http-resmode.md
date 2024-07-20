---
title: resMode
description: Metodo di ricampionamento. Consente di scegliere l'algoritmo di ricampionamento e/o interpolazione da utilizzare per il ridimensionamento dei dati immagine. Applicabile anche alla rotazione dei livelli di testo e al ridimensionamento delle immagini composite durante la trasformazione della vista.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 63c1c028-0378-4a38-8018-e358491786d8
source-git-commit: 7c4492b583e7bd6fb87229c4566f1d9493c8a650
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---

# resMode{#resmode}

Metodo di ricampionamento. Consente di scegliere l&#39;algoritmo di ricampionamento e/o interpolazione da utilizzare per il ridimensionamento dei dati immagine. Applicabile anche alla rotazione dei livelli di testo e al ridimensionamento delle immagini composite durante la trasformazione della vista.

`resMode=bilin|bicub|sharp2|bisharp`

<table id="table_FD658AC521E24EB9ADBB87F98549BC3B"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bilin </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l'interpolazione bilineare standard. Metodo di ricampionamento più veloce; alcuni artefatti di aliasing sono evidenti. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> bicub </span> </p> </td> 
   <td colname="col2"> <p>Seleziona l'interpolazione bi-cubica. Più CPU-intensive rispetto all'interpolazione bi-lineare, ma produce immagini più nitide con meno artefatti di aliasing visibili. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> sharp2 </span> </p> </td> 
   <td colname="col2"> <p>Seleziona una funzione Finestra di Lanczo modificata come algoritmo di interpolazione. Può produrre risultati leggermente più nitidi rispetto al bi-cubico a un costo di CPU più elevato. <span class="codeph"> </span> è stato sostituito da <span class="codeph"> </span>, che ha meno probabilità di causare artefatti di aliasing (Moiré). </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> vescovo </span> </p> </td> 
   <td colname="col2"> <p>Seleziona il ricampionatore predefinito di Photoshop per ridurre le dimensioni dell'immagine, che in Adobe Photoshop è denominato "bicubic sharper". </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!IMPORTANT]
>
>Per mantenere le proporzioni di un&#39;immagine quando si utilizzano sia `resMode=bisharp` che `fit=stretch`, è consigliabile utilizzare il parametro width o il parametro height. Se è necessario definire entrambi i parametri, potete racchiuderli in un livello diverso, come illustrato nell&#39;esempio seguente:
>
>`/is/image/is/image/companyname?layer=0&src=is(companyname/imagename?wid=30&hei=30&fit=stretch)&resmode=bisharp`

## Proprietà {#section-a171bacf4ddf43c782e46b86a16d443e}

Attributo della richiesta. Si applica a tutte le operazioni di ridimensionamento coinvolte nella creazione dell&#39;immagine di risposta finale, inclusa la modifica in scala di tutti i livelli.

## Predefinito {#section-d5e1b26f5703461395018a3a627f7283}

`attribute::ResMode`

## Esempio {#section-ee8c3e5a2e3845fe81de5073a8ab7efe}

Recuperate una rappresentazione di alta qualità di un&#39;immagine a livelli memorizzata in un catalogo di immagini. L&#39;immagine può includere testo. L&#39;immagine viene ulteriormente elaborata in un&#39;applicazione di modifica dell&#39;immagine e richiede quindi un canale alfa con l&#39;immagine.

` http:// *`server`*/myLayeredImage?fmt=tif-alpha,,lzw&resMode=sharp2&wid=1800`

## Consultate anche {#section-5f7b17f66bc940d197f8e77e6b4f9657}

[attribute::ResMode](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-is-cat-resmode.md#reference-609095ef568743a086f28d87c54dafa2)
