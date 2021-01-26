---
description: Gestione degli errori di selezione degli oggetti. Specifica l'azione da eseguire se il comando obj= non riesce perché il percorso specificato non corrisponde nella gerarchia degli oggetti di vignettatura.
seo-description: Gestione degli errori di selezione degli oggetti. Specifica l'azione da eseguire se il comando obj= non riesce perché il percorso specificato non corrisponde nella gerarchia degli oggetti di vignettatura.
seo-title: OnFailObj
solution: Experience Manager
title: OnFailObj
topic: Dynamic Media Image Serving - Image Rendering API
uuid: b9dcaf29-ffa5-47db-9c8c-d1809da73582
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 11%

---


# OnFailObj{#onfailobj}

Gestione degli errori di selezione degli oggetti. Specifica l&#39;azione da eseguire se il comando obj= non riesce perché il percorso specificato non corrisponde nella gerarchia degli oggetti di vignettatura.

## Proprietà {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Ereditare da <span class="codeph"> default::OnFailObj </span>. </p> </td> 
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

## Predefinito {#section-a5a95a2b4a204a4eae350e5b544d1513}

Ereditato da `default::OnFailObj` se non definito.

## Consultate anche {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [attributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
