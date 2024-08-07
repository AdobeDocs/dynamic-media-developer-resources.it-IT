---
description: Elimina un formato di pubblicazione vignettatura.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: a437cb47-c45c-41a0-8499-53e4c2ae3164
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '75'
ht-degree: 8%

---

# deleteVignettePublishFormat{#deletevignettepublishformat}

Elimina un formato di pubblicazione vignettatura.

## Tipi di utenti autorizzati {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-789625ba29df4b5f880914d4c64f77ce}

**Input (deleteVignettePublishFormatParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Handle dell&#39;azienda a cui appartiene la vignettatura. |
| vignetteFormatHandle | `xsd:string` | Sì | Handle del formato di pubblicazione vignettatura da eliminare. |

**Output (deleteVignettePublishFormatParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

In questo esempio di codice viene eliminato un formato di pubblicazione vignettatura specificato dal relativo handle.

**Richiesta**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Risposta**

Nessuno.
