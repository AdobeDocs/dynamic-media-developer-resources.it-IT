---
title: OnFailSel
description: Selezione della gestione degli errori di selezione. Specifica l'azione da eseguire se il comando sel= ha esito negativo perché la posizione del pixel specificata non si trova nell'area della maschera di un oggetto selezionabile.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d5485569-def8-4e16-9f0e-7dd30d38439d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 13%

---

# OnFailSel{#onfailsel}

Selezione della gestione degli errori di selezione. Specifica l&#39;azione da eseguire se la `sel=` il comando non riesce perché la posizione del pixel specificata non si trova nell&#39;area della maschera di un oggetto selezionabile.

## Proprietà {#section-cec491e6c5c744f9bfafaaa9d8774f83}

Enum.

<table id="simpletable_1CFD2BC6F9BC4D2AB372EAF115B7F2FC"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Eredita da <span class="codeph"> predefinito::OnFailSel </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Mantieni selezione precedente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Deselezionare; qualsiasi tentativo di applicare un materiale o mostrare/nascondere oggetti viene ignorato. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Restituisci un errore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Selezionare il gruppo predefinito (il primo gruppo nella gerarchia delle vignette che contiene oggetti renderizzabili). </p> </td> 
 </tr> 
</table>

## Predefinito {#section-c25f458f9f8f4236963a95779529e664}

Ereditato da `default::OnFailSel` se non definito.

## Consultate anche {#section-f8b15dd64c674c5484d190dd9e3016af}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b) , [attributo::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
