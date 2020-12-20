---
description: Crea un’immagine a più livelli con più livelli di testo e immagine.
seo-description: Crea un’immagine a più livelli con più livelli di testo e immagine.
seo-title: createTemplate
solution: Experience Manager
title: createTemplate
topic: Scene7 Image Production System API
uuid: c54bd47c-13e1-4b0d-a24c-9829b0a6d5bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 9%

---


# createTemplate{#createtemplate}

Crea un’immagine a più livelli con più livelli di testo e immagine.

Il parametro `urlModifier` specifica i comandi del protocollo Image Server memorizzati nel catalogo Image Server applicati prima dei comandi forniti dall’utente nell’URL. Il parametro `urlPostApplyModifier` specifica i comandi del protocollo applicati dopo eventuali comandi URL, che ignoreranno eventuali impostazioni fornite dall&#39;utente in conflitto.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | La società a cui appartiene il modello. |
| ` *`folderHandle`*` | `xsd:string` | Sì | handle della cartella che rappresenta la cartella in cui risiede il modello. |
| ` *`name`*` | `xsd:string` | Sì | Nome del modello. |
| ` *`type`*` | `xsd:string` | Sì | Tipo di modello. |
| ` *`urlModifier`*` | `xsd:string` | Sì | Specifica i comandi Image Server memorizzati nel catalogo IS applicati prima di qualsiasi comando fornito dall’utente sull’URL. |
| ` *`urlPostApplyModifier`*` | `xsd:string` | No | Specifica i comandi del protocollo applicati dopo eventuali comandi URL, che ignoreranno eventuali impostazioni in conflitto fornite dall&#39;utente. |

**Output (createTemplateParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`assetHandle`*` | `xsd:string` | Sì | La maniglia del modello. |

## Esempi {#section-09adb4d2f0c944af875c4463a461f55d}

Questo esempio di codice crea un modello in una cartella specificata da un handle, con un nome `APIcreateTemplate`, un `urlModifier` e un `urlPostApplyModifier`. La risposta restituisce l’handle al modello appena creato.

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

