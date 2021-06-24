---
description: Aggiorna le autorizzazioni della cartella.
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '77'
ht-degree: 15%

---

# updateFolderPermissions{#updatefolderpermissions}

Aggiorna le autorizzazioni della cartella.

Sintassi

## Tipi di utenti autorizzati {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-339e6e17c5504e1ea79fbdc05f618050}

**Input (updateFolderPermissionsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`folderHandle`*` | `xsd:string` | Sì | Maniglia della cartella. |
| `*`updateChildren`*` | `xsd:boolean` | Sì | Determina se aggiornare gli elementi secondari con le autorizzazioni impostate per la cartella di livello principale. |
| `*`updateArray`*` | `types:PermissionUpdateArray` | Sì | Array di aggiornamenti delle autorizzazioni da applicare alla cartella. |

**Output (updateFolderPermissionsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-c3fe4d4388674870a3856c35ef66b631}

**Request Contents (Richiesta contenuto)**

```java
<ns1:updateFolderPermissionsParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:folderHandle>MyCompany/eCatalogs/</ns1:folderHandle>
   <ns1:updateChildren>false</ns1:updateChildren>
   <ns1:updateArray>
      <ns1:items>
         <ns1:groupHandle>225</ns1:groupHandle>
         <ns1:permissionType>Read</ns1:permissionType>
         <ns1:isAllowed>true</ns1:isAllowed>
         <ns1:isOverride>true</ns1:isOverride>
      </ns1:items>
   </ns1:updateArray>
</ns1:updateFolderPermissionsParam>
```

**Risposta**

Nessuno.
