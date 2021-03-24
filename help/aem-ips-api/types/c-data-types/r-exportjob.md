---
description: Tipo di processo per consentire l’esportazione autorizzata di file caricati in precedenza.
solution: Experience Manager
title: ExportJob
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 10%

---


# ExportJob{#exportjob}

Tipo di processo per consentire l’esportazione autorizzata di file caricati in precedenza.

ExportJob non supporta i seguenti tipi di risorse:

* Set di immagini
* Set di rendering
* Set 360 gradi
* Set di file multimediali
* Set con bitrate multiplo
* Set video
* eCatalog
* Set di offerte

<table id="table_D8F3FD30D15648BFA5B980D3DC0A5AB1"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipi:HandleArray</span> </p> </td> 
   <td colname="col3" valign="top"> <p>Elenco di <span class="codeph"> assetHandle</span> da esportare. Vedere <a href="../../types/c-data-types/r-handle-array.md#reference-1b93fefb5477459faf9253b54349b5f9" type="reference" format="dita" scope="local"> HandleArray</a>. </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> fmt</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>Specifica il tipo di <span class="codeph"> export.Possibili Valori</span>: [orig, convert] </p> <p> 
     <ul id="ul_16EF4B14100C4C7AA464CA9CF7F11D1C"> 
      <li id="li_DAB2844CC55145C88A18A1F8EC4527F9">Se <span class="codeph"> fmt=orig</span>, le risorse vengono esportate come originali </li> 
      <li id="li_07F2F8D159934D889FDC1022AB12B564">Se <span class="codeph"> fmt=convert</span>, le risorse vengono convertite nel formato specificato nei parametri di input <span class="codeph"> is_modifer</span> o <span class="codeph"> macro</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> is_modifier</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>Specifica la stringa URL di rendering <span class="codeph"> ImageServer</span>, che viene aggiunta alla richiesta ExportJob <span class="codeph"> convert</span>. </p> <p>Per informazioni sull'invio dei modificatori IS, fare riferimento alla <a href="https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/home.html" scope="external" format="html"> documentazione IS</a> . </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> macro</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p></p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>Scelta dell’impostazione e-mail. Valori possibili: </p> <p> 
     <ul id="ul_0EEDAE11B7CD4C53A6E4B2B8CB2CF730"> 
      <li id="li_F235F93828594ED78C6D464440F953FF"> <span class="codeph"> Tutto</span> </li> 
      <li id="li_59E14E7EBFA64432A5FAC15DA21A0521"> <span class="codeph"> Errore</span> </li> 
      <li id="li_BFE0B52CADD14CC1BA1AF42AB0AA1CE1"> <span class="codeph"> ErrorAndWarning</span> </li> 
      <li id="li_BE3AA67E14FB487B8B9CD6EF3D58824C"> <span class="codeph"> CompletamentoProcesso</span> </li> 
      <li id="li_409C68AD0D244975BFB86B08609E0146"> <span class="codeph"> Nessuno</span> </li> 
     </ul> </p> </td> 
  </tr> 
  <tr valign="top"> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> clientId</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> xsd:string  </span> </p> </td> 
   <td colname="col3"> <p>Specifica l'indirizzo IP del client o del cliente che ha avviato la richiesta di esportazione. </p> <p> <p>Nota:  questo parametro non è attualmente popolato attivamente ed è strettamente riservato solo per l'utilizzo futuro. </p> </p> </td> 
  </tr> 
 </tbody> 
</table>

Per le richieste ExportJob in cui sono forniti `fmt=convert` e `is_modifier` e `macro`, il file di destinazione rispetta il formato fornito da `macro`. Ad esempio:

```
input_file = fileToExport.jpg
is_modifer = &fmt=png
macro=$test$ 
output_file = fileToExport.tiff
```

