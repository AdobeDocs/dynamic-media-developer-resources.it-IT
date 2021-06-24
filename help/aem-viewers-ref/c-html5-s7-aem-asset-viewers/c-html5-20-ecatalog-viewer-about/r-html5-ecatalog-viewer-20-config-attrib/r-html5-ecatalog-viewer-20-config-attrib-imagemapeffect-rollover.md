---
description: ImageMapEffect.rollover
solution: Experience Manager
title: ImageMapEffect.rollover
feature: Dynamic Media Classic,Visualizzatori,SDK/API,eCatalog
role: Developer,Business Practitioner
exl-id: 3d5eb17d-668a-4ad8-9f84-5684941d450d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 5%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

`[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Specifica quando visualizzare il pannello informazioni. </p> <p>Se è impostato su <span class="codeph"> 1</span>, il pannello informazioni viene visualizzato quando il mouse entra nell'area della mappa immagine (nel caso in cui la mappa immagine non sia vuota, l'attributo <span class="codeph"> rollover_key</span> ). </p> <p>Se è impostato su <span class="codeph"> 0</span> pannello info viene attivato quando si fa clic sulla mappa immagine (se la mappa immagine ha attributi <span class="codeph"> rollover_key</span> non vuoti e <span class="codeph"> href</span> vuoti). </p> <p> Sui dispositivi touch, inclusi i sistemi desktop touch, viene ignorato e viene automaticamente impostato su <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-ccfedc2da28f412a86d03f390db92b4b}

Facoltativo.

## Predefinito {#section-79eb39c444814c9398df1f5f3730d289}

`0`

## Esempio {#section-b548ed09b52b4b65888ac891af08d725}

`rollover=1`
