---
description: Scala immagine. Consente di ridimensionare un'immagine sorgente del livello in base al fattore rispetto all'immagine a risoluzione piena.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 5%

---


# scale{#scale}

Scala immagine. Consente di ridimensionare un&#39;immagine sorgente del livello in base al fattore rispetto all&#39;immagine a risoluzione piena.

`scale= *`fattore`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fattore</span> </p> </td> 
  <td class="stentry"> <p>Fattore di scala (reale, maggiore di 0,0). </p></td> 
 </tr> 
</table>

Non viene applicato alcun ridimensionamento quando `scale=1`. *`factor`* dimensioni inferiori a 1.0 e maggiori di 1.0 ingrandiscono l&#39;immagine sorgente.

## Proprietà {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Attributo immagine/maschera di origine. Ignorato se è specificato `size=` anche per il livello corrente. Sostituisce `res=`. Si applica al livello 0 se specificato per `layer=comp`. Ignorato se il livello non è associato a un&#39;immagine o a una maschera.

## Predefinito {#section-26e64904362342a5a62c5f6598f330c4}

Se non specificato, viene utilizzato `res=`. Se `res=` non è specificato, l&#39;immagine viene utilizzata senza ridimensionamento.

## Consultate anche {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) ,  [size=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
