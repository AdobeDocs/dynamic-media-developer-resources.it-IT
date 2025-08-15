---
description: Vengono descritti i parametri operativi comuni gestiti dall'API del servizio Web IPS.
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

In questa sezione vengono descritti i parametri operativi comuni gestiti dall&#39;API del servizio Web IPS.

Per una descrizione completa di ciascun parametro dell&#39;operazione, vedere [Parametri](/help/aem-ips-api/operations/c-operations-intro/c-methods/c-methods.md) operativi.

## Maniglie:Informazioni {#section-094ce1afa6244fa5b2c762f44ffdca1c}

Gestisce gli oggetti IPS di riferimento restituiti da determinate operazioni API. È inoltre possibile passare handle come parametri alle chiamate di operazione successive. Gli handle sono tipi di dati stringa ( `xsd:string`).

Gli handle sono destinati all&#39;uso durante una sola sessione applicazione. Inoltre, è consigliabile rendere gli handle persistenti perché il loro formato può cambiare tra una versione IPS e l&#39;altra. Quando scrivete applicazioni interattive, implementare i timeout delle sessioni ed eliminate tutti gli handle tra una sessione e l&#39;altra, in particolare dopo un aggiornamento IPS. Quando si scrivono applicazioni non interattive, chiamare le operazioni appropriate per recuperare gli handle ogni volta che viene eseguito il applicazione. I seguenti esempi di codice Java/Axis2 mostrano un&#39;esecuzione di codice non corretta e corretta:

**Code handle errato**

Questo esempio di codice non è corretto perché contiene un valore hardcoded (555) per l&#39;handle aziendale.

```
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle("555");// INCORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

**Handle corretto Code**

Questo esempio di codice è corretto perché richiede `getCompanyInfo` di restituire un handle valido. Non si basa su un valore hardcoded. Utilizza questo metodo o altre API IPS equivalenti per restituire l&#39;handle richiesto.

```
GetCompanyInfoParam companyInfoParam = new GetCompanyInfoParam(); 
companyInfoParam.setCompanyName("My Company"); GetCompanyInfoReturn companyInfoReturn = ipsApi.getCompanyInfo(companyInfoParam, authHeader); 
String companyHandle = companyInfoReturn.getCompanyInfo().getCompanyHandle(); 
SearchAssetsParam searchParam = new SearchAssetsParam(); searchParam.setCompanyHandle(companyHandle); //CORRECT 
searchParam.setFolder("myFolder"); 
SearchAssetsReturn retVal = ipsApi.searchAssets(searchParam, authHeader);
```

## Tipi di handle comuni {#section-e683ac8283284f9688e63f51a494f7a0}

**CompanyHandle**

Per la maggior parte delle operazioni è necessario impostare un contesto aziendale trasmettendo un `companyHandle` parametro. L&#39;handle aziendale è un puntatore restituito da alcune operazioni come `getCompanyInfo`, `addCompany`, e `getCompanyMembership`.

**Handle utente**

Il `userHandle` parametro è facoltativo per le operazioni che destinazione un utente specifico. Per impostazione predefinita, queste operazioni destinazione il utente chiamante (il utente le cui credenziali vengono passate per l&#39;autenticazione). Tuttavia, gli utenti amministratore con le autorizzazioni appropriate possono specificare una utente diversa. Ad esempio, l&#39;operazione `setPassword` normalmente imposta il password del utente autenticato, ma un amministratore può utilizzare il `userHandle` parametro per impostare il password per un utente diverso.

Per le operazioni che richiedono un contesto aziendale (utilizzando il `companyHandle` parametro), sia gli utenti autenticati che quelli destinazione devono essere membri della società specificata. Per le operazioni che non richiedono un contesto aziendale, gli utenti autenticati e destinazione devono essere entrambi membri di almeno una società comune.

Le seguenti operazioni consentono di recuperare utente handle:

* `getUsers`
* `getAllUsers`
* `getUserInfo`
* `getCompanyMembers`
* `getGroupMembers`
* `addUser`

**accessUserHandle e accessGroupHandle**

Per impostazione predefinita, le operazioni che richiedono autorizzazioni accesso (lettura, scrittura, eliminazione) operano nel contesto autorizzazione del utente chiamante. Alcune operazioni consentono di modificare questo contesto con il `accessUserHandle` parametro or `accessGroupHandle` . Il `accessUserHandle` parametro consente a un amministratore di impersonare un&#39;altra utente. Il `accessGroupHandle` parametro consente al chiamante di operare nel contesto di un gruppo di utente specifico.

**responseFieldArray e excludeFieldArray**

Alcune operazioni consentono al chiamante di limitare i campi inclusi nella risposta. La limitazione dei campi consente di ridurre il tempo e la memoria necessari per elaborare il richiesta e ridurre le dimensioni dei dati di risposta. Il chiamante può richiesta un elenco specifico di campi passando un `responseFieldArray` parametro o con un elenco enumerato di campi esclusi tramite il `excludeFieldArray` parametro.

Entrambi `responseFieldArray` e `excludeFieldArray` specificare i campi utilizzando un percorso di nodo separato da `/`. Ad esempio, per specificare che `searchAssets` restituisce solo il nome, la data dell&#39;ultima modifica e il metadati per ogni risorsa fare riferimento a quanto segue:

```
<responseFieldArray> 
   <items>assetArray/items/name</items> 
   <items>assetArray/items/lastModified</items> 
   <items>assetArray/items/metadataArray</items> 
</responseFieldArray>
```

Analogamente, per restituire tutti i campi (ad eccezione delle autorizzazioni):

```
<excludeFieldArray> 
   <items>assetArray/items/permissions</items> 
</excludeFieldArray>
```

Si noti che i percorsi dei nodi sono relativi alla radice del nodo di ritorno. Se si specifica un campo di tipo complesso senza alcuno dei relativi sottoelementi (ad esempio, `assetArray/items/imageInfo`), vengono inclusi tutti i relativi sottoelementi. Se si specificano uno o più sottoelementi in un campo di tipo complesso (ad esempio, `assetArray/items/imageInfo/originalPath`), vengono inclusi solo tali sottoelementi.

Se non includete `responseFieldArray` o `excludeFieldArray` fate parte di un richiesta, vengono restituiti tutti i campi.

**Scena**

A partire da IPS 4.0, l&#39;API IPS supporta l&#39;impostazione del contesto locale di un&#39;operazione trasmettendo il `authHeader` parametro locale. Se il parametro locale non è presente, viene utilizzata l&#39;intestazione `Accept-Language` HTTP. Se anche questa intestazione non è presente, viene utilizzata la lingua predefinita per il server IPS.

Alcune operazioni accettano anche parametri internazionali espliciti, che possono essere diversi dal contesto delle impostazioni internazionali dell&#39;operazione. Ad esempio, l&#39;operazione `submitJob` accetta un `locale` parametro che imposta le impostazioni internazionali utilizzate per registrazione di lavoro e notifica di posta elettronica.

I parametri delle impostazioni internazionali utilizzano il formato `<language_code>[-<country_code>]`

Se il codice della lingua è un codice di due lettere minuscolo specificato da ISO-639 e il codice facoltativo del paese è un codice maiuscolo di due lettere specificato da ISO-3266. Ad esempio, la stringa delle impostazioni internazionali per gli Inglese statunitensi è `en-US`.
