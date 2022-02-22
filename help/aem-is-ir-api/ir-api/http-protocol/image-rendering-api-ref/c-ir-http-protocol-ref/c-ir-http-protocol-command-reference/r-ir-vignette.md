---
title: vignetta
description: File di vignetta. Specifica la vignetta da utilizzare per la richiesta.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8419d68d-7579-4e62-abbd-7dc0a736ae23
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# vignetta{#vignette}

File di vignetta. Specifica la vignetta da utilizzare per la richiesta.

`vignette=[ *`catId`*/] *`recId`*|[catId/] *`file`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>ID catalogo materiale (corrispondente a <span class="codeph"> attributo::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>ID vignetta (corrispondente a <span class="codeph"> vignetta::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p></td> 
  <td class="stentry"> <p>Percorso e nome del file della vignetta relativa. </p></td> 
 </tr> 
</table>

Può specificare una voce di mappa di vignetta o un file di vignetta. Gli URL remoti non sono consentiti.

`vignette=` Può essere utilizzato come alternativa a specificare la vignetta nel percorso URL della richiesta. Utilizzato per specificare le vignette tramite variabili nei modelli.

Se *`catId`* non è specificato, viene utilizzato il catalogo di sessione.

## Proprietà {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Può verificarsi in qualsiasi punto della richiesta. Sostituisce la vignetta specificata con il percorso URL della richiesta.

## Predefinito {#section-db0618d48bc84dc8abcc989550349ccc}

Nessuno.

## Consultate anche {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Cataloghi dei materiali](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2), [Variabili personalizzate](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
