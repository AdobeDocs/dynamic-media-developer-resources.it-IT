---
description: Tipo opzionale che consente di scegliere un particolare fotogramma video da usare come miniatura.
seo-description: Tipo opzionale che consente di scegliere un particolare fotogramma video da usare come miniatura.
seo-title: ThumbnailOptions
solution: Experience Manager
title: ThumbnailOptions
topic: Scene7 Image Production System API
uuid: 50b2ecee-8396-4323-83e1-1f5060bec6c4
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 4%

---


# ThumbnailOptions{#thumbnailoptions}

Tipo opzionale che consente di scegliere un particolare fotogramma video da usare come miniatura.

Sintassi

## Parametri {#section-b1777bf868764a7099d4a954b471856c}

<table id="table_C71FD0C995D94CE18994CDA2DC3460DF"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailTime</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> <p>Imposta il tempo (in millisecondi dall’inizio del video) in base al fotogramma che si desidera utilizzare per la miniatura del video. I valori vanno da 0 alla fine del video. <p>Nota: Il sistema utilizza il primo fotogramma del video per la miniatura se l'ora non è specificata correttamente. Vedere <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-ce3b59c60fea4cd4945427a025051447}

```
<complexType name="ThumbnailOptions">
     <sequence>
        <element name="thumbnailTime" type="xsd:long" minOccurs="0"/>
      </sequence>
</complexType>
```

