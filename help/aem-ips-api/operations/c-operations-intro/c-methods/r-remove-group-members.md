---
description: Rimuove gli utenti aziendali da un gruppo specifico.
solution: Experience Manager
title: removeGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 8a9b7d54-d11b-41a8-9783-573a316e0ac6
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 5%

---

# removeGroupMembers{#removegroupmembers}

Rimuove gli utenti aziendali da un gruppo specifico.

**Differenze tra i comandi di rimozione**

* `removeGroupMembers`: rimuove più utenti da un gruppo.
* `removeGroupMembership`: rimuove un singolo utente da un array di gruppi.

## Tipi di utenti autorizzati {#section-2c64cdac15184fbba6c7b2945b5d87f7}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-b5596614a3be4ce5962455884e4636af}

**Input (removeGroupMembersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | L’handle dell’azienda con gli utenti con cui desideri lavorare. |
| groupHandle | `xsd:string` | Sì | Handle di gruppo. |
| userHandleArray | `types:HandleArray` | Sì | Matrice di handle per gli utenti di cui si desidera rimuovere l&#39;appartenenza ai gruppi. |

**Output (removeGroupMembersParam)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-9eedac852cea46ec80de6a6928bf97ac}

Questo esempio di codice rimuove un utente dalla società specificata. Rimuovere più utenti da un gruppo con l&#39;array di handle utente.

**Richiesta**

```java
<ns1:removeGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>621|jduvar@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:removeGroupMembersParam>
```

**Risposta**

Nessuno.
