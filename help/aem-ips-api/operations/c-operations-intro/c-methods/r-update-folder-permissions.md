---
description: Aggiornare le autorizzazioni della cartella.
solution: Experience Manager
title: updateFolderPermissions
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 4e4f382e-4339-4b9d-a721-d33a4fa8be6b
TQID: 'https://experienceleague.adobe.com/rZv5saDJ9TTY7IYvE6i6CZIHX9xqx9HFnIJTQxdbjPU'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 73
ht-degree: 10%

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
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| folderHandle | `xsd:string` | Sì | Handle di cartella. |
| updateChildren | `xsd:boolean` | Sì | Determina se aggiornare gli elementi figlio con le autorizzazioni impostate per la cartella di livello principale. |
| updateArray | `types:PermissionUpdateArray` | Sì | Matrice di aggiornamenti delle autorizzazioni da applicare alla cartella. |

**Output (updateFolderPermissionsReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-c3fe4d4388674870a3856c35ef66b631}

**Richiesta**

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
