---
description: Imposta i campi dei metadati del tipo di carattere.
solution: Experience Manager
title: batchSetFontFields
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: f38aa861-2a81-4663-967e-72611122f51b
TQID: 'https://experienceleague.adobe.com/IkKqBLa2j-YKPTp5Nsttxb8GgpPgcSee1zG0asjxNyQ'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 125
ht-degree: 12%

---

# batchSetFontFields{#batchsetfontfields}

Imposta i campi dei metadati del tipo di carattere.

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
| companyHandle | `xsd:string` | Sì | Gestire l&#39;azienda che contiene i caratteri. |
| updateArray | `types:FontFieldUpdateArray` | Sì | Array di aggiornamenti dei campi carattere. |

**Output (batchSetFontFieldsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | `xsd:int` | Sì | Numero di campi carattere impostati correttamente. |
| warningCount | `xsd:int` | Sì | Numero di avvisi generati quando l&#39;operazione ha tentato di impostare i campi carattere. |
| errorCount | `xsd:int` | Sì | Numero di errori generati quando l&#39;operazione ha tentato di impostare i campi carattere. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Array di dettagli associati alle risorse che hanno generato avvisi quando l’operazione ha tentato di applicare gli aggiornamenti. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | L’array di dettagli associati alle risorse che hanno generato errori quando l’operazione ha tentato di applicare gli aggiornamenti. |

## Esempi {#section-0449c2e4ec534f4b8ee849ec4fe12c4e}

**Richiesta**

```javascript {.line-numbers}
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

```javascript {.line-numbers}
<batchSetFontFieldsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2009-07-31">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</batchSetFontFieldsReturn>
```
