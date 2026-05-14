---
description: Determina se un batch di risorse è pronto per la pubblicazione.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: dce324e4-cf86-4a65-ab00-8cd2bba20f8f
TQID: 'https://experienceleague.adobe.com/VV11khRodimEOAdPB-6mHR-gIT4AMiKOKeuuH6J15VA'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 151
ht-degree: 9%

---

# setAssetsPublishState{#setassetspublishstate}

Determina se un batch di risorse è pronto per la pubblicazione.

Versione batch di [setAssetState](../../../operations/c-operations-intro/c-methods/r-set-asset-publish-state.md#reference-9efc2eeea42348e0b1d5f3d1005c6563).

## Tipi di utenti autorizzati {#section-0804726f683944dbbe9acfc3d35ccf25}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>L’utente deve disporre dell’accesso in lettura e scrittura alla risorsa.

## Parametri {#section-3e49d7859f8647b990d75373cc8dbc24}

**Input (setAssetsPublishStateParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| publishStateUpdateArray | `types:PublishStateUpdateArray` | Sì | Array dei valori dello stato di pubblicazione per le risorse. |

**Output (setAssetsPublishStateParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | `xsd:int` | Sì | Numero di risorse aggiornate correttamente. |
| warningCount | `xsd:int` | Sì | Il numero di risorse che hanno generato un avviso quando l’operazione ha tentato di aggiornarle. |
| errorCount | `xsd:int` | Sì | Il numero di risorse che hanno generato un errore quando l’operazione ha tentato di eliminarle. |
| warningDetailArray | `types:AssetOperationFaultArray` | No | Dettagli associati agli aggiornamenti della risorsa che hanno generato un avviso. |
| errorDetailArray | `types:AssetOperationFaultArray` | No | Dettagli associati agli aggiornamenti delle risorse che hanno generato un errore. |

## Esempi {#section-38cfdd3436214a06a1bae16875501d51}

Questo esempio di codice imposta lo stato di pubblicazione di una risorsa.

**Richiesta**

```java
<element name="setAssetsPublishStateParam">
   <complexType>
      <sequence>
         <element name="companyHandle" type="xsd:string"/>
         <element name="publishStateUpdateArray" type="types:PublishStateUpdateArray"/>
      </sequence>
   </complexType>
</element>
```

**Risposta**

```java
<element name="setAssetsPublishStateReturn">
   <complexType>
      <sequence>
         <element name="successCount" type="xsd:int"/>
         <element name="warningCount" type="xsd:int"/>
         <element name="errorCount" type="xsd:int"/>
         <element name="warningDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
         <element name="errorDetailArray"type="types:AssetOperationFaultArray" minOccurs="0"/>
      </sequence>
   </complexType>
</element>
```
