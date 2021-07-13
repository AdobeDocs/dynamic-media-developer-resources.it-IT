---
description: stile
solution: Experience Manager
title: stile
feature: Dynamic Media Classic,Visualizzatori,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%

---

# stile{#style}

Puoi applicare il seguente comando sia dalla stringa di query URL che dalla configurazione. Il comando applicato nella stringa di query URL ha sempre la precedenza sullo stesso comando presente nella configurazione.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Posizione CSS relativa o assoluta. </p> <p>Specifica la posizione del file CSS personalizzato. Se il <span class="codeph"><span class="varname"> cssPath</span></span> è relativo, viene risolto rispetto alla posizione della pagina HTML del visualizzatore e al valore del parametro <span class="codeph"> contentUrl=</span> . </p> </td> 
  </tr> 
 </tbody> 
</table>

Tutti i riferimenti di risorse all’interno del file CSS vengono risolti rispetto al percorso del file CSS, non al percorso della pagina HTML chiamante.

## Proprietà {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Facoltativo.

## Predefinito {#section-79a827f7a3bb4f36b3d72c309155059e}

Nessuno.

## Esempi {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
