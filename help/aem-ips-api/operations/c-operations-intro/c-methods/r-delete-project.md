---
description: Elimina un progetto da una società. I collegamenti tra le risorse e il progetto non funzionano, ma le risorse non vengono eliminate da IPS.
solution: Experience Manager
title: deleteProject
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: b42be3ef-c935-4548-8f92-4fc33af321b5
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 7%

---

# deleteProject{#deleteproject}

Elimina un progetto da una società. I collegamenti tra le risorse e il progetto non funzionano, ma le risorse non vengono eliminate da IPS.

Sintassi

## Tipi di utenti autorizzati {#section-d8a70e23c68d426e9af1357b978ae2f0}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-00d1e00dd5014513a52b4e6b4f61de62}

**Input (deleteProjectParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyName`*` | `xsd:string` | Sì | Nome della società associata al progetto. |
| `*`projectHandle`*` | `xsd:string` | Sì | L&#39;handle del progetto da eliminare. |

**Output (deleteProjectReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-e38507f1f7ec41b9a625f47390490254}

Questo esempio di codice utilizza l&#39;handle dell&#39;azienda e l&#39;handle del progetto come campi nel componente deleteProjectParam inviato al server dei servizi Web IPS per eliminare il progetto.

**Request Contents (Richiesta contenuto)**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Risposta**

Nessuno.
