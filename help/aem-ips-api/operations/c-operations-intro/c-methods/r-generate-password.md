---
description: Genera una nuova password.
seo-description: Genera una nuova password.
seo-title: generatePassword
solution: Experience Manager
title: generatePassword
topic: Dynamic Media Image Production System API
uuid: e3367bfc-d437-4a61-83e8-69830154dc61
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 15%

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
| `*`password`*` | `xsd:string` | Sì | Una nuova password. |

## Esempi {#section-f580fefdccec46fe95359e3aef0ed17f}

Questo esempio di codice genera una password. È insolito perché la richiesta è semplicemente un parametro senza elementi o valori racchiusi. IPS restituisce una password complessa.

**Request Contents (Richiesta contenuto)**

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

