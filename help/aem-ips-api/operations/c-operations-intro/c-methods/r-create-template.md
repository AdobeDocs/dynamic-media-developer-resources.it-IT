---
description: Crea un'immagine a livelli che può avere più livelli di testo e immagine.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 8%

---

# createTemplate{#createtemplate}

Crea un&#39;immagine a livelli che può avere più livelli di testo e immagine.

Il `urlModifier` Il parametro specifica i comandi del protocollo Image Server memorizzati nel catalogo Image Server applicati prima di qualsiasi comando fornito dall&#39;utente sull&#39;URL. Il `urlPostApplyModifier` Il parametro specifica i comandi di protocollo applicati dopo qualsiasi comando URL, che ignorano eventuali impostazioni in conflitto fornite dall&#39;utente.

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
| urlPostApplyModifier | `xsd:string` | No | Specifica i comandi di protocollo applicati dopo qualsiasi comando URL, che ignoreranno eventuali impostazioni in conflitto fornite dall&#39;utente. |

**Output (createTemplateParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| assetHandle | `xsd:string` | Sì | Handle del modello. |

## Esempi {#section-09adb4d2f0c944af875c4463a461f55d}

Questo esempio di codice crea un modello in una cartella specificata da un handle, con il nome `APIcreateTemplate`, a `urlModifier`, e un `urlPostApplyModifier`. La risposta restituisce l’handle al modello appena creato.

**Request Contents (Richiesta contenuto)**

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
