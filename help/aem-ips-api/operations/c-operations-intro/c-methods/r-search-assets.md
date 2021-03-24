---
description: Cerca le risorse in base ai criteri specificati.
solution: Experience Manager
title: searchAssets
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 6%

---


# searchAssets{#searchassets}

Cerca le risorse in base ai criteri specificati.

Sintassi

## searchAssets: Informazioni su {#section-4ad74f12eb754768bf85bd235a7e25f0}

`searchAssets` è il metodo principale per recuperare le risorse IPS. Questo metodo viene utilizzato per vari scopi, ad esempio per sfogliare la gerarchia delle cartelle o trovare una risorsa specifica per nome.

**Dimensione risposta**

`searchAssets` restituisce fino a 1000 risorse in una singola chiamata. Per restituire fino a 10.000 risorse per chiamata, limita i dati di risposta a un sottoinsieme dei campi `totalRows`, `name`, `handle`, `type` e `subType`. Per restituire set più grandi, imposta il paging con il parametro `resultPage` .

**Limita le dimensioni del file dei risultati con responseFieldArray o excludeFieldArray**

Limita le dimensioni del set di dati con i parametri `responseFieldArray` o `excludFieldArray` . Questi parametri contribuiscono a ridurre l&#39;utilizzo della memoria e della larghezza di banda e possono migliorare i tempi di risposta del server.

## Tipi di utenti autorizzati {#section-9c4bc41bb8b4493982197eb13c7cdc55}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura per restituire le risorse.

## Parametri {#section-49aabc0600764f55a8b7017d86ded44f}

**Input (searchAssetsParam)**

<table id="table_2972D1BB9CED4F7F9207747AE8CBAE8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obbligatorio? </th> 
   <th colname="col4" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> L’handle dell’azienda con le risorse da cercare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessUserHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Consente agli amministratori di lavorare come un altro utente. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> accessGroupHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Consente agli amministratori di lavorare come parte di un gruppo diverso. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cartella</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Percorso principale per la ricerca delle risorse. Se omesso, verrà utilizzata la cartella principale della società. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> includeSubfolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Impostare su <span class="codeph"> true</span> per cercare le sottocartelle. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> publishState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Selezione dello stato di pubblicazione. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> trashState</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Scelta dello stato del cestino. Il valore predefinito è <span class="codeph"> NotInTrash</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> conditionMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Scelta delle modalità di corrispondenza della ricerca per combinare i risultati di <span class="codeph"> keywordArray</span>, </p> <p> <span class="codeph"> conditionMatchMode</span> </p> <p> <span class="codeph"> systemFieldConditionArray</span> e  <span class="codeph"> metadataConditionArray</span>. Il valore predefinito è <span class="codeph"> MatchAll</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> keywordArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p> <p>Nota:  Parametro obsoleto. Si consiglia di non utilizzarlo. </p> </p> <p>Matrice di stringhe di parole chiave da abbinare. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> systemFieldMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Scelta delle modalità di corrispondenza della ricerca per combinare le corrispondenze di <span class="codeph"> systemFieldCondition</span> . Il valore predefinito è <span class="codeph"> MatchAll</span> </p>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> systemFieldConditionArray</span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipi:SystemFieldConditionArray</span> </p> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matrice di condizioni del campo di sistema. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Costanti stringa in modalità di corrispondenza ricerca. Il valore predefinito è <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> tagConditionArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:TagConditionArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Matrice di predicati per la ricerca di campi di tag. </p> <p>I predicati vengono combinati in base all'impostazione <span class="codeph"> tagMatchMode</span> e quindi combinati con qualsiasi termine in <span class="codeph"> keywordArray</span>, <span class="codeph"> systemFieldConditionArray</span> e <span class="codeph"> metadataConditionArray</span> in base all'impostazione <span class="codeph"> conditionMatchMode</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataMatchMode</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Modalità di corrispondenza ricerca per combinare le corrispondenze di <span class="codeph"> metadataCondition</span> . Il valore predefinito è <span class="codeph"> MatchAll</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> metadataConditionArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipi:MetadataConditionArray</span> </p> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Matrice di condizioni di ricerca dei campi di metadati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Array di tipi di risorse da includere nella ricerca. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeAssetTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Array di tipi di risorse da escludere dalla ricerca. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSubTypeArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Elenco di nomi di sottotipo su cui eseguire il filtro. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> narrowSubTypeCheck</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Se <span class="codeph"> true</span> e <span class="codeph"> assetSubTypeArray</span> non è vuoto, vengono restituite solo le risorse i cui sottotipi sono in <span class="codeph"> assetSubTypeArray</span>. Se <span class="codeph"> false</span> (predefinito), vengono restituite risorse senza sottotipo definito. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeByproducts</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Se true, le risorse per sottoprodotto generate durante l’assimilazione di una risorsa principale, come le immagini di una pagina PDF strappata, sono escluse dai risultati della ricerca. Il valore predefinito è false. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludByproductArray</span> </span> </td> 
   <td colname="col2"> <p> <span class="codeph"> tipi:ExcludeByproductArray</span> </p> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Array di condizioni di generazione delle risorse per sottoprodotto da escludere dai risultati della ricerca. Se presente, questo parametro sostituisce l’impostazione excludeByproducts . </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> projectHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Gestione di un progetto contenente le risorse da cercare. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> recordsPerPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Numero massimo di risultati da restituire. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> resultPage</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Specifica la pagina dei risultati da restituire, in base alle dimensioni della pagina <span class="codeph"> recordsPerPage</span>. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortBy</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Scelta dei campi di ordinamento delle risorse. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> sortDirection</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Scelta del tipo di direzione. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> responseFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Contiene un elenco di campi e sottocampi da includere nella risposta. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excludeFieldArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:StringArray</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Contiene un elenco di campi e sottocampi da escludere dalla risposta. </td> 
  </tr> 
 </tbody> 
</table>

**Output (searchAssetsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`totalRows`*` | `xsd:int` | No | Numero di righe restituite da una ricerca quando i record per pagina non sono limitati. |
| `*`assetArray`*` | `types:AssetArray` | No | Risorse restituite dalla ricerca. |

## Esempi {#section-725484cc09b54772a838ad2cc930b94b}

Questo esempio di codice cerca le risorse di immagini che appartengono a una società specifica. La risposta viene troncata per brevità.

**Request Contents (Richiesta contenuto)**

```java
<ns1:searchAssetsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:includeSubfolders>true</ns1:includeSubfolders>
   <ns1:assetTypeArray>
      <ns1:items>Image</ns1:items>
   </ns1:assetTypeArray>
</ns1:searchAssetsParam>
```

**Risposta**

```java
<searchAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <totalRows>210</totalRows>
   <assetArray>
      <items>
         <assetHandle>24265|1|17061</assetHandle>
         <type>Image</type>
         <name>Autumn Leaves</name>
         ...
      </items>
    </assetArray>
</searchAssetsReturn>
```

