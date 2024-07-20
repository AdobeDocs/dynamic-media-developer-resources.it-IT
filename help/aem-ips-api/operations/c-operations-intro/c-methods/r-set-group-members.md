---
description: Imposta l'appartenenza al gruppo degli utenti che appartengono a una società specifica.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 81348da7-6733-4da9-8a0a-376fccf791ea
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 5%

---

# setGroupMembers{#setgroupmembers}

Imposta l&#39;appartenenza al gruppo degli utenti che appartengono a una società specifica.

Se non si dispone dei privilegi necessari per eseguire l&#39;operazione, verrà generato un errore di autenticazione. Ciò vale anche se uno qualsiasi degli utenti nell’array dell’handle utente non appartiene all’azienda specificata nell’handle aziendale,

## Tipi di utenti autorizzati {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-6a18562fc8e942af94be10bbb8c51151}

**Input (setGroupMembersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| companyHandle | `xsd:string` | Sì | Gestore azienda. |
| groupHandle | `xsd:string` | Sì | Handle di gruppo. |
| userHandleArray | `types:HandleArray` | Sì | Array di handle per gli utenti di cui si desidera impostare l&#39;appartenenza al gruppo. |

**Output (setGroupMembesReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-9c528c3f44a141ce9eaddf634f26c487}

Questo esempio di codice imposta l&#39;appartenenza al gruppo per un singolo utente.

**Richiesta**

```java
<ns1:setGroupMembersParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandle>225</ns1:groupHandle>
   <ns1:userHandleArray>
      <ns1:items>70|kmagnusson@adobe.com</ns1:items>
   </ns1:userHandleArray>
</ns1:setGroupMembersParam>
```

**Risposta**

Nessuno.
