---
title: Scaffali
description: I materiali dei cabinet specificano un file stile cabinet (estensione .vnc), un file di dati speciale contenente rappresentazioni fotografiche di armadi insieme alle definizioni di layout parametrico e altre informazioni necessarie per il rendering dei fronti dei cabinet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 5%

---

# Scaffali{#cabinets}

I materiali dei cabinet specificano un file stile cabinet (estensione .vnc), un file di dati speciale contenente rappresentazioni fotografiche di armadi insieme alle definizioni di layout parametrico e altre informazioni necessarie per il rendering dei fronti dei cabinet.

[!DNL vnc] i file possono includere una texture di granella di legno ripetibile, oppure la texture può essere fornita esternamente tramite un secondo argomento a `src=`. Certi [!DNL vnc] I file consentono di colorare o testurizzare aree selezionate di frontali di armadietti (tipicamente utilizzati per gli stili laminati di armadio).

I materiali del cabinet possono essere applicati solo agli oggetti del mobile.

<table id="table_0B16200886FE4DFEBB1E4BE8FBA67EE4"> 
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
   <td colname="col2"> <p>File in stile cabinet; obbligatorio. </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>File immagine a texture opzionale (secondo valore per <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Risoluzione di texture opzionale. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attributo::Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span> </a> </p> </td> 
   <td colname="col2"> <p>Colorizza l'armadio e/o la texture. </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> Sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Opzioni. </p> </td> 
   <td colname="col3"> <p>0 (nessuna nitidezza) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> flags= </span> </a> </p> </td> 
   <td colname="col2"> <p>Flag di rendering speciali. </p> </td> 
   <td colname="col3"> <p>0 (nessun flag) </p> </td> 
  </tr> 
 </tbody> 
</table>
