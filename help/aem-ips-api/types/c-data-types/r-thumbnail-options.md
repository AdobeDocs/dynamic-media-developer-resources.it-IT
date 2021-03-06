---
description: Tipo opzionale che consente di scegliere un particolare fotogramma video da usare come immagine miniatura.
solution: Experience Manager
title: ThumbnailOptions
feature: Dynamic Media Classic, SDK/API
role: Developer,Admin
exl-id: 7d84590d-2227-4d9a-9cb0-0f4b1fcabd8e
source-git-commit: fcda99340a18d5037157723bb3bdca5fa9df3277
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 5%

---

# ThumbnailOptions{#thumbnailoptions}

Tipo opzionale che consente di scegliere un particolare fotogramma video da usare come immagine miniatura.

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
   <td colname="col3"> <p>Imposta il tempo (in millisecondi dall'inizio del video) per il fotogramma che si desidera utilizzare per la miniatura del video. I valori variano da 0 alla fine del video. <p>Nota: Il sistema utilizza il primo fotogramma del video per la miniatura se si specifica l'ora in modo errato. Consulta <a href="../../types/c-data-types/r-media-options.md#reference-18618fc6803a4b6e994bbb48eba93b5b" format="dita" scope="local"> MediaOptions</a>. </p></p> </td> 
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
