---
description: Imposta l'iscrizione al gruppo degli utenti che appartengono a una specifica azienda.
solution: Experience Manager
title: setGroupMembers
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 8%

---


# setGroupMembers{#setgroupmembers}

Imposta l&#39;iscrizione al gruppo degli utenti che appartengono a una specifica azienda.

L&#39;operazione genera un errore di autenticazione se non si dispone dei privilegi per eseguire questa operazione. Questo vale anche se uno degli utenti dell&#39;array di handle utente non appartiene alla società specificata nell&#39;handle della società,

## Tipi di utenti autorizzati {#section-4523594039c24aa29c8d0d5c9c415391}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`

## Parametri {#section-6a18562fc8e942af94be10bbb8c51151}

**Input (setGroupMembersParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | Sì | Tratta l&#39;azienda. |
| `*`groupHandle`*` | `xsd:string` | Sì | Maniglia di gruppo. |
| `*`userHandleArray`*` | `types:HandleArray` | Sì | Array di handle per gli utenti di cui si desidera impostare l&#39;appartenenza al gruppo. |

**Output (setGroupMembesReturn)**

L&#39;API IPS non restituisce una risposta per questa operazione.

## Esempi {#section-9c528c3f44a141ce9eaddf634f26c487}

Questo esempio di codice imposta l&#39;appartenenza al gruppo per un singolo utente.

**Request Contents (Richiesta contenuto)**

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
