---
title: initialFrame
description: Parametro comune a tutti i visualizzatori.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: db77edf0-e223-4f44-b83b-b6dbe5c1abd6
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '97'
ht-degree: 3%

---

# initialFrame{#initialframe}

Parametro comune a tutti i visualizzatori.

>[!NOTE]
>
>Questo comando non è applicabile al Visualizzatore immagini video.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un indice di frame a base zero visualizzato al caricamento del visualizzatore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Un indice in base zero della pagina all’interno del set di pagine affiancate quando il dispositivo è in orientamento verticale. Per un ambiente "da sinistra a destra": <span class="codeph"> 0</span> significa "pagina sinistra" e <span class="codeph"> 1</span> significa "pagina destra". Per un ambiente "da destra a sinistra", è l’opposto: <span class="codeph"> 0</span> significa "pagina destra" e <span class="codeph"> 1</span> significa "pagina sinistra". </p> <p>Se non specificato, <span class="codeph"> 0</span> viene utilizzato per impostazione predefinita. Ignorato quando il dispositivo è in orientamento orizzontale. </p> </td> 
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
