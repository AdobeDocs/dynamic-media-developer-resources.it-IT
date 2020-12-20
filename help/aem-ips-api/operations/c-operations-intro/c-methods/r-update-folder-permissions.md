---
description: Aggiornare le autorizzazioni della cartella.
seo-description: Aggiornare le autorizzazioni della cartella.
seo-title: updateFolderPermissions
solution: Experience Manager
title: updateFolderPermissions
topic: Scene7 Image Production System API
uuid: 940d7b63-80cf-4097-9cf9-8499b69181b7
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '76'
ht-degree: 15%

---


# updateFolderPermissions{#updatefolderpermissions}

Aggiornare le autorizzazioni della cartella.

Sintassi

## Tipi di utenti autorizzati {#section-e5c2217231bf4b3386e0ab3f2e9aca0b}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-339e6e17c5504e1ea79fbdc05f618050}

**Input (updateFolderPermissionsParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | Sì | Maniglia aziendale. |
| ` *`folderHandle`*` | `xsd:string` | Sì | handle della cartella. |
| ` *`updateChildren`*` | `xsd:boolean` | Sì | Determina se aggiornare gli elementi figlio con autorizzazioni impostate per la cartella di livello principale. |
| ` *`updateArray`*` | `types:PermissionUpdateArray` | Sì | L’array di aggiornamenti delle autorizzazioni da applicare alla cartella. |

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
