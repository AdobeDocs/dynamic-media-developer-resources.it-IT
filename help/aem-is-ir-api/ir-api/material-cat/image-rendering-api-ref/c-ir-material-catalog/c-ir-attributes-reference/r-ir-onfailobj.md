---
title: OnFailObj
description: Gestione degli errori nella selezione degli oggetti. Specifica l'azione da eseguire se il comando obj= non riesce perché il percorso specificato non corrisponde nella gerarchia degli oggetti di vignettatura.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 0ed04daf-1797-4c12-ae6d-a9a008de9d1d
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '113'
ht-degree: 7%

---

# OnFailObj{#onfailobj}

Gestione degli errori nella selezione degli oggetti. Specifica l&#39;azione da eseguire se il comando obj= non riesce perché il percorso specificato non corrisponde nella gerarchia degli oggetti di vignettatura.

## Proprietà {#section-2c779d9c133a443d9f0aed9fde7b703c}

Enum.

<table id="simpletable_538B76AB784D4DEE9B8021A6BDCE06AB"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Eredita da <span class="codeph"> impostazione predefinita::OnFailObj </span>. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Mantieni la selezione precedente. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Deselezionate questa opzione; qualsiasi tentativo di applicare un materiale o di mostrare/nascondere oggetti viene ignorato. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Restituisce un errore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Selezionate il gruppo predefinito (il primo gruppo nella gerarchia di vignettatura contenente oggetti renderizzabili). </p> </td> 
 </tr> 
</table>

## Predefinito {#section-a5a95a2b4a204a4eae350e5b544d1513}

Ereditato da `default::OnFailObj` se non definito.

## Consultate anche {#section-806dc2c5973c41f683af085b3315043c}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [attributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
