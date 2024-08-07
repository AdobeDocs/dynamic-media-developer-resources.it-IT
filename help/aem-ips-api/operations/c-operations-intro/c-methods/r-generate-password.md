---
description: Genera una nuova password.
solution: Experience Manager
title: generatePassword
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 80e7642f-4aec-4ff0-a090-e59b7a065c39
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '59'
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
