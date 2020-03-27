---
description: I materiali dei cabinet specificano un file di stile cabinet (estensione .vnc), un file di dati speciale contenente rappresentazioni fotografiche di cabinet insieme alle definizioni di layout parametrico e altre informazioni necessarie per il rendering dei frontali dei cabinet.
seo-description: I materiali dei cabinet specificano un file di stile cabinet (estensione .vnc), un file di dati speciale contenente rappresentazioni fotografiche di cabinet insieme alle definizioni di layout parametrico e altre informazioni necessarie per il rendering dei frontali dei cabinet.
seo-title: Scaffali
solution: Experience Manager
title: Scaffali
topic: Scene7 Image Serving - Image Rendering API
uuid: d515c613-07c5-49ef-ad6e-568a1f6c1335
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Scaffali{#cabinets}

I materiali dei cabinet specificano un file di stile cabinet (estensione .vnc), un file di dati speciale contenente rappresentazioni fotografiche di cabinet insieme alle definizioni di layout parametrico e altre informazioni necessarie per il rendering dei frontali dei cabinet.

[!DNL vnc] i file possono includere una texture di grana di legno ripetibile, oppure la texture può essere fornita esternamente tramite un secondo argomento a `src=`. Alcuni [!DNL vnc] file consentono la colorazione o la texture di aree selezionate di frontali di armadio (tipicamente utilizzati per gli stili di cabinet laminati).

I materiali del cabinet possono essere applicati solo agli oggetti del cabinet.

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
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>file di stile del cabinet; obbligatorio. </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span></a> </p> </td> 
   <td colname="col2"> <p>File immagine texture opzionale (secondo valore per <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span></a> </p> </td> 
   <td colname="col2"> <p>Risoluzione texture opzionale. </p> </td> 
   <td colname="col3"> <p> <span class="codeph"> attribute:Resolution </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> color= </span></a> </p> </td> 
   <td colname="col2"> <p>Colora il cabinet e/o la texture. </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span></a> </p> </td> 
   <td colname="col2"> <p>Opzioni. </p> </td> 
   <td colname="col3"> <p>0 (nessuna nitidezza) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> flags= </span></a> </p> </td> 
   <td colname="col2"> <p>Flag di rendering speciali. </p> </td> 
   <td colname="col3"> <p>0 (nessun flag) </p> </td> 
  </tr> 
 </tbody> 
</table>

