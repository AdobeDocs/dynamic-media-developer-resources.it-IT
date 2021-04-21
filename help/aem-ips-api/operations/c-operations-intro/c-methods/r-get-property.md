---
description: Ottiene i valori stringa delle proprietà di sistema relative a Image Portal.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 10%

---


# getProperty{#getproperty}

Ottiene i valori stringa delle proprietà di sistema relative a Image Portal.

Le proprietà di sistema supportate includono:

* `IpsVersion`: Numero di versione IPS.
* `IpsImageServerUrl`: Prefisso URL completo ed esterno per il server immagini IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: Prefisso URL per il rendering delle risorse SVG.
* `SvgRenderEnabled`: True se è possibile eseguire il rendering delle risorse SVG tramite  `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`: Dimensione massima (in byte) dei dati del file consentiti in un caricamento  [!DNL POST]. Il sistema rifiuta i file di dimensioni superiori al limite massimo.

## Tipi di utenti autorizzati {#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**Input (getPropertyParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`name`*` | `xsd:string` | Sì | Nome della proprietà da ottenere. |

**Output (getPropertyReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`value`*` | `xsd:string` | Sì | Il valore della proprietà. |

## Esempi {#section-3f80a78dd60c404181b34d3a912d7a36}

Questo esempio di codice utilizza una costante stringa Proprietà IPS per restituire un valore specifico. In questo esempio, la proprietà IPS è la versione del server IPS .

**Request Contents (Richiesta contenuto)**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**Risposta**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```

