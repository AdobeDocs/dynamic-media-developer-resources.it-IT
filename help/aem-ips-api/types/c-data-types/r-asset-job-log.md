---
title: RegistroProcessiRisorse
description: Dettagli di una voce del registro processi associata a una particolare risorsa. Dati restituiti da getAssetJobLogs.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 2c8ebec2-a664-46cd-b843-9893bfa0a9d1
TQID: 'https://experienceleague.adobe.com/WUS-oaI47IowEv60EpzEMZnd-euKdN-YTVfCS3-DSvo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 89
ht-degree: 3%

---

# [!DNL AssetJobLog]{#assetjoblog}

Dettagli di una voce del registro processi associata a una particolare risorsa. Dati restituiti da getAssetJobLogs.

Sintassi

## Parametri {#section-5da4d6156b7f4ca88a67202fbf736104}

<table id="table_7BC785BC95EA43D582D1B2289FF3130D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> Nome </th> 
   <th colname="col2" class="entry"> Tipo </th> 
   <th colname="col3" class="entry"> Descrizione </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL jobHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Handle di processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL jobName]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Nome processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL logMessage]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">Messaggio nel registro del processo. <p>Il campo di risposta <span class="codeph"> [!DNL logMessage]</span> è localizzato in base al campo locale <span class="codeph"> authHeader</span>. </p></td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL logType]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Tipo di processo nella voce del registro. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL submitUserEmail]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> e-mail dell’utente che ha inviato il processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL logDate]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> Data processo. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL auxArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> tipi:JobLogDetailArray</span> </td> 
   <td colname="col3"> Array di messaggi del registro di processo ausiliari per ogni registro di processo. </td> 
  </tr> 
 </tbody> 
</table>
