---
title: Requisiti di spazio su disco e raccomandazioni
description: Oltre allo spazio necessario per installare il software, Image Server dispone dei seguenti requisiti di spazio su disco.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# Requisiti di spazio su disco e raccomandazioni{#disk-space-requirements-and-recommendations}

Oltre allo spazio necessario per installare il software, Image Server dispone dei seguenti requisiti di spazio su disco:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Descrizione/Posizione predefinita/Impostata con</b> </th> 
   <th class="entry"> <b>Calcolo/Consiglio</b> </th> 
   <th class="entry"> <b>Commenti</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Immagini sorgente, font, profili ICC</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>Varia; consulta i commenti di seguito. </p> </td> 
   <td> <p>Solo i server devono essere accessibili al server immagini e non modificare mai i dati. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache dei dati di risposta HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; almeno 2 GB consigliati. </p> </td> 
   <td> <p>Questa cache memorizza anche dati nidificati/incorporati e immagini di origine esterne. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache dati catalogo immagini</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Consenti alla cartella del catalogo di utilizzare una quantità di spazio 1,5 volte superiore. </p> </td> 
   <td> <p>Compilato quando i cataloghi vengono caricati inizialmente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Dati di registro</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::FileRegistro </span> </p> <p> <span class="codeph"> SV::FileRegistro </span> </p> </td> 
   <td> <p>almeno 100 MB. </p> </td> 
   <td> <p>Varia a seconda della configurazione di registrazione e dell’utilizzo del server. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>File temporanei di Image Server</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::DirectoryTemp </span> </p> </td> 
   <td> <p>100 MB sono sufficienti per la maggior parte degli usi. </p> </td> 
   <td> <p>Dati di breve durata; possono essere necessari per immagini sorgente diverse dagli PTIFF e per determinati formati di immagini di risposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisiti di spazio su disco per le immagini sorgente {#section-317da75099ad480d9a461c7e706d4f1c}

L&#39;Adobe consiglia di convertire tutte le immagini di origine nel formato di file PTIFF (pyramid TIFF file format) utilizzando lo strumento da riga di comando Image Converter. Questa conversione garantisce prestazioni di runtime ottimali di Image Server per tutte le applicazioni. Sebbene il server immagini sia in grado di elaborare tutti i formati di file di origine accettati da IC, Dynamic Medie non supporta tali utilizzi.

Quando si utilizzano file PTIFF, le seguenti regole generali possono essere utili per determinare i requisiti di spazio.

*`total_space`* (byte) = *`number_of_images`*  × (2000 + *`avg_pixel_count`* x *`avg_num_components`*  ×  *`p_factor`*)

* *`avg_pixel_count`* Dimensione media in pixel (larghezza x altezza) di tutte le immagini sorgente originali. Ad esempio, se le immagini originali sono tipicamente di circa 2k × 2k pixel, questo sarebbe di 4 megapixel.
* *`avg_num_components`* Dipende dal tipo di immagini. Per la maggior parte delle immagini RGB, è 3; per la maggior parte delle immagini CMYK o RGBA, è 4. Utilizzare 3.5 se metà delle immagini sono RGB e l&#39;altra metà è RGBA.
* *`p_factor`* Dipende dal tipo di compressione e dalla qualità impostata quando le immagini vengono convertite con IC.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Compressione PTIFF</b> </th> 
   <th class="entry"> <b><i>p_factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Non compresso </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
   <td> <p> 25-0.75, a seconda dell'immagine </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compressione JPEG </p> </td> 
   <td> <p> 1 (tipico per JPEG di qualità 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questa approssimazione non tiene conto del sovraccarico del file system. Lo spazio effettivo sul disco potrebbe essere notevolmente maggiore.

**Esempio**

Un’implementazione di Image Server prevede di utilizzare 30.000 immagini legacy a bassa risoluzione, con una dimensione media di 500 × 500 RGB. Vengono aggiunti nuovi dati a una velocità di 10.000 immagini all&#39;anno. Le dimensioni tipiche dell&#39;immagine CMYK sono 4 × 6 KB. Tutti i dati vengono compressi in JPEG ad alta qualità. La quantità totale di spazio su disco dopo tre anni di utilizzo è stimata come segue:

*`total_space`* = 30.000 × (2k + 0,5k × 0,5k × 3 × 0,1) + 3 × 10.000 × (2k + 4k × 6k × 4 × 0,1) = 2,2 G + 268 GB = circa 270 GB

Per garantire la migliore qualità possibile, si può utilizzare una compressione come lo zip. Supponendo che *`p_factor`* di 0,4, la quantità totale di spazio su disco richiesto è circa quattro volte superiore. In questo caso, poco più di 1 terabyte.
