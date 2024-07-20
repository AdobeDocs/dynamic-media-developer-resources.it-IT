---
description: Raggruppare i file in set utilizzando una matrice di elenchi di handle di risorsa.
solution: Experience Manager
title: Processo di generazione automatizzata dei set
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 44df6dfa-1485-40c2-8a14-bbf451b87641
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---

# [!DNL AutomatedSetGenerationJob]{#automatedsetgenerationjob}

Raggruppare i file in set utilizzando una matrice di elenchi di handle di risorsa.

Sintassi

## Parametri {#section-939b2e6946a64238be3709fec2cd0b84}

<table id="table_0E031B2014B646BDA2A94D7E0B55DD5B"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetHandleArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:HandleArray</span> </td> 
   <td colname="col3">Array di handle di risorsa utilizzati per creare il set. <p>Per impostazione predefinita, 1000 è il numero massimo di risorse che è possibile avere nell’array. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL destFolder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Percorso della cartella in cui desideri salvare i set. Salva nella cartella principale della società per impostazione predefinita. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:booleano</span> </td> 
   <td colname="col3"> Imposta un flag per indicare se le risorse devono essere pubblicate o meno. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL autoSetCreationOptions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Matrice di script per la generazione di set eseguibili sui file caricati. Vedere <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL emailSetting]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Imposta una notifica e-mail automatica per il processo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**opzioni emailSetting**

Il parametro `emailSetting` include le opzioni seguenti:

| Opzione | Restituisce |
|---|---|
| `All` | Tutte le notifiche di processo (errori, avvisi, completamento) al destinatario specificato. |
| `Error` | Errori di processo per il destinatario specificato. |
| `ErrorAndWarning` | Errori di processo e avvisi al destinatario specificato. |
| `JobCompletion` | Notifica di completamento del processo al destinatario specificato. |
| `None` | Il processo non invia alcuna notifica di processo al destinatario specificato. |

## Esempio {#section-d01ee7671f274a1fa12737e8df91d2cf}

```
<complexType name="AutomatedSetGenerationJob">
  <sequence>
    <element name="assetHandleArray" type="types:HandleArray"/>
    <element name="destFolder" type="xsd:string" minOccurs="0"/>
    <element name="readyForPublish" type="xsd:boolean"/>
    <element name="autoSetCreationOptions" type="types:AutoSetCreationOptions"/>
    <element name="emailSetting" type="xsd:string"/>
  </sequence>
</complexType>
```
