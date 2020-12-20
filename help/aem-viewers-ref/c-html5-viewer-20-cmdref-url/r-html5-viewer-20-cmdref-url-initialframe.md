---
description: Parametro comune a tutti i visualizzatori.
seo-description: Parametro comune a tutti i visualizzatori.
seo-title: initialFrame
solution: Experience Manager
title: initialFrame
topic: Dynamic media
uuid: 5d1c3a8a-8598-47c9-a106-36e8c6fcafb0
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# initialFrame{#initialframe}

Parametro comune a tutti i visualizzatori.

>[!NOTE]
>
>Questo comando non si applica al visualizzatore di immagini video.

` initialFrame= *`frameIdx`*[ *`,pageIdx`*]`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> frameIdx</span> </span> </p> </td> 
   <td colname="col2"> <p> Specifica un indice di frame basato su zero visualizzato dal visualizzatore al caricamento. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"><span class="varname"> pageIdx</span></span> </p> </td> 
   <td colname="col2"> <p>Un indice basato su zero della pagina all'interno del set di pagine affiancate quando il dispositivo è con orientamento verticale. In un ambiente "da sinistra a destra" <span class="codeph"> 0</span> significa "pagina sinistra" e <span class="codeph"> 1</span> significa "pagina destra". In "da destra a sinistra" è l'opposto: <span class="codeph"> 0</span> significa "pagina destra" e <span class="codeph"> 1</span> significa "pagina sinistra". </p> <p>Se non viene specificato, per impostazione predefinita viene utilizzato <span class="codeph"> 0</span>. Ignorato quando il dispositivo è con orientamento orizzontale. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-10ee45d637134e0fbcd943c62578cb78}

Facoltativo.

## Predefinito {#section-d411e450028c460392cb8508f8ccc5d9}

Nessuna impostazione predefinita.

## Esempio {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
initialFrame=2
```

