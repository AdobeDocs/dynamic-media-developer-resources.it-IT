---
description: Aggiunge un termine di ricerca da usare con searchAssets.
seo-description: Aggiunge un termine di ricerca da usare con searchAssets.
seo-title: MetadataCondition
solution: Experience Manager
title: MetadataCondition
topic: Scene7 Image Production System API
uuid: 9d65b8ce-86a5-4730-af84-a87134fd7db6
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# MetadataCondition{#metadatacondition}

Aggiunge un termine di ricerca da usare con searchAssets.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

<table id="table_04100BB8ABD84EF68B0A7CE3AD946414"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Maniglia del campo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> op</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Scelta degli operatori di confronto delle stringhe. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> value</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Valore da verificare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> boolVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Valore di confronto booleano (solo per i campi con tipo booleano). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> longVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Valore di confronto lungo (solo per i campi con tipo int). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minLong</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Valore minimo lungo nel confronto degli intervalli (solo per i campi con tipo int). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxLong</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:long</span> </td> 
   <td colname="col3"> Valore massimo lungo nel confronto degli intervalli (solo per i campi con tipo int). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> doubleVal</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> Valore di confronto doppio (solo per i campi con tipo mobile). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minDouble</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> Valore doppio minimo nel confronto degli intervalli (solo per i campi con tipo mobile). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxDouble</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:double</span> </td> 
   <td colname="col3"> Valore doppio massimo nel confronto degli intervalli (solo per i campi con tipo mobile). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> dateValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Valore di confronto delle date (solo per i campi con tipo data). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> minDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Valore data minimo nel confronto dell'intervallo (solo per i campi con tipo data). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> maxDate</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Valore data massimo nel confronto tra intervalli (solo per i campi con tipo data). </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> con distinzione tra maiuscole e minuscole</span></span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> <p> Stabilisce la distinzione tra maiuscole e minuscole per il server di metadati. Utilizzata nella chiamata <span class="codeph"> searchAssetsByMetadata</span> . </p> <p>Consulta <a href="../../operations/c-operations-intro/c-methods/r-search-assets-by-metadata.md#reference-609ec73944a34ce49b152389fbb40414" format="dita" scope="local"> searchAssetsByMetadata</a>. </p> </td> 
  </tr> 
 </tbody> 
</table>

