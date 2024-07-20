---
description: Crea una vista predefinita che determina ciò che un utente può vedere. Il visualizzatore può essere di qualsiasi tipo disponibile in IPS. La vista dei predefiniti viene applicata quando le risorse vengono pubblicate.
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 8%

---

# createViewerPreset{#createviewerpreset}

Crea una vista predefinita che determina ciò che un utente può vedere. Il visualizzatore può essere di qualsiasi tipo disponibile in IPS. La vista dei predefiniti viene applicata quando le risorse vengono pubblicate.

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
| companyHandle | `xsd:string` | Sì | Handle dell’azienda che contiene i predefiniti visualizzatore e le risorse. |
| folderHandle | `xsd:string` | Sì | Handle della cartella che contiene le risorse. |
| nome | `xsd:string` | Sì | Nome visualizzatore. |
| tipo | `xsd:string` | Sì | Tipo di visualizzatore. |
| configSettingArray | `types:ConfigSettingArray` | No | Matrice che contiene nomi, valori e handle di immagini a cui si applicano i predefiniti. |

**Output (createViewerPresetReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| viewerPresetHandle | `xsd:string` | Sì | Maniglia del predefinito per il visualizzatore. |

## Esempi {#section-c88ea63536f3461cbe4677ba53f875dd}

Questo esempio di codice crea un predefinito per lettore video. La risposta restituisce un handle per il predefinito.

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
