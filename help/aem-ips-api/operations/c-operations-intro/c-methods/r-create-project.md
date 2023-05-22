---
description: Crea un nuovo progetto.
solution: Experience Manager
title: createProject
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dd9c07df-9a8f-4b67-9838-31dd96fd127b
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 15%

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
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda associata al nuovo progetto. |
| projectName | `xsd:string` | Sì | Nome nuovo progetto. |

**Output (createProjectParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| projectHandle | `xsd:string` | Sì | Handle del nuovo progetto. |

## Esempi {#section-a0cd532b67e346d088fbec141231a0e5}

In questo esempio di codice viene creato un progetto denominato `ApiTestProject` in una società specificata dal relativo handle. La risposta restituisce l’handle al progetto.

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
