---
description: Gestione degli errori di selezione. Specifica l'azione da eseguire se il comando sel= ha esito negativo perché la posizione in pixel specificata non si trova all'interno dell'area della maschera di un oggetto selezionabile.
seo-description: Gestione degli errori di selezione. Specifica l'azione da eseguire se il comando sel= ha esito negativo perché la posizione in pixel specificata non si trova all'interno dell'area della maschera di un oggetto selezionabile.
seo-title: OnFailSel
solution: Experience Manager
title: OnFailSel
topic: Scene7 Image Serving - Image Rendering API
uuid: 073b6651-970c-460c-b044-e3ef37cc677a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# OnFailSel{#onfailsel}

Gestione degli errori di selezione. Specifica l&#39;azione da eseguire se il comando sel= ha esito negativo perché la posizione in pixel specificata non si trova all&#39;interno dell&#39;area della maschera di un oggetto selezionabile.

## Proprietà {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Enum.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Eredita da <span class="codeph"> default::OnFailSel </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Mantieni selezione precedente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Deselezionare; eventuali tentativi di applicare un materiale o mostrare o nascondere oggetti verranno ignorati. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Restituisci un errore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Selezionare il gruppo predefinito (il primo gruppo nella gerarchia di vignettatura che contiene oggetti renderable). </p> </td> 
 </tr> 
</table>

## Predefinito {#section-c25f458f9f8f4236963a95779529e664}

Ereditato da `default::OnFailSel` se non definito.

## Consultate anche {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
