---
description: Restituisce le impostazioni IPS per una società specifica.
seo-description: Restituisce le impostazioni IPS per una società specifica.
seo-title: getCompanySettings
solution: Experience Manager
title: getCompanySettings
uuid: 28ee706d-aaef-45a1-9655-3805f158cdc3
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 16%

---


# getCompanySettings{#getcompanysettings}

Restituisce le impostazioni IPS per una società specifica.

Sintassi

## Tipi di utenti autorizzati {#section-3378c9c67029473a87d5f5d8c616b1f3}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-e146f479c2744baa8f68be8c8848c97f}

**Input (getCompanySettingsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | L&#39;handle dell&#39;azienda di cui si desidera recuperare le impostazioni. |

**Output (getCompanySettingsReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`impostazioni`*` | `types:CompanySettings` | Sì | Impostazioni aziendali. |

## Esempi {#section-191f78995ecf473a95eadf7296204fd7}

Questo esempio di codice restituisce tutte le impostazioni IPS per una società specifica.

**Request Contents (Richiesta contenuto)**

```java
<ns1:getCompanySettingsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <ns1:companyHandle>c|6</ns1:companyHandle>
</ns1:getCompanySettingsParam>
```

**Risposta**

```java
<getCompanySettingsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <settings>
      <metadataArray>
         <items>
            <name>Profile Class</name>
            <value>1</value>
            <longVal>1</longVal>
         </items>
         <items>
             <name>Default Color Profile</name>
             <value>1</value>
         </items>
      </metadataArray>
      <iccProfileInfo>
         <originalPath>Scene7SharedAssets/ICCColorProfiles/Adobe ICC Profiles/RGB Profiles/</originalPath>
         <originalFile>sRGB Color Space Profile.icm</originalFile>
         <fileSize>0</fileSize>
      </iccProfileInfo>
      </defaultDisplayProfile>
      <diskSpaceWarningMin>100000</diskSpaceWarningMin>
      <emailTrashCleanupWarning>true</emailTrashCleanupWarning>
   </settings>
</getCompanySettingsReturn>
```

