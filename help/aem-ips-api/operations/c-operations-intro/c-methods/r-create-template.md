---
description: Crea un'immagine a livelli che può avere più livelli di testo e immagine.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
TQID: 'https://experienceleague.adobe.com/T9x2yuGOkwJ5xp6CVyREMySIy7HYL58jYI3-J2E2K6g'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 194
ht-degree: 7%

---

# createTemplate{#createtemplate}

Crea un&#39;immagine a livelli che può avere più livelli di testo e immagine.

Il parametro `urlModifier` specifica i comandi del protocollo Image Server memorizzati nel catalogo Image Server applicati prima di qualsiasi comando fornito dall&#39;utente sull&#39;URL. Il parametro `urlPostApplyModifier` specifica i comandi di protocollo applicati dopo qualsiasi comando URL, che ignora eventuali impostazioni in conflitto fornite dall&#39;utente.

## Tipi di utenti autorizzati {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**Input (createTemplateParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Società a cui appartiene il modello. |
| folderHandle | `xsd:string` | Sì | Handle di cartella che rappresenta la cartella in cui risiede il modello. |
| nome | `xsd:string` | Sì | Nome modello. |
| tipo | `xsd:string` | Sì | Tipo di modello. |
| urlModifier | `xsd:string` | Sì | Specifica i comandi del server immagini memorizzati nel catalogo IS che vengono applicati prima di qualsiasi comando fornito dall&#39;utente sull&#39;URL. |
| urlPostApplyModifier | `xsd:string` | No | Specifica i comandi di protocollo applicati dopo qualsiasi comando URL, che ignorano eventuali impostazioni in conflitto fornite dall&#39;utente. |

**Output (createTemplateParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| assetHandle | `xsd:string` | Sì | Handle del modello. |

## Esempi {#section-09adb4d2f0c944af875c4463a461f55d}

In questo esempio di codice viene creato un modello in una cartella specificata da un handle, con nome `APIcreateTemplate`, `urlModifier` e `urlPostApplyModifier`. La risposta restituisce l’handle al modello appena creato.

**Richiesta**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**Risposta**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```
