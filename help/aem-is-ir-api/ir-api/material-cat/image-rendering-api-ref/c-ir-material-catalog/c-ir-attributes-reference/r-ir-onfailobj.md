---
description: Gestione degli errori di selezione degli oggetti. Specifica l'azione da eseguire se il comando obj= non riesce perché il percorso specificato non può essere corrispondente nella gerarchia degli oggetti vignetta.
solution: Experience Manager
title: OnFailObj
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 13%

---


# OnFailObj{#onfailobj}

Gestione degli errori di selezione degli oggetti. Specifica l&#39;azione da eseguire se il comando obj= non riesce perché il percorso specificato non può essere corrispondente nella gerarchia degli oggetti vignetta.

## Proprietà {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Eredita da <span class="codeph"> predefinito::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Mantieni selezione precedente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Deselezionare; eventuali tentativi di applicare un materiale o mostrare/nascondere oggetti verranno ignorati. </p> </td> 
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

## Predefinito {#section-a5a95a2b4a204a4eae350e5b544d1513}

Ereditato da `default::OnFailObj` se non definito.

## Consultate anche {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) ,  [attributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
