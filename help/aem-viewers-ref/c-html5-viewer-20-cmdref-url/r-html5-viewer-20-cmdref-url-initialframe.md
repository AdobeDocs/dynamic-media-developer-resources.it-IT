---
title: Fotogramma iniziale
description: Parametro comune a tutti i visualizzatori.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 2%

---

# Fotogramma iniziale{#initialframe}

Parametro comune a tutti i visualizzatori.

>[!NOTE]
>
>Questo comando non si applica a Video visualizzatore Immagine.

` initialFrame= *`frameIdx`*[ *`, pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un indice di fotogramma basato su zero che l'visualizzatore visualizza al momento del caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Indice basato su zero della pagina all'interno dello spread quando il dispositivo è in orientamento verticale. Per un ambiente "da sinistra a destra", <span class="codeph"> 0</span> significa "pagina sinistra" e <span class="codeph"> 1</span> significa "pagina destra". Per un ambiente "da destra a sinistra", è opposto: <span class="codeph"> 0</span> significa "pagina destra" e <span class="codeph"> 1</span> significa "pagina sinistra". </p> <p>Se non viene specificato, <span class="codeph"> per impostazione predefinita si presume 0</span> . Ignorato quando dispositivo è con orientamento orizzontale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-10ee45d637134e0fbcd943c62578cb78}

Facoltativo.

## Predefinito {#section-d411e450028c460392cb8508f8ccc5d9}

Nessun valore predefinito.

## Esempio {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```
