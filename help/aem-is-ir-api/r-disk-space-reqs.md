---
description: 'Oltre allo spazio necessario per installare il software, Image Server ha i seguenti requisiti di spazio su disco '
seo-description: 'Oltre allo spazio necessario per installare il software, Image Server ha i seguenti requisiti di spazio su disco '
seo-title: Requisiti di spazio su disco e raccomandazioni
solution: Experience Manager
title: Requisiti di spazio su disco e raccomandazioni
topic: Scene7 Image Serving - Image Rendering API
uuid: a6a21886-94d6-45b3-af68-497e039bdbac
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Requisiti di spazio su disco e raccomandazioni{#disk-space-requirements-and-recommendations}

Oltre allo spazio necessario per installare il software, Image Server ha i seguenti requisiti di spazio su disco:

<table id="table_0AE363AB76304F258A19E43500FE8423"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Descrizione/Posizione predefinita/Set con</b> </th> 
   <th class="entry"> <b>Calcolo/Raccomandazione</b> </th> 
   <th class="entry"> <b>Commenti</b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p><b>Immagini sorgente, font, profili ICC</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/images </span><span class="codeph"></span> </p> <p> <span class="codeph"> IS::RootPaths </span> </p> </td> 
   <td> <p>Varie; si vedano i commenti riportati di seguito. </p> </td> 
   <td> <p>Deve essere accessibile solo al server immagini; i server non modificano mai i dati. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache dei dati di risposta HTTP</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/is-response </span> </p> <p> <span class="codeph"> PS::ResponseCacheFolders </span> </p> </td> 
   <td> <p> <span class="codeph"> PlatformServer::cache.maxSize </span> x 2; consigliato almeno 2 GB. </p> </td> 
   <td> <p>Questa cache memorizza anche i dati nidificati/incorporati e le immagini sorgente esterne. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Cache dei dati del catalogo immagini</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/cache/catalog </span> </p> <p> <span class="codeph"> CS::CatalogCacheFolder </span> </p> </td> 
   <td> <p>Consentite alla cartella del catalogo di usare 1,5 volte lo spazio disponibile. </p> </td> 
   <td> <p>Viene compilata quando i cataloghi vengono caricati inizialmente. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>Dati del registro</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/logs </span> </p> <p> <span class="codeph"> PS::LogFolder </span> </p> <p> <span class="codeph"> IS::LogFile </span> </p> <p> <span class="codeph"> SV::LogFile </span> </p> </td> 
   <td> <p>almeno 100 Mbyte. </p> </td> 
   <td> <p>Varia a seconda della configurazione di accesso e dell'uso del server. </p> </td> 
  </tr> 
  <tr> 
   <td> <p><b>File temporanei di Image Server</b> </p> <p> <span class="filepath"> <span class="varname"> install_folder </span>/temp </span> </p> <p> <span class="codeph"> IS::TempDirectory </span> </p> <p> <span class="codeph"> SV::TempDirectory </span> </p> </td> 
   <td> <p>100 MByte è sufficiente per la maggior parte degli usi. </p> </td> 
   <td> <p>dati di breve durata; può essere necessario per immagini sorgente diverse dai PTIFF e per alcuni formati immagine di risposta. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Requisiti di spazio su disco per le immagini sorgente {#section-317da75099ad480d9a461c7e706d4f1c}

Si consiglia di convertire tutte le immagini sorgente nel formato PTIFF (piramide TIFF) utilizzando lo strumento da riga di comando Image Converter (IC). Questa conversione assicura prestazioni di runtime ottimali di Image Server per tutte le applicazioni. mentre il server immagini può elaborare tutti i formati di file sorgente accettati da IC, Scene7 non supporta tali usi.

Quando si utilizzano i file PTIFF, è possibile determinare i requisiti di spazio mediante le regole riportate di seguito.

*`total_space`* (byte) = *`number_of_images`* x(2000 + *`avg_pixel_count`* x *`avg_num_components`* x *`p_factor`*)

* *`avg_pixel_count`* La dimensione in pixel media (larghezza x altezza) di tutte le immagini sorgente originali. Ad esempio, se le immagini originali sono in genere circa 200 x 2000 pixel, si tratterebbe di 4000 pixel.
* *`avg_num_components`* Dipende dal tipo di immagini. Per la maggior parte delle immagini RGB è 3, per la maggior parte immagini CMYK o RGBA è 4. Usate 3,5 se metà delle immagini sono RGB e l’altra metà è RGBA.
* *`p_factor`* Dipende dal tipo di compressione e dalla qualità impostata quando le immagini vengono convertite con l’interfaccia IC.

<table id="table_89995BECF30243569954819D07DA2A2F"> 
 <thead> 
  <tr> 
   <th class="entry"> <b>Compressione PTIFF</b> </th> 
   <th class="entry"> <b><i>p_Factor</i></b> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p>Non compresso </p> </td> 
   <td> <p> 33 </p> </td> 
  </tr> 
  <tr> 
   <td> <p>Deflate-Compression </p> </td> 
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
>Questa approssimazione non tiene conto del sovraccarico del file system. Lo spazio effettivo su disco potrebbe essere notevolmente più grande.

**Esempio**

Una distribuzione di Image Serving prevede l’utilizzo di 30.000 immagini precedenti a bassa risoluzione, con una dimensione media di 500x500 pixel RGB. I nuovi dati immagine di qualità di stampa dovrebbero essere aggiunti alla velocità di 10.000 all&#39;anno. Le dimensioni tipiche dell&#39;immagine CMYK saranno di 4k x 6k byte. Tutti i dati saranno compressi JPEG ad alta qualità. La quantità totale di spazio su disco dopo 3 anni di utilizzo è stimata come segue:

*`total_space`* = 30.000 x (2 k + 0,5 k x 0,5 k x 3 x 0,1) + 3 x 10.000 x (2 k + 4 k x 6 k x 4 x 0,1) = 2,2 G + 268 GB = circa 270 GB

Per garantire la massima qualità, si potrebbe utilizzare la compressione deflate (zip). Supponendo *`p_factor`* di 0,4, lo spazio su disco richiesto è circa 4 volte maggiore. In questo caso, poco più di 1 TB.
