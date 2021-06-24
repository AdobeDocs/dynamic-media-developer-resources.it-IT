---
description: 'Oltre allo spazio necessario per l''installazione del software, Image Server ha i seguenti requisiti di spazio su disco '
solution: Experience Manager
title: Requisiti e raccomandazioni per lo spazio su disco
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 35486f3f-f0aa-4b69-a1d2-4bc6b5e41c43
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# Requisiti e raccomandazioni per lo spazio su disco{#disk-space-requirements-and-recommendations}

Oltre allo spazio necessario per l&#39;installazione del software, Image Server dispone dei seguenti requisiti di spazio su disco:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Descrizione/ Posizione predefinita/ Imposta con</b> </th> 
   <th class="entry"> <b>Calcolo/raccomandazione</b> </th> 
   <th class="entry"> <b>Commenti</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Immagini di origine, font, profili ICC</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/images  </span> <span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths  </span> </p> </td> 
   <td> <p>Varie; si vedano i commenti di seguito. </p> </td> 
   <td> <p>Deve essere accessibile solo al server di immagini; i server non modificano mai i dati. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache dei dati di risposta HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/is-response  </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders  </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize  </span> x 2; almeno 2 GB consigliati. </p> </td> 
   <td> <p>Questa cache memorizza anche i dati nidificati/incorporati e le immagini sorgente esterne. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache dei dati del catalogo immagini</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/cache/catalog  </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder  </span> </p> </td> 
   <td> <p>Consentire alla cartella del catalogo di utilizzare 1.5x dello spazio. </p> </td> 
   <td> <p>Viene compilata quando i cataloghi vengono caricati inizialmente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Dati del registro</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/logs  </span> </p> <p> <span class="codeph"> PS::LogFolder  </span> </p> <p> <span class="codeph"> IS::LogFile  </span> </p> <p> <span class="codeph"> SV::LogFile  </span> </p> </td> 
   <td> <p>100 Mbyte o più. </p> </td> 
   <td> <p>Varia a seconda della configurazione di registrazione e dell’utilizzo del server. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>File temporanei di Image Server</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder  </span>/temp  </span> </p> <p> <span class="codeph"> IS::TempDirectory  </span> </p> <p> <span class="codeph"> SV::TempDirectory  </span> </p> </td> 
   <td> <p>100 MBytes è sufficiente per la maggior parte degli usi. </p> </td> 
   <td> <p>dati di breve durata; può essere necessario per le immagini sorgente diverse da PTIFF e da alcuni formati immagine di risposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisiti di spazio su disco per le immagini sorgente {#section-317da75099ad480d9a461c7e706d4f1c}

Si consiglia di convertire tutte le immagini di origine nel formato file TIFF piramidale (PTIFF) utilizzando lo strumento a riga di comando Image Converter (IC). Questa conversione assicura prestazioni di runtime ottimali di Image Serving per tutte le applicazioni. Mentre Image Server è in grado di elaborare tutti i formati di file sorgente accettati da IC, Dynamic Media non fornisce supporto per tali usi.

Quando si utilizzano file PTIFF, è possibile determinare i requisiti di spazio tramite le seguenti regole generali.

*`total_space`* (byte) =  *`number_of_images`* x(2000 +  *`avg_pixel_count`* x  *`avg_num_components`* x  *`p_factor`*)

* *`avg_pixel_count`* Dimensione media dei pixel (larghezza x altezza) di tutte le immagini sorgente originali. Ad esempio, se le immagini originali sono generalmente circa 2 k x 2 k pixel, questo sarebbe 4M pixel.
* *`avg_num_components`* Dipende dal tipo di immagini. Per la maggior parte immagini RGB è 3, per la maggior parte immagini CMYK o RGBA è 4. Utilizzare 3,5 se metà delle immagini sono RGB e l&#39;altra metà è RGBA.
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
   <td> <p>Deflate-Compressione </p> </td> 
   <td> <p> 25-0,75, a seconda dell'immagine </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Compressione JPEG </p> </td> 
   <td> <p> 1 (tipico per la qualità JPEG 95) </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>Questa approssimazione non tiene conto del sovraccarico del file system. Lo spazio effettivo sul disco potrebbe essere notevolmente più grande.

**Esempio**

Una distribuzione di Image Serving prevede di utilizzare 30.000 immagini legacy a bassa risoluzione, con una dimensione media di 500x500 pixel RGB. Si prevede che i nuovi dati di qualità di stampa verranno aggiunti a una velocità di 10.000 all&#39;anno. Le dimensioni tipiche dell&#39;immagine CMYK saranno 4k x 6k byte. Tutti i dati saranno compressi in JPEG ad alta qualità. La quantità totale di spazio su disco dopo 3 anni di utilizzo è stimata come segue:

*`total_space`* = 30.000 x (2 k + 0,5 k x 0,5 k x 3 x 0,1) + 3 x 10.000 x (2 k + 4 k x 6 k x 4 x 0,1) = 2,2 G + 268 GB = circa 270 GB

Per garantire la migliore qualità possibile, si può utilizzare la compressione deflate (zip). Supponendo che *`p_factor`* sia pari a 0,4, lo spazio totale su disco richiesto è circa 4 volte più grande. In questo caso, poco più di 1 TB.
