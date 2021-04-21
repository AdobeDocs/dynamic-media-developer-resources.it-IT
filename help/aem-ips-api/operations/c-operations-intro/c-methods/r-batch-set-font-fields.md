---
description: Imposta i campi dei metadati dei font.
solution: Experience Manager
title: batchSetFontFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 13%

---


# batchSetFontFields{#batchsetfontfields}

Imposta i campi dei metadati dei font.

## Tipi di utenti autorizzati {#section-89eff13b5ed54cddb87b1304ba4eff0e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-836f5948d00a46e98ccb62f0573e4e68}

**Input (batchSetFontFieldsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Gestisci l&#39;azienda che contiene i font. |
| `*`updateArray`*` | `types:FontFieldUpdateArray` | Sì | Array di aggiornamenti dei campi di font. |

**Output (batchSetFontFieldsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sì | Numero di campi di font impostati correttamente. |
| `*`warningCount`*` | `xsd:int` | Sì | Numero di avvisi generati quando l&#39;operazione tentava di impostare campi di font. |
| `*`errorCount`*` | `xsd:int` | Sì | Numero di errori generati quando l&#39;operazione tentava di impostare campi di font. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione tentava di applicare gli aggiornamenti. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generavano errori quando l’operazione tentava di applicare gli aggiornamenti. |

## Esempi {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**Request Contents (Richiesta contenuto)**

```java
<batchSetFontFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
          <assetHandle>a|450|14|19</assetHandle>
          <fontName>Bookman Old Style Font Name</fontName>
          <postscriptName>Bookman Old Style PostScript</postscriptName>
          <rtfName>Bookman Old Style RTF</rtfName>
          <fontFamily>Bookman Old Style Family</fontFamily>
          <style>BoldItalic</style>
          <typeName>Open Type</typeName><type>OTF</type>
      </items>
   </updateArray>
</batchSetFontFieldsParam>
```

**Risposta**

```java
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```

