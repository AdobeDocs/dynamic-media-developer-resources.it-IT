---
description: Selezionare l'oggetto in base al nome. Seleziona il gruppo di vignettature specificato per nome e avvia un nuovo MSS.
seo-description: Selezionare l'oggetto in base al nome. Seleziona il gruppo di vignettature specificato per nome e avvia un nuovo MSS.
seo-title: obj
solution: Experience Manager
title: obj
topic: Scene7 Image Serving - Image Rendering API
uuid: 2fede992-6759-45bd-b2f1-36e2c791d536
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%

---


# obj{#obj}

Selezionare l&#39;oggetto in base al nome. Seleziona il gruppo di vignettature specificato per nome e avvia un nuovo MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome del gruppo o percorso/nome. </p> </td> 
 </tr> 
</table>

I sottogruppi o i singoli oggetti possono essere selezionati utilizzando un percorso di gruppo completo (ovvero specificando il nome del gruppo o dell&#39;oggetto di destinazione preceduto da tutti i gruppi principali, separati da / (barre).

Se non viene trovato alcun gruppo/oggetto con il nome specificato, viene eseguita l&#39;azione specificata in `attribute::OnObjFail`.

## Proprietà {#section-9463b36e8ff74c81a70c7c2b58927430}

Selezione, comando; delimitatore MSS. La selezione dell&#39;oggetto è persistente finché non viene selezionato un altro oggetto, con `obj=` o `sel=`.

I percorsi e i nomi dei gruppi/oggetti non fanno distinzione tra maiuscole e minuscole.

## Predefinito {#section-0c322850512c4896bb551856a549440e}

Il primo gruppo nella vignettatura contenente oggetti renderabili viene selezionato automaticamente all’apertura di una nuova vignettatura.

## Consultate anche {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b),  [attribute::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
