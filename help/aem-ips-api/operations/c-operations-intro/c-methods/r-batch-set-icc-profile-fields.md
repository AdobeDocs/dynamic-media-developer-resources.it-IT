---
description: Imposta i campi di metadati del profilo ICC.
solution: Experience Manager
title: batchSetIccProfileFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: d10a30ca-afa7-4ef0-8cef-0329b0068bf3
TQID: 'https://experienceleague.adobe.com/YmeLGJ9N-W-JOU7oG7utN4d1Q2pV17wtqocdrwYD-lQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 10%

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
| companyHandle | `xsd:string` | Sì | Gestire la società che contiene i profili ICC. |
| aggiorna array | `xsd:string` | Sì | Array di aggiornamenti del profilo ICC. |

**Output (batchSetIccProfileFields)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | `xsd:int` | Sì | Numero di campi del profilo ICC impostati correttamente. |
| warningCount | `xsd:int` | Sì | Numero di avvisi generati quando l&#39;operazione ha tentato di impostare i campi del profilo ICC. |
| errorCount | `xsd:int` | Sì | Il numero di errori generati quando l&#39;operazione ha tentato di impostare i campi del profilo ICC. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione ha tentato di applicare gli aggiornamenti. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | L’array di dettagli associati alle risorse che hanno generato errori quando l’operazione ha tentato di applicare gli aggiornamenti. |

## Esempi {#section-5dc90cfbd9b1411485b44859032f7cb9}

**Richiesta**

```java {.line-numbers}
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

```java {.line-numbers}
<batchSetIccProfileFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetIccProfileFieldsReturn>
```
