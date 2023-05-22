---
title: Rivestimenti per finestre
description: I materiali di rivestimento delle finestre includono sia rivestimenti morbidi per finestre (tende, mantovane, tende da caffè) che rivestimenti duri per finestre (tonalità e persiane).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ce6543a1-2438-4661-95bf-ff3d956013bc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 4%

---

# Rivestimenti per finestre{#window-coverings}

I materiali di rivestimento delle finestre includono sia rivestimenti morbidi per finestre (tende, mantovane, tende da caffè) che rivestimenti duri per finestre (tonalità e persiane).

I materiali di rivestimento per finestre specificano *file di stile per la visualizzazione di finestre* ( [!DNL .vnw] file extension), un file di dati speciale simile a una vignettatura, contenente dati di maschera, illuminazione, layout e texture che definiscono il rivestimento della finestra.

[!DNL vnw] I file non includono il colore e la trama (fabric) del rivestimento della finestra. Queste informazioni sono specificate separatamente, in modo simile alle texture ripetibili.

I materiali di rivestimento delle finestre possono essere applicati solo agli oggetti di frame di copertura delle finestre, che sono oggetti sovrapposti.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>File di stile di copertina della finestra; obbligatorio. </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>File immagine texture (secondo valore per <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Risoluzione della texture. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute::Risoluzione </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-repeat.md#reference-37749da8233f42599ecf4731055fb7d8" type="reference" format="dita" scope="local"> <span class="codeph"> repeat= ripetizione </span> </a> </p> </td> 
   <td colname="col2"> <p>Modalità di ripetizione. </p> </td> 
   <td colname="col3"> <p>0 (ripetizione diretta) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= colore </span> </a> </p> </td> 
   <td colname="col2"> <p>Tinta unita (o colorizza la texture). </p> </td> 
   <td colname="col3"> <p>128 (grigio neutro) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Opzioni. </p> </td> 
   <td colname="col3"> <p>0 (nessuna nitidezza) </p> </td> 
  </tr> 
 </tbody> 
</table>
