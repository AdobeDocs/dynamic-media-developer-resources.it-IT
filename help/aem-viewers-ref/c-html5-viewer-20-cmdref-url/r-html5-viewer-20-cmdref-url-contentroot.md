---
title: contentUrl
description: Parametro comune a tutti i visualizzatori.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: cab3c3fe-1a64-4a50-8559-57cadb31f689
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---

# contentUrl{#contenturl}

Parametro comune a tutti i visualizzatori.

` contentUrl= *`contentUrlPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> contentUrlPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Specifica il percorso di base dei file CSS personalizzati, del contenuto dei sottotitoli o del contenuto di navigazione. </p> <p>Se il percorso non ha un <span class="filepath"> /</span> iniziale, è relativo alla posizione della pagina HTML del visualizzatore. Se il percorso contiene un <span class="filepath"> /</span> iniziale, specifica un percorso assoluto sullo stesso server. </p> <p> Non influisce sul caricamento del file CSS predefinito quando non si specifica un comando di stile. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-10ee45d637134e0fbcd943c62578cb78}

Facoltativo.

## Predefinito {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/content/`

## Esempi {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
contentUrl=/skins/
```

```
contentUrl=http://aodmarketingna.assetsadobe.com/
```

```
contentUrl=https://demos-pub.assetsadobe.com/
```
