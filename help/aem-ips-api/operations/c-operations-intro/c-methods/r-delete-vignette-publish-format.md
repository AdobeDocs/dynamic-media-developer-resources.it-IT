---
description: Elimina un formato di pubblicazione della vignetta.
solution: Experience Manager
title: deleteVignettePublishFormat
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '82'
ht-degree: 12%

---


# deleteVignettePublishFormat{#deletevignettepublishformat}

Elimina un formato di pubblicazione della vignetta.

## Tipi di utenti autorizzati {#section-a127680d6b53462daaf2579d6f6fe5a8}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-789625ba29df4b5f880914d4c64f77ce}

**Input (deleteVignettePublishFormatParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;impugnatura dell&#39;azienda alla quale appartiene la vignetta. |
| `*`vignetteFormatHandle`*` | `xsd:string` | Sì | L&#39;handle del formato di pubblicazione della vignetta da eliminare. |

**Output (deleteVignettePublishFormatParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-5ab2a314ad4c41ac8b3a24eaea7d8585}

Questo esempio di codice elimina un formato di pubblicazione della vignetta specificato dal relativo handle.

**Request Contents (Richiesta contenuto)**

```java
<deleteVignettePublishFormatParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <vignetteFormatHandle>v|21|282</vignetteFormatHandle>
</deleteVignettePublishFormatParam>
```

**Risposta**

Nessuno.
