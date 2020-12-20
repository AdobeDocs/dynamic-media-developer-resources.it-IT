---
description: Elimina un progetto da una società. I collegamenti tra le risorse e il progetto sono interrotti, ma le risorse non vengono eliminate da IPS.
seo-description: Elimina un progetto da una società. I collegamenti tra le risorse e il progetto sono interrotti, ma le risorse non vengono eliminate da IPS.
seo-title: deleteProject
solution: Experience Manager
title: deleteProject
topic: Scene7 Image Production System API
uuid: 0915066f-2106-4cbc-a68a-f149810c24f8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 6%

---


# deleteProject{#deleteproject}

Elimina un progetto da una società. I collegamenti tra le risorse e il progetto sono interrotti, ma le risorse non vengono eliminate da IPS.

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
| ` *`companyName`*` | `xsd:string` | Sì | Nome della società associata al progetto. |
| ` *`projectHandle`*` | `xsd:string` | Sì | L’handle del progetto da eliminare. |

**Output (deleteProjectReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-e38507f1f7ec41b9a625f47390490254}

Questo esempio di codice utilizza l&#39;handle della società e l&#39;handle del progetto come campi nell&#39;deleteProjectParam inviato al server dei servizi Web IPS per eliminare il progetto.

**Request Contents (Richiesta contenuto)**

```java
<deleteProjectParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
<projectHandle>p|6|ProjectTestAPI</projectHandle></deleteProjectParam>
```

**Risposta**

Nessuno.
