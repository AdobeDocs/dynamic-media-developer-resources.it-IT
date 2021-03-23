---
description: Ottiene informazioni su un utente. Utilizza l’indirizzo e-mail e la password di un utente di sistema come credenziali per autorizzare la richiesta. In caso contrario, l'operazione ottiene informazioni sull'utente predefinito.
seo-description: Ottiene informazioni su un utente. Utilizza l’indirizzo e-mail e la password di un utente di sistema come credenziali per autorizzare la richiesta. In caso contrario, l'operazione ottiene informazioni sull'utente predefinito.
seo-title: getUserInfo
solution: Experience Manager
title: getUserInfo
uuid: b305c108-22e9-4268-a5b3-25fddd844c24
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore,Amministratore
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 8%

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

