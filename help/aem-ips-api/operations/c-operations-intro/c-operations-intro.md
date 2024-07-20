---
description: Descrive i parametri operativi comuni gestiti dall'API del servizio Web IPS.
solution: Experience Manager
title: Metodi operativi
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 020c8e63-ad4e-4c0d-8da6-b51efb2b89a5
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 0%

---

# Metodi operativi{#operations-methods}

Questa sezione descrive i parametri operativi comuni gestiti dall&#39;API del servizio Web IPS.

Per una descrizione completa di ciascun parametro dell&#39;operazione, vedere [Parametri dell&#39;operazione](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md).

## Handle: informazioni {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Gestisce gli oggetti IPS di riferimento restituiti da determinate operazioni API. Puoi anche trasmettere gli handle come parametri alle chiamate di operazione successive. Gli handle sono tipi di dati stringa ( `xsd:string`).

Gli handle devono essere utilizzati solo durante una singola sessione dell&#39;applicazione. Inoltre, è necessario rendere gli handle persistenti perché il loro formato può cambiare tra le versioni IPS. Quando si scrivono applicazioni interattive, si implementano timeout di sessione e si eliminano tutti gli handle tra sessioni, in particolare dopo un aggiornamento IPS. Quando scrivi applicazioni non interattive, chiama le operazioni appropriate per recuperare gli handle ogni volta che l’applicazione viene eseguita. I seguenti esempi di codice Java/Axis2 mostrano un’esecuzione del codice errata e corretta:

**Codice handle Non Corretto**

Questo esempio di codice non è corretto perché contiene un valore hardcoded (555) per l’handle aziendale.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Codice handle corretto**

Questo esempio di codice è corretto perché chiama `getCompanyInfo` per restituire un handle valido. Non si basa su un valore hardcoded. Utilizza questo metodo o un’altra API IPS equivalente per restituire l’handle richiesto.

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

La maggior parte delle operazioni richiede l&#39;impostazione di un contesto aziendale passando un parametro `companyHandle`. L&#39;handle dell&#39;azienda è un puntatore restituito da operazioni quali `getCompanyInfo`, `addCompany` e `getCompanyMembership`.

**userHandle**

Il parametro `userHandle` è un parametro facoltativo per le operazioni destinate a un utente specifico. Per impostazione predefinita, queste operazioni sono indirizzate all’utente chiamante (l’utente le cui credenziali vengono passate per l’autenticazione). Tuttavia, gli utenti amministratori con le autorizzazioni appropriate possono specificare un utente diverso. L&#39;operazione `setPassword`, ad esempio, imposta in genere la password dell&#39;utente autenticato, ma un amministratore può utilizzare il parametro `userHandle` per impostare la password per un altro utente.

Per le operazioni che richiedono un contesto aziendale (utilizzando il parametro `companyHandle`), sia gli utenti autenticati che quelli di destinazione devono essere membri della società specificata. Per le operazioni che non richiedono un contesto aziendale, gli utenti autenticati e di destinazione devono essere membri di almeno una società comune.

Le operazioni seguenti possono recuperare gli handle utente:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle e accessGroupHandle**

Per impostazione predefinita, le operazioni che richiedono autorizzazioni di accesso (lettura, scrittura, eliminazione) funzionano nel contesto delle autorizzazioni dell&#39;utente chiamante. Alcune operazioni consentono di modificare questo contesto con il parametro `accessUserHandle` o `accessGroupHandle`. Il parametro `accessUserHandle` consente a un amministratore di rappresentare un altro utente. Il parametro `accessGroupHandle` consente al chiamante di operare nel contesto di un gruppo di utenti specifico.

**responseFieldArray ed excludeFieldArray**

Alcune operazioni consentono al chiamante di limitare quali campi sono inclusi nella risposta. Limitare i campi può contribuire a ridurre il tempo e la memoria necessari per elaborare la richiesta e la dimensione dei dati di risposta. Il chiamante può richiedere un elenco specifico di campi passando un parametro `responseFieldArray` o con un elenco enumerato di campi esclusi tramite il parametro `excludeFieldArray`.

Sia `responseFieldArray` che `excludeFieldArray` specificano i campi utilizzando un percorso del nodo separato da `/`. Ad esempio, per specificare che `searchAssets` restituisce solo il nome, la data dell&#39;ultima modifica e i metadati di ciascuna risorsa, fai riferimento a quanto segue:

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

I percorsi dei nodi sono relativi alla radice del nodo restituito. Se si specifica un campo di tipo complesso senza i relativi sottoelementi (ad esempio, `assetArray/items/imageInfo`), verranno inclusi tutti i relativi sottoelementi. Se si specificano uno o più elementi secondari in un campo di tipo complesso, ad esempio `assetArray/items/imageInfo/originalPath`, verranno inclusi solo tali elementi secondari.

Se non includi `responseFieldArray` o `excludeFieldArray` in una richiesta, vengono restituiti tutti i campi.

**Impostazioni locali**

A partire da IPS 4.0, l&#39;API IPS supporta l&#39;impostazione del contesto delle impostazioni locali di un&#39;operazione passando il parametro delle impostazioni locali `authHeader`. Se il parametro locale non è presente, viene utilizzata l&#39;intestazione HTTP `Accept-Language`. Se anche questa intestazione non è presente, viene utilizzata la lingua predefinita per il server IPS.

Alcune operazioni utilizzano inoltre parametri locali espliciti, che possono essere diversi dal contesto locale dell&#39;operazione. L&#39;operazione `submitJob`, ad esempio, accetta un parametro `locale` che imposta le impostazioni locali utilizzate per la registrazione dei processi e la notifica e-mail.

I parametri delle impostazioni internazionali utilizzano il formato `<language_code>[-<country_code>]`

Se il codice lingua è un codice a due lettere minuscole specificato dalla norma ISO-639 e il codice paese facoltativo è un codice a due lettere maiuscole specificato dalla norma ISO-3266. Ad esempio, la stringa delle impostazioni internazionali per l&#39;inglese US è `en-US`.
