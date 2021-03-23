---
description: Parametro comune a tutti i visualizzatori.
seo-description: Parametro comune a tutti i visualizzatori.
seo-title: serverUrl
solution: Experience Manager
title: serverUrl
uuid: a079a223-7478-4b6a-bc99-284e3366fb30
feature: Dynamic Media Classic,Visualizzatori,SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 2%

---


# serverUrl{#serverurl}

Parametro comune a tutti i visualizzatori.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Percorso principale di Image Server relativo o assoluto. </p> <p> Specifica un percorso relativo o assoluto di Image Server, dal quale il visualizzatore recupera le immagini. Se il percorso non ha una <span class="filepath"> /</span> iniziale, è relativo alla posizione della pagina HTML del visualizzatore. Se il percorso ha un percorso iniziale <span class="filepath"> /</span>, specifica un percorso assoluto sullo stesso server. </p> <p> Utilizza solo un percorso assoluto nel caso in cui il modulo Condivisione e-mail sia abilitato nel visualizzatore. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-10ee45d637134e0fbcd943c62578cb78}

Facoltativo. Non necessario per l&#39;utilizzo standard SaaS (software as a service).

## Predefinito {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Esempi {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

