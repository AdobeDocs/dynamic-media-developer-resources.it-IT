---
description: Imposta vari valori di configurazione specifici per l’azienda.
solution: Experience Manager
title: setCompanySettings
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: c6b72ceb-3c86-4b13-89e9-5f1bb9846b2c
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '151'
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
| iptcExifMappingXsltHandle | `xsd:string` | No | Risorsa XSL utilizzata per la mappatura dei metadati IPTC ed EXIF ai campi di metadati IPS. |
| xmpMappingXsltHandle | `xsd:string` | No | Risorsa XSL utilizzata per mappare i metadati XMP ai campi di metadati IPS. |
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
