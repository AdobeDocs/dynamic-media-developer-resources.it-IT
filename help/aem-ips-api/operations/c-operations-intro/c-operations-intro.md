---
description: Descrive i parametri dell'operazione comuni gestiti dall'API del servizio Web IPS.
solution: Experience Manager
title: Metodi operativi
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '698'
ht-degree: 0%

---

# Metodi operativi{#operations-methods}

Questa sezione descrive i parametri operativi comuni gestiti dall&#39;API del servizio Web IPS.

Per una descrizione completa di ciascun parametro di operazione, vedi [Parametri di funzionamento](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Maniglie: Informazioni {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Gestisce i riferimenti agli oggetti IPS restituiti da alcune operazioni API. Puoi anche passare gli handle come parametri alle chiamate di operazione successive. Gli handle sono tipi di dati stringa ( `xsd:string`).

Le maniglie sono destinate all&#39;uso solo durante una singola sessione dell&#39;applicazione. Inoltre, devi rendere persistenti gli handle perché il loro formato può cambiare tra le versioni IPS. Quando si scrivono applicazioni interattive, si implementano i timeout delle sessioni ed eliminano tutti gli handle tra le sessioni, in particolare dopo un aggiornamento IPS. Quando si scrivono applicazioni non interattive, chiamare le operazioni appropriate per recuperare gli handle ogni volta che l&#39;applicazione viene eseguita. I seguenti esempi di codice Java/Axis2 mostrano un’esecuzione del codice errata e corretta:

**Codice di handle non corretto**

Questo esempio di codice non è corretto perché contiene un valore hardcoded (555) per l&#39;handle dell&#39;azienda.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Codice di gestione corretto**

Questo esempio di codice è corretto perché chiama `getCompanyInfo` per restituire un handle valido. Non si basa su un valore hardcoded. Utilizza questo metodo o un altro equivalente API IPS per restituire l’handle richiesto.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Tipi di handle comuni {#section-e683ac8283284f9688e63f51a494f7a0}

**companyHandle**

La maggior parte delle operazioni richiede di impostare un contesto aziendale trasmettendo un `companyHandle` parametro . L&#39;handle della società è un puntatore restituito da alcune operazioni, ad esempio `getCompanyInfo`, `addCompany`e `getCompanyMembership`.

**userHandle**

La `userHandle` è un parametro facoltativo per le operazioni che hanno come target un utente specifico. Per impostazione predefinita, queste operazioni sono indirizzate all&#39;utente chiamante (l&#39;utente le cui credenziali vengono passate per l&#39;autenticazione). Tuttavia, gli utenti amministratori con le autorizzazioni appropriate possono specificare un altro utente. Ad esempio, il `setPassword` normalmente imposta la password dell&#39;utente autenticato, ma un amministratore può utilizzare il `userHandle` per impostare la password per un altro utente.

Per le operazioni che richiedono un contesto aziendale (utilizzando `companyHandle` ), gli utenti autenticati e target devono essere membri della società specificata. Per le operazioni che non richiedono un contesto aziendale, gli utenti autenticati e target devono essere entrambi membri di almeno una società comune.

Le seguenti operazioni possono recuperare gli handle utente:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle e accessGroupHandle**

Per impostazione predefinita, le operazioni che richiedono autorizzazioni di accesso (lettura, scrittura, eliminazione) operano nel contesto delle autorizzazioni dell&#39;utente chiamante. Alcune operazioni consentono di modificare questo contesto con `accessUserHandle` o `accessGroupHandle` parametro . La `accessUserHandle` consente a un amministratore di rappresentare un altro utente. La `accessGroupHandle` consente al chiamante di funzionare nel contesto di un gruppo di utenti specifico.

**responseFieldArray e excludeFieldArray**

Alcune operazioni consentono al chiamante di limitare quali campi sono inclusi nella risposta. La limitazione dei campi può contribuire a ridurre il tempo e la memoria necessari per elaborare la richiesta e ridurre le dimensioni dei dati di risposta. Il chiamante può richiedere un elenco specifico di campi passando un `responseFieldArray` o con un elenco enumerato di campi esclusi tramite il `excludeFieldArray` parametro .

Entrambi `responseFieldArray` e `excludeFieldArray` specificare i campi utilizzando un percorso nodo separato da `/`. Ad esempio, per specificare che `searchAssets` restituisce solo il nome, la data dell’ultima modifica e i metadati per ogni risorsa fanno riferimento ai seguenti elementi:

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

Allo stesso modo, per restituire tutti i campi (ad eccezione delle autorizzazioni):

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

I percorsi dei nodi sono relativi alla radice dei nodi restituiti. Se si specifica un campo di tipo complesso senza alcun sottoelemento (ad esempio, `assetArray/items/imageInfo`), vengono inclusi tutti i relativi sottoelementi. Se specifichi uno o più elementi secondari in un campo di tipo complesso (ad esempio, `assetArray/items/imageInfo/originalPath`), vengono inclusi solo i sottoelementi.

Se non includi `responseFieldArray` o `excludeFieldArray` in una richiesta vengono restituiti tutti i campi.

**Lingua**

A partire da IPS 4.0, l’API IPS supporta l’impostazione del contesto internazionale di un’operazione passando il `authHeader` parametro locale. Se il parametro locale non è presente, l’intestazione HTTP `Accept-Language` viene utilizzato. Se questa intestazione non è presente, verranno utilizzate le impostazioni internazionali predefinite per il server IPS.

Alcune operazioni utilizzano anche parametri internazionali espliciti, che possono essere diversi dal contesto internazionale delle operazioni. Ad esempio, il `submitJob` l&#39;operazione richiede un `locale` che imposta le impostazioni internazionali utilizzate per la registrazione dei processi e la notifica via e-mail.

I parametri internazionali utilizzano il formato `<language_code>[-<country_code>]`

Se il codice della lingua è un codice a due lettere, minuscolo, specificato dalla norma ISO-639 e il codice del paese opzionale è un codice a due lettere, maiuscolo e minuscolo specificato dalla norma ISO-3266. Ad esempio, la stringa locale per Inglese USA è `en-US`.
