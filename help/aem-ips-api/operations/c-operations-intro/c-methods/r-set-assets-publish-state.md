---
description: Determina se un batch di risorse è pronto per essere pubblicato.
solution: Experience Manager
title: setAssetsPublishState
feature: Dynamic Media Classic,SDK/API,Gestione risorse
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 11%

---


# setAssetsPublishState{#setassetspublishstate}

Determina se un batch di risorse è pronto per essere pubblicato.

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
| `*`companyHandle`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`publishStateUpdateArray`*` | `types:PublishStateUpdateArray` | Sì | Array di valori dello stato di pubblicazione per le risorse. |

**Output (setAssetsPublishStateParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | Sì | Numero di risorse aggiornate. |
| `*`warningCount`*` | `xsd:int` | Sì | Numero di risorse che hanno generato un avviso quando l&#39;operazione ha tentato di aggiornarle. |
| `*`errorCount`*` | `xsd:int` | Sì | Numero di risorse che hanno generato un errore quando l&#39;operazione ha tentato di eliminarle. |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | No | Dettagli associati agli aggiornamenti delle risorse che hanno generato un avviso. |
| `*`errorDetailArray`*` | `types:AssetOperationFaultArray` | No | Dettagli associati agli aggiornamenti delle risorse che hanno generato un errore. |

## Esempi {#section-38cfdd3436214a06a1bae16875501d51}

Questo esempio di codice imposta lo stato di pubblicazione di una risorsa.

**Request Contents (Richiesta contenuto)**

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

