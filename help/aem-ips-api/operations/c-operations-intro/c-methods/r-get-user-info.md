---
description: Ottiene informazioni su un utente. Utilizza l’indirizzo e-mail e la password di un utente di sistema come credenziali per autorizzare la richiesta. In caso contrario, l'operazione ottiene informazioni sull'utente predefinito.
solution: Experience Manager
title: getUserInfo
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 1981f25f-779e-4434-ab6b-0debb40521fe
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 10%

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
| `*`userHandle`*` | `xsd:string` | No | Gestisci l&#39;utente di cui desideri restituire le informazioni. |
| `*`e-mail`*` | `xsd:string` | No | Indirizzo e-mail utente. |

**Output (getUserInfoReturn)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| `*`userInfo`*` | `types:User` | Sì | Nome, cognome, indirizzo e-mail e ruolo di un utente, se l’utente è valido e quando scade la password dell’utente. |

## Esempi {#section-98d77a2e360a438dbe240099bea26a65}

Questo esempio di codice restituisce informazioni per l&#39;utente IPS predefinito.

**Request Contents (Richiesta contenuto)**

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
