---
title: setContainerId
description: Guida di riferimento dell’API JavaScript per il visualizzatore video Ritaglio avanzato.
solution: Experience Manager, Experience Manager Assets
feature-set: Experience Manager, Experience Manager Assets
feature: Dynamic Media Classic,Viewers,SDK/API,Smart Crop,Video
role: Developer,User
exl-id: 1c7a7494-e872-4e78-9518-ea30af46303c
TQID: 'https://experienceleague.adobe.com/cMIps3ogqL1H3zF8XwHTPB3XYYYQocbVwCNHx5-JluM'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
    internal-label: Experience Manager
  - id: d09181b5-a36a-43de-ba01-36641440bc43
    internal-label: Experience Manager Assets
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
    internal-label: APIs
  - id: fe490c45-63fa-5b99-b5b4-d8cfeda8aa7d
    internal-label: SDK/API
  - id: bd0d2470-932c-4269-8eca-6d939b72d9ef
    internal-label: Dynamic Media
  - id: d4b6216b-4a89-4ff0-8ac0-5a699ba23100
    internal-label: Images and videos
subfeature_v2:
  - id: c12bda38-aa1a-4647-b62e-42cd4537dac6
    internal-label: Dynamic Media Classic
  - id: d17d085a-e808-49dd-b9a6-85a996b999bd
    internal-label: Viewers
  - id: a0cde32c-c339-4649-bd06-f1111bc952fc
    internal-label: Smart Crop
  - id: cb04d42d-1b70-43b0-9951-45998eb6e842
    internal-label: Video
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
source-git-commit: 0e24e07f8c91d3e7fda5510ed4252f9953e27467
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 1%
---
# setContainerId{#setcontainerid}

Guida di riferimento dell’API JavaScript per il visualizzatore video Ritaglio avanzato.

` setContainerId( *`containerId`*)`

Imposta l&#39;ID del contenitore DOM (in genere `DIV`) in cui viene inserito il visualizzatore. Non è necessario creare l’elemento contenitore nel momento in cui viene chiamato questo metodo. Tuttavia, il contenitore deve esistere quando viene eseguito `init()`. Questo parametro viene chiamato prima di `init()`. Questo metodo è facoltativo se le informazioni di configurazione del visualizzatore vengono passate con l&#39;oggetto JSON `config` al costruttore.

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> ID contenitore </span> </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> {string} </span> ID del contenitore. </p> </td> 
  </tr> 
 </tbody> 
</table>

## Restituisce {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

Nessuno.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setContainerId("s7viewer");
```
