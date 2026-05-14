---
description: Genera una nuova password.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
TQID: 'https://experienceleague.adobe.com/3XFwGq8wAf81wEUfaUrcDiI03MNe0bhMCBdV-5LDfoQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 59
ht-degree: 8%

---

# generatePassword{#generatepassword}

Genera una nuova password.

Sintassi

## Tipi di utenti autorizzati {#section-88f7dc11e5c74be281399d8f2e3c9555}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-d516615c906240819a284786efb19863}

**Input (generatePasswordParam)**

Nessuno.

**Output (generatePasswordParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| password | `xsd:string` | Sì | Una nuova password. |

## Esempi {#section-f580fefdccec46fe95359e3aef0ed17f}

Questo esempio di codice genera una password. È insolito perché la richiesta è semplicemente un parametro senza elementi o valori racchiusi. IPS restituisce una password complessa.

**Richiesta**

```java
<generatePasswordParam xmlns="http://www.scene7.com/IpsApi/xsd">
</generatePasswordParam>
```

**Risposta**

```java
<generatePasswordReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <password>1\7aQRn]</password>
</generatePasswordReturn>
```
