---
title: serverUrl
description: Parametro comune a tutti i visualizzatori.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: c9da3d5b-492d-4e1f-8fdc-3255b2b40fc6
source-git-commit: ce1ac4938c7baf482c6c55a9ad13379153a3ec5b
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 1%

---

# serverUrl{#serverurl}

Parametro comune a tutti i visualizzatori.

` serverUrl= *`isRootPath`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> isRootPath</span> </span> </p> </td> 
   <td colname="col2"> <p>Percorso root relativo o assoluto di Image Server. </p> <p> Specifica un percorso relativo o assoluto di Image Server da cui il visualizzatore recupera le immagini. Se il percorso non ha un <span class="filepath"> /</span> iniziale, è relativo alla posizione della pagina HTML del visualizzatore. Se il percorso contiene un <span class="filepath"> /</span> iniziale, specifica un percorso assoluto sullo stesso server. </p> <p> Se nel visualizzatore è abilitato il modulo di condivisione e-mail, utilizza solo un percorso assoluto. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-10ee45d637134e0fbcd943c62578cb78}

Facoltativo. Non necessario per l&#39;utilizzo SaaS (software as a service) standard.

## Predefinito {#section-d411e450028c460392cb8508f8ccc5d9}

`/is/image/`

## Esempi {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

```
serverUrl=http://s7d9.scene7.com/is/image/
```

```
serverUrl=http://aodmarketingna.assetsadobe.com/is/image
```

<!--

```
serverUrl=https://adobedemo62-h.assetsadobe.com/is/image
```

-->
