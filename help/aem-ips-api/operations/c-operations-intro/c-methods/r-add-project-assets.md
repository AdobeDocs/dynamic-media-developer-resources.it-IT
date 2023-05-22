---
description: Aggiunge una o più risorse a un progetto.
solution: Experience Manager
title: addProjectAssets
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 60aa2846-b41e-4131-b465-82aa832434f7
source-git-commit: b89ca96947f751b750623e1f18d2a5d86f0cd759
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 10%

---

# addProjectAssets{#addprojectassets}

Aggiunge una o più risorse a un progetto.

Sintassi

## Tipi di utenti autorizzati {#section-c67e7422921047f4ab4d4e9ba5a7aafe}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-20d498e971b6466298e60c8a77fc32b2}

**Input (addProjectAssetsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestisci per la società associata al progetto corrente. |
| projectHandle | `xsd:string` | Sì | Gestisci il progetto a cui stai aggiungendo risorse. |
| projectHandleArray | `xsd:HandleArray` | Sì | Array di risorse da aggiungere al progetto corrente. |

**Output (addProjectAssetsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| successCount | `xsd:int` | Sì | Numero di risorse aggiunte correttamente. |
| warningCount | `xsd:int` | Sì | Il numero di avvisi generati quando l’operazione ha tentato di aggiungere risorse a un progetto. |
| errorCount | `xsd:int` | Sì | Il numero di errori generati quando l’operazione ha tentato di aggiungere risorse a un progetto. |
| warningDetailHandle | `xsd:AssetOperationFaultArray` | No | Matrice di avvisi generati dalle risorse quando l’operazione ha tentato di aggiungerle a un progetto. |
| companyHandle | `xsd:AssetOperationFaultArray` | No | Array di errori generati dalle risorse quando l’operazione ha tentato di aggiungerli a un progetto. |

## Esempi {#section-bee5be2402f54cb9a3a02cc07def4135}

In questo esempio viene aggiunta una singola risorsa (a cui fa riferimento il relativo handle) in una matrice di handle di risorsa a un progetto specificato nella richiesta. Operazione completata quando la risposta `successCount` restituisce `1`.

**Request Contents (Richiesta contenuto)**

```java {.line-numbers}
<addProjectAssetsParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|6</companyHandle>
   <projectHandle>p|6|ProjectTestAPI</projectHandle>
   <assetHandleArray>
      <items>a|732|1|535</items>
   </assetHandleArray>
</addProjectAssetsParam>
```

**Risposta**

```java {.line-numbers}
<addProjectAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <successCount>1</successCount>
   <warningCount>0</warningCount>
   <errorCount>0</errorCount>
</addProjectAssetsReturn>
```
