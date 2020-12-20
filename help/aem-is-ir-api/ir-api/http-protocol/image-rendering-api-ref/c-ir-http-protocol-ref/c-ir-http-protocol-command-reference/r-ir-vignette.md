---
description: Vignettatura. Specifica la vignettatura da utilizzare per questa richiesta.
seo-description: Vignettatura. Specifica la vignettatura da utilizzare per questa richiesta.
seo-title: vignettatura
solution: Experience Manager
title: vignettatura
topic: Scene7 Image Serving - Image Rendering API
uuid: 8bba4ad4-bd55-4c55-8ebf-585371cf33f1
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 3%

---


# vignettatura{#vignette}

Vignettatura. Specifica la vignettatura da utilizzare per questa richiesta.

`vignette=[ *``*/] *``*|[catId/] *`catIdrecIdfile`*`

<table id="simpletable_432EC5501CA3431B83A762C3EE4E8DD2"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> catId</span> </p> </td> 
  <td class="stentry"> <p>ID catalogo materiali (associato all'attributo <span class="codeph">::RootId</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> recId</span> </p></td> 
  <td class="stentry"> <p>ID vignettatura (associato a <span class="codeph"> vignettatura::Id</span>). </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="varname"> file</span> </p></td> 
  <td class="stentry"> <p>Percorso e nome del file di vignettatura relativo. </p></td> 
 </tr> 
</table>

È possibile specificare una voce di mappa di vignettatura o un file di vignettatura. Gli URL remoti non sono consentiti.

`vignette=` può essere utilizzato come alternativa per specificare la vignettatura nel percorso dell’URL della richiesta. Utilizzata principalmente per specificare le vignettature tramite variabili nei modelli.

Se *`catId`* non è specificato, viene utilizzato il catalogo delle sessioni.

## Proprietà {#section-f58661fc78d7496e8e3d0fb98b945c4b}

Può verificarsi ovunque nella richiesta. Sostituisce la vignettatura specificata con il percorso URL della richiesta.

## Predefinito {#section-db0618d48bc84dc8abcc989550349ccc}

Nessuno.

## Consultate anche {#section-dc2668cc2cd54a74b08cff68a12d4edd}

[Cataloghi](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-http-material-catalogs/c-ir-http-material-catalogs.md#concept-772742c1688f420a88a56f5136ad1db2) materiali, variabili  [personalizzate](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-syntax-and-features/c-ir-custom-variables/c-ir-custom-variables.md#concept-8a1d9a50d09a4b7b97b8c83365971f96)
