---
description: Raggruppa i file in set utilizzando una matrice di elenchi di handle di risorsa.
solution: Experience Manager
title: AttivitàGenerazioneAutomatizzata
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '183'
ht-degree: 3%

---


# AutomatedSetGenerationJob{#automatedsetgenerationjob}

Raggruppa i file in set utilizzando una matrice di elenchi di handle di risorsa.

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetHandleArray</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:HandleArray</span> </td> 
   <td colname="col3">Matrice di handle di risorsa utilizzata per creare il set. <p>Per impostazione predefinita, 1000 è il numero massimo di risorse disponibili nell’array. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> destFolder</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Percorso della cartella in cui salvare i set. Salva nella cartella principale della società per impostazione predefinita. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> readyForPublish</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> Imposta un flag per indicare se le risorse devono essere pubblicate o meno. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> autoSetCreationOptions</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:AutoSetCreationOptions</span> </td> 
   <td colname="col3">Matrice di script di generazione del set che è possibile eseguire sui file caricati. Vedere <a href="../../types/c-data-types/r-auto-set-creation-options.md#reference-58b42b39e53345aeb87cd1adc864e7ff" format="dita" scope="local"> AutoSetCreationOptions</a></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> emailSetting</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> <p>Imposta una notifica e-mail automatica per il processo. </p> </td> 
  </tr> 
 </tbody> 
</table>

**Opzioni e-mailSetting**

Il parametro `emailSetting` include le seguenti opzioni:

| Opzione | Restituisce |
|---|---|
| `All` | Tutte le notifiche di processo (errori, avvisi, completamento) al destinatario specificato. |
| `Error` | Errori di processo nel destinatario specificato. |
| `ErrorAndWarning` | Errori di processo e avvisi al destinatario specificato. |
| `JobCompletion` | Una notifica di completamento del processo al destinatario specificato. |
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

