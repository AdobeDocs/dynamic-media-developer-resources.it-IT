---
description: Aggiorna i valori dei dizionari di tag per un campo di tag.
seo-description: Aggiorna i valori dei dizionari di tag per un campo di tag.
seo-title: updateTagFieldValues
solution: Experience Manager
title: updateTagFieldValues
topic: Scene7 Image Production System API
uuid: 21689469-a0dd-480b-82ba-ebd12956ff8f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# updateTagFieldValues{#updatetagfieldvalues}

Aggiorna i valori dei dizionari di tag per un campo di tag.

Sintassi

## Tipi di utenti autorizzati {#section-0372b742b1344979b0668faacb36fcc6}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-0a3a4bab026746238c9d4009caf42e94}

**Input (updateTagFieldValuesParam)**

<table id="table_15F354FBC043464080BC975AE35E03A4"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Obbligatorio </th> 
   <th colname="col4" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Maniglia aziendale. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> handle del campo del tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:TagValueUpdateArray</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4">Matrice di valori dei campi di tag da aggiornare. <p>Nota:  Aggiorna solo i valori delle stringhe di tag. Non influenza le associazioni di risorse. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (updateTagFieldValuesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`successCount`*` | `xsd:int` | Sì | Numero di campi tag aggiornati correttamente. |
| ` *`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l&#39;operazione tentava di aggiornare i campi tag. |
| ` *`errorCount`*` | `xsd:int` | Sì | Il numero di errori generati quando l&#39;operazione tentava di aggiornare i campi tag. |
| ` *`warningDetailArray`*` | `types:TagValueUpdateFaultArray` | No | Array di dettagli associati alle risorse che generavano avvisi quando l&#39;operazione tentava di aggiornare i campi tag. |
| ` *`errorDetailArray`*` | `types:TagValueUpdateFaultArray` | No | L&#39;array di dettagli associati alle risorse che generavano errori quando l&#39;operazione tentava di aggiornare i campi tag. |

## Esempi {#section-bb4dcf97044c4675974c9b8d27674001}

**Request Contents (Richiesta contenuto)**

```java
<updateTagFieldValuesParam xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <companyHandle>c|3</companyHandle>
   <fieldHandle>m|3|ASSET|SingleFixedTag</fieldHandle>
   <updateArray>
      <items>
         <oldValue>Nurth</oldValue>
         <newValue>North</newValue>
      </items>
      <items>
         <oldValue>Suth</oldValue>
         <newValue>South</newValue>
      </items>
      <items>
         <oldValue>East</oldValue>
         <newValue>West</newValue>
      </items>
      <items>
         <oldValue>Banana</oldValue>
         <newValue>Pear</newValue>
      </items>
   </updateArray>
</updateTagFieldValuesParam>
```

**Risposta**

```java
<updateTagFieldValuesReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <successCount>2</successCount>
   <warningCount>0</warningCount>
   <errorCount>2</errorCount>
   <errorDetailArray>
      <items>
         <value>East</value>
         <code>30001</code>
         <reason>New tag value 'West' already exists.</reason>
      </items>
      <items>
         <value>Banana</value>
         <code>30001</code>
         <reason>Tag value 'Banana' not found.</reason>
      </items>
   </errorDetailArray>
</updateTagFieldValuesReturn>
```

