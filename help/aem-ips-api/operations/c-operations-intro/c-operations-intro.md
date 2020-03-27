---
description: Questa sezione descrive i parametri operativi comuni gestiti dall'API del servizio Web IPS.
seo-description: Questa sezione descrive i parametri operativi comuni gestiti dall'API del servizio Web IPS.
seo-title: Metodi delle operazioni
solution: Experience Manager
title: Metodi delle operazioni
topic: Scene7 Image Production System API
uuid: 713646a7-1108-4f93-bec2-3fbe7e548515
translation-type: tm+mt
source-git-commit: 806e7e670ee98e1fb6adf52ffc95fb989fa69400

---


# Metodi delle operazioni{#operations-methods}

Questa sezione descrive i parametri operativi comuni gestiti dall&#39;API del servizio Web IPS.

Per una descrizione completa di ciascun parametro di operazione, vedete Parametri [di](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md)operazione.

## Maniglie: Informazioni {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Handle fanno riferimento agli oggetti IPS restituiti da alcune operazioni API. È inoltre possibile trasmettere handle come parametri alle chiamate di operazione successive. I gestori sono tipi di dati stringa ( `xsd:string`).

Le maniglie sono destinate a essere utilizzate solo durante una singola sessione di applicazione. Inoltre, è necessario rendere persistenti i handle, in quanto il loro formato può variare tra le versioni IPS. Quando scrivete applicazioni interattive, implementate i timeout delle sessioni ed eliminate tutti i handle tra le sessioni, in particolare dopo un aggiornamento IPS. Quando scrivete applicazioni non interattive, richiamate le operazioni appropriate per recuperare i handle ogni volta che l&#39;applicazione viene eseguita. I seguenti esempi di codice Java/Axis2 mostrano un&#39;esecuzione del codice errata e corretta:

**Codice Handle Errato**

Questo esempio di codice non è corretto perché contiene un valore hardcoded (555) per l&#39;handle della società.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Correggi codice di handle**

Questo esempio di codice è corretto perché richiama `getCompanyInfo` per restituire un handle valido. Non si basa su un valore hardcoded. Utilizzate questo metodo o un&#39;altra API IPS equivalente per restituire l&#39;handle richiesto.

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

La maggior parte delle operazioni richiede di impostare un contesto aziendale trasmettendo un `companyHandle` parametro. L&#39;handle della società è un puntatore restituito da alcune operazioni quali `getCompanyInfo`, `addCompany`e `getCompanyMembership`.

**userHandle**

Il `userHandle` parametro è un parametro facoltativo per le operazioni che riguardano un utente specifico. Per impostazione predefinita, queste operazioni sono destinate all&#39;utente chiamante (l&#39;utente le cui credenziali vengono trasmesse per l&#39;autenticazione). Tuttavia, gli utenti admin con le autorizzazioni corrette possono specificare un altro utente. Ad esempio, l&#39; `setPassword` operazione normalmente imposta la password dell&#39;utente autenticato, ma un amministratore può utilizzare il `userHandle` parametro per impostare la password per un altro utente.

Per le operazioni che richiedono un contesto aziendale (utilizzando il `companyHandle` parametro), gli utenti autenticati e target devono essere membri della società specificata. Per le operazioni che non richiedono un contesto aziendale, gli utenti autenticati e target devono essere entrambi membri di almeno una società comune.

Le seguenti operazioni possono recuperare le handle utente:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle e accessGroupHandle**

Per impostazione predefinita, le operazioni che richiedono autorizzazioni di accesso (lettura, scrittura, eliminazione) operano nel contesto delle autorizzazioni dell&#39;utente chiamante. Alcune operazioni consentono di modificare questo contesto con il `accessUserHandle` parametro o `accessGroupHandle` . Il `accessUserHandle` parametro consente a un amministratore di rappresentare un altro utente. Il `accessGroupHandle` parametro consente al chiamante di funzionare nel contesto di un gruppo utente specifico.

**responseFieldArray e excludeFieldArray**

Alcune operazioni consentono al chiamante di limitare i campi inclusi nella risposta. Limitando i campi è possibile ridurre il tempo e la memoria necessari per elaborare la richiesta e ridurre la dimensione dei dati della risposta. Il chiamante può richiedere un elenco specifico di campi passando un `responseFieldArray` parametro, oppure un elenco enumerato di campi esclusi tramite il `excludeFieldArray` parametro.

Entrambi `responseFieldArray` e `excludeFieldArray` specificare i campi utilizzando un percorso nodo separato da `/`. Ad esempio, per specificare che `searchAssets` restituisce solo il nome, la data dell’ultima modifica e i metadati di ciascuna risorsa, consultate i seguenti riferimenti:

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

I percorsi dei nodi sono relativi alla radice del nodo restituito. Se si specifica un campo di tipo complesso senza i relativi sottoelementi (ad esempio, `assetArray/items/imageInfo`), vengono inclusi tutti i relativi sottoelementi. Se si specifica uno o più sottoelementi in un campo di tipo complesso (ad esempio, `assetArray/items/imageInfo/originalPath`), vengono inclusi solo tali elementi secondari.

Se non includete `responseFieldArray` o `excludeFieldArray` in una richiesta, vengono restituiti tutti i campi.

**Lingua**

A partire da IPS 4.0, l&#39;API IPS supporta l&#39;impostazione del contesto internazionale di un&#39;operazione, passando il parametro `authHeader` locale. Se il parametro locale non è presente, verrà utilizzata l&#39;intestazione HTTP `Accept-Language` . Se questa intestazione non è presente, verranno utilizzate le impostazioni internazionali predefinite per il server IPS.

Alcune operazioni utilizzano anche parametri di impostazione internazionale espliciti, che possono essere diversi dal contesto delle impostazioni internazionali dell&#39;operazione. Ad esempio, l&#39; `submitJob` operazione richiede un `locale` parametro che imposta le impostazioni internazionali utilizzate per la registrazione dei processi e la notifica e-mail.

I parametri delle impostazioni internazionali utilizzano il formato `<language_code>[-<country_code>]`

Se il codice della lingua è un codice di due lettere minuscoli specificato dallo standard ISO-639 e il codice del paese opzionale è un codice di due lettere maiuscole specificato dallo standard ISO-3266. Ad esempio, la stringa per l&#39;inglese USA è `en-US`.
