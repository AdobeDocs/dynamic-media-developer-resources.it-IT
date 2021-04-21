---
description: Consente agli amministratori di creare nuovi campi di metadati da coordinare con i sistemi di gestione dei contenuti o per le operazioni sui modelli. Esempi di campi di metadati creati includono parole chiave, informazioni sull’autore dell’immagine o informazioni sul titolare del copyright.
solution: Experience Manager
title: createMetadataField
feature: Dynamic Media Classic,SDK/API,Metadata
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 7%

---


# createMetadataField{#createmetadatafield}

Consente agli amministratori di creare nuovi campi di metadati da coordinare con i sistemi di gestione dei contenuti o per le operazioni sui modelli. Esempi di campi di metadati creati includono parole chiave, informazioni sull’autore dell’immagine o informazioni sul titolare del copyright.

Sintassi

## Tipi di utenti autorizzati {#section-2f61d79f8cac4692bfa53b95035ddd89}

* `IpsAdmin`

## Parametri {#section-f8260bc8dd0a4570bc7f714f81ab975f}

**Input (createMetadataFieldParam)**

<table id="table_E5B249BBED3B4D2F9CEE2CCF27472D1B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome parametro </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obbligatorio </th> 
   <th colname="col4" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome della società a cui appartiene il campo metadati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Tipo di risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome del campo metadati che si sta creando. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4">Tipo di campo metadati. <p>La costante dei tipi di campo metadati definisce i tipi disponibili. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Il valore predefinito del campo metadati da creare (ad esempio, <span class="codeph"> Scene 7</span>). </p> <p>I valori predefiniti non sono supportati per i tipi di campi tag e devono essere omessi. Se per un tipo di campo tag è specificato un valore predefinito non vuoto, viene restituito un errore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> isHidden</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Nascondere o esporre metadati specifici del sistema IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforcement</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Flag booleano che indica se il campo metadati è applicato (convalidato) quando il valore è impostato. </p> <p>Se è impostato su true, viene generato un errore se un valore non valido è impostato in <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Consente di creare un set di valori enumerati condivisi a cui possono fare riferimento i tag selezionati. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createMetadataFieldReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`fieldHandle`*` | `xsd:string` | Sì | Il handle del nuovo campo metadati. |

## Esempi {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

Questo esempio di codice crea un campo metadati di tipo stringa denominato `createMetadataField`. La risposta restituisce l&#39;handle al nuovo campo metadati.

**Request Contents (Richiesta contenuto)**

```java
<createMetadataFieldParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <assetType>Image</assetType>
   <name>createMetadataField</name>
   <fieldType>String</fieldType>
   <initialTagValue>Fall</initialTagValue>
   <defaultValue>Default</defaultValue>
</createMetadataFieldParam>
```

**Risposta**

```java
<createMetadataFieldReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <fieldHandle>m|21|IMAGE|createMetadataField</fieldHandle>
</createMetadataFieldReturn>
```

