---
description: Imposta vari valori di configurazione specifici per la società.
seo-description: Imposta vari valori di configurazione specifici per la società.
seo-title: setCompanySettings
solution: Experience Manager
title: setCompanySettings
topic: Scene7 Image Production System API
uuid: 5908082f-6743-4444-ba73-757ad4664890
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 10%

---


# setCompanySettings{#setcompanysettings}

Imposta vari valori di configurazione specifici per la società.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | Maniglia aziendale. |
| ` *`overwriteMode`*` | `xsd:string` | No | Modalità di sovrascrittura risorse. |
| ` *`keepPublishState`*` | `xsd:boolean` | No | Impostate questa opzione su `true` per mantenere lo stato di pubblicazione al momento del ricaricamento di una risorsa. |
| ` *`defaultSourceProfileHandle`*` | `xsd:string` | No | Risorsa IccProfile da usare come profilo colore sorgente predefinito. |
| ` *`defaultDisplayProfileHandle`*` | `xsd:string` | No | Risorsa IccProfile da usare come profilo colore di visualizzazione predefinito. |
| ` *`iptcExifMappingXsltHandle`*` | `xsd:string` | No | Risorsa XSL utilizzata per mappare i metadati IPTC e EXIF ai campi di metadati IPS. |
| ` *`xmpMappingXsltHandle`*` | `xsd:string` | No | Risorsa XSL utilizzata per mappare XMP metadati ai campi di metadati IPS. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | No | Spazio su disco disponibile minimo (in KB) prima dell&#39;invio di un messaggio di avviso. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | No | Impostate questa opzione su `true` per inviare agli amministratori della società una notifica ogni volta che le risorse vengono svuotate dal cestino. |

**Output (setCompanySettingsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-d10bf1d3d86f46f7bcf78dc1a2c363c5}

Questo esempio di codice imposta la configurazione di una società.

**Request Contents (Richiesta contenuto)**

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
