---
description: Ottiene i valori stringa delle proprietà di sistema correlate a Image Portal.
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 7%

---

# getProperty{#getproperty}

Ottiene i valori stringa delle proprietà di sistema correlate a Image Portal.

Le proprietà di sistema supportate includono:

* `IpsVersion`: numero di versione IPS.
* `IpsImageServerUrl`: prefisso URL esterno completo per il server immagini IPS.
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`: prefisso URL per il rendering delle risorse SVG.
* `SvgRenderEnabled`: True se le risorse SVG possono essere sottoposte a rendering da `SvgRenderRootUrl`.

* `UploadPostMaxFileSize`: dimensione massima (in byte) dei dati del file consentita in un caricamento [!DNL POST]. Il sistema rifiuta i file superiori al limite massimo.

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
| nome | `xsd:string` | Sì | Nome della proprietà da ottenere. |

**Output (getPropertyReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| valore | `xsd:string` | Sì | Il valore della proprietà. |

## Esempi {#section-3f80a78dd60c404181b34d3a912d7a36}

In questo esempio di codice viene utilizzata una costante stringa IPS Properties per restituire un valore specifico. In questo esempio, la proprietà IPS corrisponde alla versione del server IPS.

**Richiesta**

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
