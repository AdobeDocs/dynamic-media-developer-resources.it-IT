---
description: Carica l’impostazione per elaborare i file ZIP e TAR come risorse primarie (Nessuno) o per estrarne e caricarne il contenuto (Annulla compressione).
solution: Experience Manager
title: DecomprimiOpzioni
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 89222959-3701-4ea6-bcae-98ceec93764f
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '98'
ht-degree: 5%

---

# DecomprimiOpzioni{#uncompressoptions}

Carica l’impostazione per elaborare i file ZIP e TAR come risorse primarie (Nessuno) o per estrarne e caricarne il contenuto (Annulla compressione).

>[!NOTE]
>
>`None` è il valore predefinito.

## Parametri {#section-10e49e27f60743da970a4ff1c4587eab}

<table id="table_89C2F7CDB24848459E47F1F7F58D91BA"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> processo</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Controlla l'elaborazione dei file di archivio ZIP e TAR. Fornisce 2 opzioni: 
     <ul id="ul_F34E2F3B9B74450CA7E76BD9FD7137C2">
      <li id="li_E982468ED814446593B0C0A3F3D729FB"><span class="codeph"> Nessuno:</span> elabora come risorse primarie. </li>
      <li id="li_4A45DA99592B4EF7A1FE0A946A835104"><span class="codeph"> Decomprimi:</span> estrae ed elabora il contenuto. </li>
     </ul><p>Nota: Le costanti stringa fanno distinzione tra maiuscole e minuscole. Utilizzare <span class="codeph"> UnCompress</span>, non <span class="codeph"> decomprimere</span> o <span class="codeph"> unCompress</span>. </p></p> </td> 
  </tr> 
 </tbody> 
</table>

## Esempio {#section-48fd14af768a436284c31692038579a8}

```
 <!-- uncompress zip/tar/gzip files -->
            <element name="unCompressOptions" type="types:UnCompressOptions" minOccurs="0"/>
    <complexType name="UnCompressOptions">
        <sequence>
            <!-- Options: None (default),UnCompress -->
            <element name="process" type="xsd:string"/>
        </sequence>
    </complexType>
```

## Utilizzato da {#section-b2a829cf5511412e968bb2000f85cc31}

Il tipo `unCompressionOptions` viene utilizzato da:

* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)
