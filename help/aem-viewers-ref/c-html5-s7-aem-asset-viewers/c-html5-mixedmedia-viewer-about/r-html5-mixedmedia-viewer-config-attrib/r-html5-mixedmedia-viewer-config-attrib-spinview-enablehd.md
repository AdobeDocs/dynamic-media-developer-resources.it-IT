---
description: SpinView.enableHD
solution: Experience Manager
title: SpinView.enableHD
feature: Dynamic Media Classic,Visualizzatori,SDK/API,Set di file multimediali diversi
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 4%

---


# SpinView.enableHD{#spinview-enablehd}

` [SpinView.|<containerId>_spinView.]enableHD=always|never|limit[, *`numero`*]`

<table id="table_8929B59833DE4E1C89FA4BCF07309809"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> always|never|limit</span> </p> </td> 
   <td colname="col2"> <p> Abilita, limita o disabilita l'ottimizzazione per i dispositivi in cui <span class="codeph"> devicePixelRatio</span> è maggiore di <span class="codeph"> 1</span>, ovvero per i dispositivi con visualizzazione ad alta densità come iPhone4 e dispositivi simili. Se attivo, il componente limita le dimensioni della richiesta di immagine IS come se il dispositivo avesse solo un rapporto di pixel di <span class="codeph"> 1</span> e quindi riducesse la larghezza di banda. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"><span class="varname"> numero</span></span> </p> </td> 
   <td colname="col2"> <p> Se si utilizza l'impostazione <span class="codeph"> limit</span> , il componente attiva una densità di pixel elevata solo fino al limite specificato. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Proprietà {#section-65be9301796240e38f31818229da7acc}

Facoltativo.

## Predefinito {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`limit,1500`

## Esempio {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`enableHD=always`
