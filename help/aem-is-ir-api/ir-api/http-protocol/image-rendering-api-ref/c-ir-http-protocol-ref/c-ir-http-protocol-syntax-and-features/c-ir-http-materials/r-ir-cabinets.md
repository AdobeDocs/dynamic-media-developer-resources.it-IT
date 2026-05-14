---
title: Archivi
description: I materiali dei cabinet specificano un file di stile (estensione .vnc), un file di dati speciale contenente le rappresentazioni fotografiche dei cabinet insieme alle definizioni di layout parametrico e altre informazioni necessarie per il rendering dei frontali dei cabinet.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: cdb3ed5e-c396-483d-aea0-2b3f24efe56e
TQID: 'https://experienceleague.adobe.com/SzkFcvt2K-pHseOvk42kwWVaIl2-BnQK8aSEwSTB9zA'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 159
ht-degree: 1%

---

# Archivi{#cabinets}

I materiali dei cabinet specificano un file di stile (estensione .vnc), un file di dati speciale contenente le rappresentazioni fotografiche dei cabinet insieme alle definizioni di layout parametrico e altre informazioni necessarie per il rendering dei frontali dei cabinet.

I file [!DNL vnc] possono includere una trama a grana di legno ripetibile oppure la trama può essere fornita esternamente tramite un secondo argomento a `src=`. Alcuni file [!DNL vnc] consentono di colorare o texture aree selezionate della facciata di un cabinet (in genere utilizzato per gli stili di cabinet laminati).

I materiali di scaffale possono essere applicati solo agli oggetti di scaffale.

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
   <td colname="col2"> <p>File di stile archivio; obbligatorio. </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-src.md#reference-62c98abad22149d68d405ed6aaff8272" type="reference" format="dita" scope="local"> <span class="codeph"> src= </span> </a> </p> </td> 
   <td colname="col2"> <p>File immagine di trama facoltativo (secondo valore per <span class="codeph"> src= </span>). </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-res.md#reference-0ad9de8887144c83a6db97b4994f7c04" type="reference" format="dita" scope="local"> <span class="codeph"> res= </span> </a> </p> </td> 
   <td colname="col2"> <p>Risoluzione opzionale della texture. </p> </td> 
   <td colname="col3"> <p> Attributo <span class="codeph">::Risoluzione </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-color.md#reference-ea3cba9edfe94dbab86d8f123a9ed0aa" type="reference" format="dita" scope="local"> <span class="codeph"> colore= </span> </a> </p> </td> 
   <td colname="col2"> <p>Colora il cabinet e/o la texture. </p> </td> 
   <td colname="col3"> <p>Nessuno. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-http-sharp.md#reference-acdd87f6b5de4e3a85e5d3c03022a35a" type="reference" format="dita" scope="local"> <span class="codeph"> sharp= </span> </a> </p> </td> 
   <td colname="col2"> <p>Nitidezza. </p> </td> 
   <td colname="col3"> <p>0 (nessuna nitidezza) </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <a href="../../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-flags.md#reference-3a4844f0f21346d79e6508aaad9a9ac9" type="reference" format="dita" scope="local"> <span class="codeph"> flag= </span> </a> </p> </td> 
   <td colname="col2"> <p>Flag di rendering speciali. </p> </td> 
   <td colname="col3"> <p>0 (nessun flag) </p> </td> 
  </tr> 
 </tbody> 
</table>
