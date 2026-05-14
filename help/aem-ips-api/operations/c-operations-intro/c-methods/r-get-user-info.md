---
description: Ottiene informazioni su un utente. Utilizza l’indirizzo e-mail e la password di un utente di sistema come credenziali per autorizzare la richiesta. In caso contrario, l'operazione ottiene informazioni sull'utente predefinito.
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
TQID: 'https://experienceleague.adobe.com/4FEwXXgelDJ5CDf4FhaE11GS3vsnZi6wjY7HproyCIw'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 139
ht-degree: 7%

---

# getUserInfo{#getuserinfo}

Ottiene informazioni su un utente. Utilizza l’indirizzo e-mail e la password di un utente di sistema come credenziali per autorizzare la richiesta. In caso contrario, l&#39;operazione ottiene informazioni sull&#39;utente predefinito.

Sintassi

## Tipi di utenti autorizzati {#section-1c42d78e914a4b84a946b3480f29b36a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-e87b3cb743494719925c9458eed433b6}

**Input (getUserInfoParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userHandle | `xsd:string` | No | Gestisci per l’utente di cui desideri restituire le informazioni. |
| email | `xsd:string` | No | Indirizzo e-mail utente. |

**Output (getUserInfoReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| userInfo | `types:User` | Sì | Il nome, il cognome, l’indirizzo e-mail e il ruolo di un utente, nonché se l’utente è valido e quando scade la password dell’utente. |

## Esempi {#section-98d77a2e360a438dbe240099bea26a65}

In questo esempio di codice vengono restituite informazioni per l&#39;utente IPS predefinito.

**Richiesta**

```java
<getUserInfoParam xmlns="http://www.scene7.com/IpsApi/xsd" /></getUserInfoParam>
```

**Risposta**

```java
<ns1:getUserInfoReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd"> 
   <ns1:userInfo> 
      <ns1:userHandle>3261|user@scene7.com</ns1:userHandle> 
      <ns1:firstName>FirstName</ns1:firstName> 
      <ns1:lastName>LastName</ns1:lastName> 
      <ns1:email>user@scene7.com</ns1:email> 
      <ns1:role>IpsAdmin</ns1:role> 
      <ns1:isValid>true</ns1:isValid> 
      <ns1:passwordExpires>2107-04-22T18:35:41.995Z</ns1:passwordExpires> 
   </ns1:userInfo> 
</ns1:getUserInfoReturn>
```
