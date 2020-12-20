---
description: Consente di creare una visualizzazione predefinita che determina il contenuto visibile all’utente. Il visualizzatore può essere di qualsiasi tipo disponibile in IPS. La visualizzazione predefinita viene applicata quando le risorse vengono pubblicate.
seo-description: Consente di creare una visualizzazione predefinita che determina il contenuto visibile all’utente. Il visualizzatore può essere di qualsiasi tipo disponibile in IPS. La visualizzazione predefinita viene applicata quando le risorse vengono pubblicate.
seo-title: createViewerPreset
solution: Experience Manager
title: createViewerPreset
topic: Scene7 Image Production System API
uuid: 4160d2b0-6147-459f-830a-43c99b8dc196
translation-type: tm+mt
source-git-commit: 87164dbf805a179f7bdeecd7cc6140c3456b61bb
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 10%

---


# createViewerPreset{#createviewerpreset}

Consente di creare una visualizzazione predefinita che determina il contenuto visibile all’utente. Il visualizzatore può essere di qualsiasi tipo disponibile in IPS. La visualizzazione predefinita viene applicata quando le risorse vengono pubblicate.

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
| ` *`companyHandle`*` | `xsd:string` | Sì | handle della società che contiene i predefiniti per visualizzatori e le risorse. |
| ` *`folderHandle`*` | `xsd:string` | Sì | handle della cartella contenente le risorse. |
| ` *`name`*` | `xsd:string` | Sì | Nome visualizzatore. |
| ` *`type`*` | `xsd:string` | Sì | Tipo visualizzatore. |
| ` *`configSettingArray`*` | `types:ConfigSettingArray` | No | Un array che contiene nomi, valori e maniglie delle immagini a cui si applicano i predefiniti. |

**Output (createViewerPresetReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`viewerPresetHandle`*` | `xsd:string` | Sì | Gestione del predefinito per il visualizzatore. |

## Esempi {#section-c88ea63536f3461cbe4677ba53f875dd}

Questo esempio di codice crea un predefinito per lettori video. La risposta restituisce una maniglia al predefinito.

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

