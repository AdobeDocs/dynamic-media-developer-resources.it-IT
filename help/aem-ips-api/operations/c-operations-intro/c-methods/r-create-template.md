---
description: Crea un’immagine a livelli che può avere più livelli di testo e immagine.
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 9%

---


# createTemplate{#createtemplate}

Crea un’immagine a livelli che può avere più livelli di testo e immagine.

Il parametro `urlModifier` specifica i comandi del protocollo Image Server memorizzati nel catalogo Image Server applicati prima di qualsiasi comando fornito dall&#39;utente sull&#39;URL. Il parametro `urlPostApplyModifier` specifica i comandi del protocollo applicati dopo eventuali comandi URL, che sovrascriveranno eventuali impostazioni in conflitto fornite dall&#39;utente.

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
| `*`companyHandle`*` | `xsd:string` | Sì | Società a cui appartiene il modello. |
| `*`folderHandle`*` | `xsd:string` | Sì | L&#39;handle di cartella che rappresenta la cartella in cui si trova il modello. |
| `*`name`*` | `xsd:string` | Sì | Nome del modello. |
| `*`type`*` | `xsd:string` | Sì | Tipo di modello. |
| `*`urlModifier`*` | `xsd:string` | Sì | Specifica i comandi Image Server memorizzati nel catalogo IS applicati prima di qualsiasi comando fornito dall&#39;utente sull&#39;URL. |
| `*`urlPostApplyModifier`*` | `xsd:string` | No | Specifica i comandi di protocollo applicati dopo eventuali comandi URL, che sostituiranno eventuali impostazioni in conflitto fornite dall&#39;utente. |

**Output (createTemplateParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | Sì | L&#39;handle del modello. |

## Esempi {#section-09adb4d2f0c944af875c4463a461f55d}

Questo esempio di codice crea un modello in una cartella specificata da un handle, con un nome `APIcreateTemplate`, un `urlModifier` e un `urlPostApplyModifier`. La risposta restituisce l&#39;handle al modello appena creato.

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

