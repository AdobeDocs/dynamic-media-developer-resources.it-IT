---
description: Crea una visualizzazione preimpostata che determina cosa può vedere un utente. Il visualizzatore può essere di qualsiasi tipo disponibile in IPS. La visualizzazione predefinita viene applicata quando le risorse vengono pubblicate.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic, SDK/API, Predefiniti visualizzatore
role: Sviluppatore,Amministratore
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 11%

---

# createViewerPreset{#createviewerpreset}

Crea una visualizzazione preimpostata che determina cosa può vedere un utente. Il visualizzatore può essere di qualsiasi tipo disponibile in IPS. La visualizzazione predefinita viene applicata quando le risorse vengono pubblicate.

Sintassi

## Tipi di utenti autorizzati {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## Parametri {#section-aa6dc37e327541ebbfed7685cd8071ff}

**Input (createViewerPresetParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Il handle della società che contiene i predefiniti e le risorse per visualizzatori. |
| `*`folderHandle`*` | `xsd:string` | Sì | L’handle della cartella contenente le risorse. |
| `*`name`*` | `xsd:string` | Sì | Nome del visualizzatore. |
| `*`type`*` | `xsd:string` | Sì | Tipo visualizzatore. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | No | Matrice che contiene nomi, valori e handle di immagini a cui si applicano i predefiniti. |

**Output (createViewerPresetReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`viewerPresetHandle`*` | `xsd:string` | Sì | Gestione del predefinito al visualizzatore. |

## Esempi {#section-c88ea63536f3461cbe4677ba53f875dd}

Questo esempio di codice crea un predefinito per lettore video. La risposta restituisce un handle al predefinito.

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**Risposta**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```
