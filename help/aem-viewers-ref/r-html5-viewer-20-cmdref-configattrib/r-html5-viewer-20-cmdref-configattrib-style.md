---
title: stile
description: stile
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: a0547ada-3d8f-4ec2-a7e4-424fd1a78a28
TQID: 'https://experienceleague.adobe.com/vkV2CfEEhJmPdQg64y0G-5Ep-T6SPd4tQX88CWbPryw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 97
ht-degree: 2%

---

# stile{#style}

Puoi applicare il seguente comando sia dalla stringa di query URL che dalla configurazione. Il comando applicato nella stringa di query URL ha sempre la precedenza sullo stesso comando presente nella configurazione.

`style= *`cssPath`*`

<table id="table_F800F787CF0342749B934DAEB600C0EB"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> cssPath</span> </span> </p> </td> 
   <td colname="col2"> <p> Posizione CSS relativa o assoluta. </p> <p>Specifica la posizione del file CSS personalizzato. Se il percorso cssPath </span></span> <span class="codeph"><span class="varname"> è relativo, verrà risolto in base alla posizione della pagina HTML del visualizzatore e al valore del parametro <span class="codeph"> contentUrl=</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

Tutti i riferimenti alle risorse all’interno del file CSS vengono risolti in base alla posizione del file CSS, non alla posizione della pagina HTML chiamante.

## Proprietà {#section-8ce2a4493d454d97a9975fc7f9f4eb2c}

Facoltativo.

## Predefinito {#section-79a827f7a3bb4f36b3d72c309155059e}

Nessuno.

## Esempi {#section-f8a0c032979047a38041abfce3f7a70b}

`style=/skins/customStyle.css`

`style=etc/dam/presets/css/html5_interactiveimage.css`

`style=etc/dam/presets/css/html5_interactivevideo.css`

`style=etc/dam/presets/css/html5_carouselviewer_dotted_light.css`
