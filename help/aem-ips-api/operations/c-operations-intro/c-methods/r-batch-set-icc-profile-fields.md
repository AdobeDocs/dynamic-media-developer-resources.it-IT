---
description: Imposta i campi di metadati del profilo ICC.
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 12%

---


# batchSetIccProfileFields{#batchseticcprofilefields}

Imposta i campi di metadati del profilo ICC.

Sintassi

## Tipi di utenti autorizzati {#section-f6f7caf9434b4f469518dab64b76c0f4}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-75a02b55ae0d444ca26b59aac6e86d6f}

**Input (batchSetIccProfileFields)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Gestisci la società che contiene i profili ICC. |
| `*`aggiorna array`*` | `xsd:string` | Sì | Array di aggiornamenti del profilo ICC. |

**Output (batchSetIccProfileFields)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sì | Numero di campi del profilo ICC impostati correttamente. |
| `*`warningCount`*` | `xsd:int` | Sì | Il numero di avvisi generati quando l&#39;operazione tentava di impostare i campi del profilo ICC. |
| `*`errorCount`*` | `xsd:int` | Sì | Il numero di errori generati quando l&#39;operazione tentava di impostare i campi del profilo ICC. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione tentava di applicare gli aggiornamenti. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che generavano errori quando l’operazione tentava di applicare gli aggiornamenti. |

## Esempi {#section-5dc90cfbd9b1411485b44859032f7cb9}

**Request Contents (Richiesta contenuto)**

```java
<batchSetIccProfileFieldsParam xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <companyHandle>c|1</companyHandle>
   <updateArray>
      <items>
         <assetHandle>a|1808|13|169</assetHandle>
         <class>Output</class>
         <colorSpace>CMYK</colorSpace>
         <pcsType>Luv</pcsType>
      </items>
   </updateArray>
</batchSetIccProfileFieldsParam>
```

**Risposta**

```java
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```

