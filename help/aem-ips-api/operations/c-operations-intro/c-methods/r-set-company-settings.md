---
description: Imposta vari valori di configurazione specifici per l’azienda.
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
TQID: 'https://experienceleague.adobe.com/df-NUZDApA-q0a-A3oxM6PUQUoVmGy8gqS4HU8lhfvc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 154
ht-degree: 8%

---

# setCompanySettings{#setcompanysettings}

Imposta vari valori di configurazione specifici per l’azienda.

Sintassi

## Tipi di utenti autorizzati {#section-41732fa7424b455cb458eec21a02259c}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-a472da6c57c74a94a179dda081004888}

**Input (setCompanySettingsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| overwriteMode | `xsd:string` | No | Modalità di sovrascrittura delle risorse. |
| keepPublishState | `xsd:boolean` | No | Imposta su `true` per mantenere lo stato di pubblicazione quando una risorsa viene ricaricata. |
| defaultSourceProfileHandle | `xsd:string` | No | Risorsa IccProfile da utilizzare come profilo colore di origine predefinito. |
| defaultDisplayProfileHandle | `xsd:string` | No | Risorsa IccProfile da utilizzare come profilo colore di visualizzazione predefinito. |
| iptcExifMappingXsltHandle | `xsd:string` | No | Risorsa XSL utilizzata per la mappatura dei metadati IPTC ed EXIF su campi di metadati IPS. |
| xmpMappingXsltHandle | `xsd:string` | No | Risorsa XSL utilizzata per mappare i metadati di XMP ai campi di metadati IPS. |
| diskSpaceWarningMin | `xsd:int` | No | Spazio su disco disponibile minimo (in KB) prima dell&#39;invio di un messaggio di avviso. |
| emailTrashCleanupWarning | `xsd:boolean` | No | Impostato su `true` per inviare agli amministratori della società una notifica ogni volta che le risorse vengono svuotate dal cestino. |

**Output (setCompanySettingsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Questo esempio di codice imposta la configurazione di un’azienda.

**Richiesta**

```java
<ns1:setCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
   <ns1:overwriteMode>OverwriteFullName</ns1:overwriteMode>
   <ns1:retainPublishState>true</ns1:retainPublishState>
   <ns1:diskSpaceWarningMin>100000</ns1:diskSpaceWarningMin>
   <ns1:emailTrashCleanupWarning>true</ns1:emailTrashCleanupWarning>
</ns1:setCompanySettingsParam>
```

**Risposta**

Nessuno.
