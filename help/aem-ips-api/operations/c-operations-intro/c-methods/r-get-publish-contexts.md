---
title: getPublishContexts
description: getPublishContexts
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7b26e659-71b9-40c4-9df4-94e78c3e4baf
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 13%

---

# getPublishContexts{#getpublishcontexts}

Sintassi

## Tipi di utenti autorizzati {#section-1a3a50349b5640dd8e498ff9e9c37340}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>* Per restituire le risorse, l’utente deve disporre dell’accesso in lettura.
>* Tutti gli utenti hanno accesso alla società condivisa.
>

## Parametri {#section-d08e2175d3f84774b55b91bc590b8b3f}

**Input (getPublishContextsParam)**

<table id="table_4A505A067586464B99F8F68E3B1BE75E"> 
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
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> Sì </td> 
   <td colname="col4"> Gestire l'azienda. </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> contextType</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> No </td> 
   <td colname="col4">Tipo di contesto di pubblicazione che si desidera restituire. Include: 
    <ul id="ul_21EDF8F0026E402EAE8226A0CADEE652">
     <li id="li_06DB502952D943198F16C06C59816268"><span class="codeph"> ImageServer</span></li>
     <li id="li_E67A42934E8F4689A148CE125F7372AE"><span class="codeph"> ImageRendering</span></li>
     <li id="li_3CB3A9C4E7AB4A71819567A9566E396C"><span class="codeph"> Video</span></li>
     <li id="li_27E3DB89B53B4B50B2231622A157A228"><span class="codeph"> DirectoryServer</span></li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

**Output (getPublishContextsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| publishContextArray | tipi:PublishContextArray | Sì | Matrice di contesti di pubblicazione per un’azienda, filtrati per tipo di contesto, se necessario. |

## Esempi {#section-23fb7d6a15004b7eb4c3d3bcb37ceb04}

**Richiesta**

```java
<getPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
</getPublishContextsParam>
```

**Risposta**

```java
<getPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
  <publishContextArray>
    <items>
      <contextHandle>pc|3001</contextHandle>
      <contextName>ImageRendering</contextName>
      <contextType>ImageRendering</contextType>
    </items>
    <items>
      <contextHandle>pc|3002</contextHandle>
      <contextName>ImageServing</contextName>
      <contextType>ImageServing</contextType>
    </items>
    <items>
      <contextHandle>pc|3003</contextHandle>
      <contextName>ServerDirectory</contextName>
      <contextType>ServerDirectory</contextType>
    </items>
    <items>
      <contextHandle>pc|3004</contextHandle>
      <contextName>Video</contextName>
      <contextType>Video</contextType>
    </items>
  </publishContextArray>
</getPublishContextsReturn>
```
