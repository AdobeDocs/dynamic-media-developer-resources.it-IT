---
description: Controlla se un utente con una società specifica (identificata dall'handle), l'indirizzo e-mail e la password possono effettuare l'accesso.
seo-description: Controlla se un utente con una società specifica (identificata dall'handle), l'indirizzo e-mail e la password possono effettuare l'accesso.
seo-title: checkLogin
solution: Experience Manager
title: checkLogin
topic: Scene7 Image Production System API
uuid: 69f9e5f6-50c2-403d-93b2-b84a01f512a9
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# checkLogin{#checklogin}

Controlla se un utente con una società specifica (identificata dall&#39;handle), l&#39;indirizzo e-mail e la password possono effettuare l&#39;accesso.

>[!NOTE]
>
>Se l&#39;handle della società viene omesso, questo metodo verifica il login dell&#39;utente predefinito.

## Tipi di utenti autorizzati {#section-df8b26b550854f899948276adaca083a}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## Parametri {#section-1ad4c0b4803b4388aedd655030676cb3}

**Input (checkLoginParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`companyHandle`*` | `xsd:string` | No | L’handle della società che contiene l’utente. |
| ` *`e-mail`*` | `xsd:string` | Sì | L&#39;indirizzo e-mail dell&#39;utente. |
| ` *`password`*` | `xsd:string` | Sì | La password dell&#39;utente. |

**Output (checkLoginParam)**

| Nome | Tipo | Obbligatorio | Descrizione |
|---|---|---|---|
| ` *`status`*` | `xsd:string` | Sì | Stato di accesso dell&#39;utente. |

## Esempi {#section-23f90100a9d94bc7b4045634cccd1b98}

Questo codice di esempio utilizza un parametro di handle della società, un indirizzo e-mail e una password per determinare se un utente può accedere a IPS. Se l&#39;utente *può* eseguire l&#39;accesso, questo metodo restituisce la stringa, `ValidLogin`. Se l&#39;utente *non può* eseguire l&#39;accesso, questo metodo restituisce la stringa, `InvalidLogin`.

**Request Contents (Richiesta contenuto)**

```java
<ns1:checkLoginParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>137</ns1:companyHandle>
   <ns1:email>juser3@scene7.com</ns1:email>
   <ns1:password>welcome</ns1:password>
</ns1:checkLoginParam>
```

**Risposta**

```java
<ns1:checkLoginReturn xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:status>InvalidLogin</ns1:status>
</ns1:checkLoginReturn>
```

