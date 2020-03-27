---
description: I materiali di rivestimento per finestre comprendono sia rivestimenti per finestre morbidi (tende, valance, tende per caffè), sia rivestimenti per finestre duri (tonalità e persiane).
seo-description: I materiali di rivestimento per finestre comprendono sia rivestimenti per finestre morbidi (tende, valance, tende per caffè), sia rivestimenti per finestre duri (tonalità e persiane).
seo-title: Rivestimenti per finestre
solution: Experience Manager
title: Rivestimenti per finestre
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d74466a-b7c3-43b0-9b0b-f8bb809e2773
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Window coverings{#window-coverings}

I materiali di rivestimento per finestre comprendono sia rivestimenti per finestre morbidi (tende, valance, tende per caffè), sia rivestimenti per finestre duri (tonalità e persiane).

I materiali di copertura della finestra specificano un file *di stile di* finestra (estensione del [!DNL .vnw] file), un file di dati speciale simile a una vignettatura, contenente maschera, illuminazione, layout e dati di texture che definiscono la copertura della finestra.

[!DNL vnw] i file non includono il colore e la texture (tessuto) per la copertura della finestra. Queste informazioni vengono specificate separatamente, in modo simile alle texture ripetibili.

I materiali di rivestimento delle finestre possono essere applicati solo agli oggetti Frame che si sovrappongono.

<table id="table_545865B054E84592BDAEDA57DBFAE9B3"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Attributo </p> </th> 
   <th colname="col2" class="entry"> <p>Descrizione </p> </th> 
   <th colname="col3" class="entry"> <p>Predefinito </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>Finestra che copre il file di stile; obbligatorio. </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>File immagine texture (secondo valore per <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>Risoluzione della texture. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute:Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= </span></a> </p> </td> 
   <td colname="col2"> <p>Modalità di ripetizione. </p> </td> 
   <td colname="col3"> <p>0 (ripetizione retta) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span></a> </p> </td> 
   <td colname="col2"> <p>Colore tinta unita (o colora la texture). </p> </td> 
   <td colname="col3"> <p>128 (grigio neutro) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span></a> </p> </td> 
   <td colname="col2"> <p>Opzioni. </p> </td> 
   <td colname="col3"> <p>0 (nessuna nitidezza) </p> </td> 
  </tr> 
 </tbody> 
</table>

