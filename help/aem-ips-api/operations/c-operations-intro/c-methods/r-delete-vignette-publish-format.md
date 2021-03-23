---
description: Elimina un formato di pubblicazione della vignetta.
seo-description: Elimina un formato di pubblicazione della vignetta.
seo-title: deleteVignettePublishFormat
solution: Experience Manager
title: deleteVignettePublishFormat
uuid: 3c8148d5-dec6-4ffa-8ab8-2cd70811ada6
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 11%

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
