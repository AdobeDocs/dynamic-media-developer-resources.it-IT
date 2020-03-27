---
description: Consente agli amministratori di creare nuovi campi di metadati da coordinare con i sistemi di gestione dei contenuti o per le operazioni sui modelli. Alcuni esempi di campi di metadati creati includono parole chiave, informazioni sull’autore dell’immagine o informazioni sul titolare del copyright.
seo-description: Consente agli amministratori di creare nuovi campi di metadati da coordinare con i sistemi di gestione dei contenuti o per le operazioni sui modelli. Alcuni esempi di campi di metadati creati includono parole chiave, informazioni sull’autore dell’immagine o informazioni sul titolare del copyright.
seo-title: createMetadataField
solution: Experience Manager
title: createMetadataField
topic: Scene7 Image Production System API
uuid: 50ab61fa-df44-4305-ad9f-693c4aea1e69
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# createMetadataField{#createmetadatafield}

Consente agli amministratori di creare nuovi campi di metadati da coordinare con i sistemi di gestione dei contenuti o per le operazioni sui modelli. Alcuni esempi di campi di metadati creati includono parole chiave, informazioni sull’autore dell’immagine o informazioni sul titolare del copyright.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome della società a cui appartiene il campo di metadati. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Tipo di risorsa. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> name</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Nome del campo di metadati che si sta creando. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldType</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4">Tipo di campo metadati. <p>La costante dei tipi di campo di metadati definisce i tipi disponibili. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> defaultValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> <p>Il valore predefinito del campo di metadati da creare (ad esempio, <span class="codeph"> Scene7</span>). </p> <p>I valori predefiniti non sono supportati per i tipi di campo tag e devono essere omessi. Se per un tipo di campo di tag è specificato un valore predefinito non vuoto, verrà restituito un errore. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> is Hidden</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Nascondere o esporre i metadati specifici del sistema IPS. </td> 
  </tr> 
  <tr> 
   <td colname="col1"><span class="codeph"><span class="varname"> isEnforzato</span></span> </td> 
   <td colname="col2"><span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> <p>No </p> </td> 
   <td colname="col4"> <p>Flag booleano che indica se il campo di metadati viene applicato (convalidato) quando il valore viene impostato. </p> <p>Se è impostato su true, viene generato un errore se un valore non valido è impostato in <span class="codeph"> setAssetMetadata</span> /<span class="codeph"> batchSetAssetMetadata</span>. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> initialTagValue</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4"> Consente di creare un set di valori enumerati condivisi a cui i tag selezionati possono puntare. </td> 
  </tr> 
 </tbody> 
</table>

**Output (createMetadataFieldReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`fieldHandle`*` | `xsd:string` | Sì | handle del nuovo campo di metadati. |

## Esempi {#section-ba66be30f36b4aeba1bc721b0b92fdfc}

Questo esempio di codice crea un campo di metadati di tipo stringa denominato `createMetadataField`. La risposta restituisce la maniglia al nuovo campo di metadati.

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

