---
description: Ridimensiona immagine. Ridimensiona l'immagine sorgente di un livello in base al fattore relativo all'immagine a risoluzione completa.
solution: Experience Manager
title: scale
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c2cd37de-f81e-4b08-9a3e-ff05a72c363c
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '106'
ht-degree: 4%

---

# scale{#scale}

Ridimensiona immagine. Ridimensiona l&#39;immagine sorgente di un livello in base al fattore relativo all&#39;immagine a risoluzione completa.

`scale= *`fattore`*`

<table id="simpletable_AC596A87494A4213A7D1C76612E8F2FD"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> fattore</span> </p> </td> 
  <td class="stentry"> <p>Fattore di scala (reale, maggiore di 0,0). </p></td> 
 </tr> 
</table>

Non viene applicata alcuna scala quando `scale=1`. *`factor`* inferiore a 1.0 ridimensiona e maggiore di 1.0 ingrandisce l&#39;immagine sorgente.

## Proprietà {#section-3c7eb45527394fe79b1ddba6c1fcca09}

Attributo immagine/maschera di origine. Ignorato se `size=` viene specificato anche per il livello corrente. Sostituzioni `res=`. Si applica al livello 0 se specificato per `layer=comp`. Ignorato se il livello non è associato a un&#39;immagine o a una maschera.

## Predefinito {#section-26e64904362342a5a62c5f6598f330c4}

Se non specificato, `res=` viene utilizzato. Se `res=` non è specificato, l&#39;immagine viene utilizzata senza ridimensionamento.

## Consultate anche {#section-61a11f30d37341d58c10df759bfff951}

[res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55) , [size= dimensione](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-size.md#reference-04d383f32c7b4003bed9978cb854747b)
