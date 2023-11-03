---
title: obj
description: Selezionare l'oggetto per nome. Seleziona il gruppo di vignettatura specificato per nome e avvia un nuovo MSS.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 17387203-f7a7-4876-a15b-2084894f981d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---

# obj{#obj}

Selezionare l&#39;oggetto per nome. Seleziona il gruppo di vignettatura specificato per nome e avvia un nuovo MSS.

` obj= *`nome`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> nome </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome o percorso/nome del gruppo. </p> </td> 
 </tr> 
</table>

I sottogruppi o i singoli oggetti possono essere selezionati utilizzando un percorso di gruppo completo, ovvero specificando il nome del gruppo di destinazione o dell&#39;oggetto preceduto da tutti i gruppi padre, separati da / (barre).

Se non viene trovato alcun gruppo/oggetto con il nome specificato, l&#39;azione specificata in `attribute::OnObjFail` viene eseguita.

## Proprietà {#section-9463b36e8ff74c81a70c7c2b58927430}

Comando di selezione; delimitatore MSS. La selezione dell&#39;oggetto è permanente finché non viene selezionato un altro oggetto, con `obj=` o `sel=`.

I percorsi e i nomi di gruppi/oggetti non fanno distinzione tra maiuscole e minuscole.

## Predefinito {#section-0c322850512c4896bb551856a549440e}

Il primo gruppo della vignettatura contenente oggetti renderizzabili viene selezionato automaticamente all&#39;apertura di una nuova vignettatura.

## Consultate anche {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b), [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
