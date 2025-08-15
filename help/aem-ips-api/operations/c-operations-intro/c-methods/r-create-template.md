---
description: Crea un'immagine con livelli che può avere più livelli di testo e immagine.
solution: Experience Manager
title: Crea modello
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 7%

---

# Crea modello{#createtemplate}

Crea un&#39;immagine con livelli che può avere più livelli di testo e immagine.

Il `urlModifier` parametro consente di specificare i comandi del protocollo Immagine Server memorizzati nel catalogo di Immagine Server applicati prima di qualsiasi comando fornito da utente sul URL. Il `urlPostApplyModifier` parametro specifica i comandi di protocollo applicati dopo ogni comando URL, che esegue l&#39;override di eventuali impostazioni fornite da utente in conflitto.

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
| CompanyHandle | `xsd:string` | Sì | Società a cui appartiene il modello. |
| Handle cartella | `xsd:string` | Sì | L&#39;handle di cartella che rappresenta la cartella in cui risiede il modello. |
| nome | `xsd:string` | Sì | Nome del modello. |
| digitare | `xsd:string` | Sì | Tipo di modello. |
| urlModifier | `xsd:string` | Sì | Specifica i comandi del server Immagine memorizzati nel catalogo IS che vengono applicati prima di qualsiasi comando fornito da utente sul URL. |
| urlPostApplyModifier | `xsd:string` | No | Specifica i comandi di protocollo applicati dopo ogni comando URL, che sostituisce eventuali impostazioni fornite da utente in conflitto. |

**Output (createTemplateParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| Gestione risorsa | `xsd:string` | Sì | Handle del modello. |

## Esempi {#section-09adb4d2f0c944af875c4463a461f55d}

In questo esempio di codice viene creato un modello in una cartella specificata da un handle, con nome , `APIcreateTemplate`a `urlModifier`e a .`urlPostApplyModifier` La risposta restituisce l&#39;handle al modello appena creato.

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
