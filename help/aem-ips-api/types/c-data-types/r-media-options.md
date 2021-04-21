---
description: Genera un’immagine in miniatura per il video.
solution: Experience Manager
title: MediaOptions
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '131'
ht-degree: 4%

---


# MediaOptions{#mediaoptions}

Genera un’immagine in miniatura per il video.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoEncodingPresetsArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:HandleArray</span> </td> 
   <td colname="col3">Un array di <span class="codeph"> PropertySet</span> gestisce il riferimento ai predefiniti di codifica video per la transcodifica dei video. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generateThumbnail</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Se true, il primo fotogramma del video viene estratto e utilizzato come immagine di anteprima. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbnailOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:ThumbnailOptions</span> </td> 
   <td colname="col3">Facoltativo. Consente di scegliere un particolare fotogramma video da usare come immagine miniatura. <p>Per specificare un'immagine in miniatura, passare il tempo (in millisecondi dall'inizio del video) per il fotogramma che si desidera utilizzare. I valori variano da 0 alla fine del video. <p>Nota: Se specifichi l'ora in modo errato, per impostazione predefinita <span class="codeph"> generateThumbnail</span> restituisce true. </p></p><p>Vedere <a href="../../types/c-data-types/r-thumbnail-options.md#reference-370088b0a4ce4096b9b3e5489a368b5c" format="dita" scope="local"> ThumbnailOptions</a>. </p></td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-a9356de782d74af6933c39fa7ad12212}

```
<complexType name="MediaOptions">
        <sequence>
            <element name="videoEncodingPresetsArray" type="types:HandleArray" minOccurs="0"/>
            <element name="generateThumbnail" type="xsd:boolean" minOccurs="0"/>
            <element name="thumbnailOptions" type="types:ThumbnailOptions" minOccurs="0"/>
        </sequence>
    </complexType>
```

## Utilizzato da {#section-87cb83407198432c95eaa2db9f12f9db}

Il tipo `mediaOptions` viene utilizzato da:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadURLsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

