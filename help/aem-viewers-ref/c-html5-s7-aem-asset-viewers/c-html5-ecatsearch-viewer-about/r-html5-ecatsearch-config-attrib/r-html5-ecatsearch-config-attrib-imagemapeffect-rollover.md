---
title: ImageMapEffect.rollover
description: ImageMapEffect.rollover
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: 29ca3d4d-6953-4148-9b1e-01e94d1da7df
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 4%

---

# ImageMapEffect.rollover{#imagemapeffect-rollover}

[!DNL `[ImageMapEffect.|<containerId>_imageMapEffect.]rollover=0|1`]

<table id="table_2671D63442B54F659C32C4A3CC61DD7C"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 0 | 1</span> </p> </td> 
   <td colname="col2"> <p>Specifica quando visualizzare il pannello informazioni. </p> <p>Se impostato su <span class="codeph"> 1</span>, il pannello info viene visualizzato quando il mouse entra nell'area mappa immagine (nel caso in cui la mappa immagine abbia un valore non vuoto, <span class="codeph"> chiave_rollover</span> ). </p> <p>Se impostato su <span class="codeph"> 0</span>, il pannello informazioni viene attivato quando si seleziona la mappa immagine (se questa ha un valore non vuoto) <span class="codeph"> chiave_rollover</span> e vuoto <span class="codeph"> href</span> attributi). </p> <p> Ignorato sui dispositivi touch, inclusi i sistemi desktop touch, impostato automaticamente su <span class="codeph"> 0</span>. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-ccfedc2da28f412a86d03f390db92b4b}

Facoltativo.

## Predefinito {#section-79eb39c444814c9398df1f5f3730d289}

[!DNL `0`]

## Esempio {#section-b548ed09b52b4b65888ac891af08d725}

[!DNL `rollover=1`]
