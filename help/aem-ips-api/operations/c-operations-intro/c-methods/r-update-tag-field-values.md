---
description: Aggiorna i valori del dizionario tag per un campo tag.
solution: Experience Manager
title: updateTagFieldValues
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 6de49217-2d15-49d9-9357-b058b2564686
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 11%

---

# updateTagFieldValues{#updatetagfieldvalues}

Aggiorna i valori del dizionario tag per un campo tag.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> companyHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Gestore azienda. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fieldHandle</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:stringa</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Handle campo tag. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> updateArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:TagValueUpdateArray</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4">Matrice di valori dei campi tag che si desidera aggiornare. <p>Nota: aggiorna solo i valori delle stringhe di tag. Non influisce sulle associazioni di risorse. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Output (updateTagFieldValuesReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | `xsd:int` | Sì | Numero di campi tag aggiornati correttamente. |
| warningCount | `xsd:int` | Sì | Numero di avvisi generati quando l’operazione ha tentato di aggiornare i campi tag. |
| errorCount | `xsd:int` | Sì | Il numero di errori generati quando l’operazione ha tentato di aggiornare i campi tag. |
| warningDetailArray | `types:TagValueUpdateFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione ha tentato di aggiornare i campi tag. |
| errorDetailArray | `types:TagValueUpdateFaultArray` | No | Array di dettagli associati alle risorse che hanno generato errori quando l’operazione ha tentato di aggiornare i campi tag. |

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

```java {.line-numbers}
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
