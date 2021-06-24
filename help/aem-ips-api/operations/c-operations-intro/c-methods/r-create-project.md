---
description: Crea un nuovo progetto.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 16%

---

# createProject{#createproject}

Crea un nuovo progetto.

Sintassi

## Tipi di utenti autorizzati {#section-17878e2e4c3a44988c9a1af82c2ac319}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-8c741884eb54489bbaad0c444fee80b6}

**Input (createProjectParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda associata al nuovo progetto. |
| `*`projectName`*` | `xsd:string` | Sì | Nuovo nome del progetto. |

**Output (createProjectParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`projectHandle`*` | `xsd:string` | Sì | L&#39;handle del nuovo progetto. |

## Esempi {#section-a0cd532b67e346d088fbec141231a0e5}

Questo esempio di codice crea un progetto denominato `ApiTestProject` in una società specificata dal relativo handle. La risposta restituisce l&#39;handle al progetto.

**Request Contents (Richiesta contenuto)**

```java
<createProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectName>ApiTestProject</projectName>
</createProjectParam>
```

```java
<createProjectReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <projectHandle>p|6|ApiTestProject</projectHandle>
</createProjectReturn>
```
