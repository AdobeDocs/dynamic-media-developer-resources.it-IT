---
description: Selezionare l’oggetto in base al nome. Seleziona il gruppo di vignette specificato per nome e avvia un nuovo MSS.
solution: Experience Manager
title: obj
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 3%

---


# obj{#obj}

Selezionare l’oggetto in base al nome. Seleziona il gruppo di vignette specificato per nome e avvia un nuovo MSS.

` obj= *`name`*`

<table id="simpletable_6E0DA6CBCDCF4CDDAFA5A4C38E0D5FC5"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> name  </span> </span> </p> </td> 
  <td class="stentry"> <p>Nome del gruppo o percorso/nome. </p> </td> 
 </tr> 
</table>

I sottogruppi o i singoli oggetti possono essere selezionati utilizzando un percorso di gruppo completo (ovvero specificando il nome del gruppo o dell’oggetto di destinazione preceduto da tutti i gruppi principali, separati da / (barre).

Se non viene trovato alcun gruppo/oggetto con il nome specificato, viene eseguita l&#39;azione specificata in `attribute::OnObjFail`.

## Proprietà {#section-9463b36e8ff74c81a70c7c2b58927430}

comando di selezione; delimitatore MSS. La selezione dell’oggetto è permanente finché non viene selezionato un altro oggetto, sia con `obj=` che con `sel=`.

I nomi e i percorsi dei gruppi/oggetti non fanno distinzione tra maiuscole e minuscole.

## Predefinito {#section-0c322850512c4896bb551856a549440e}

Il primo gruppo della vignetta contenente oggetti renderizzabili viene selezionato automaticamente all’apertura di una nuova vignetta.

## Consultate anche {#section-d9d2c92ef48548f48b9781e2a8a5fb5a}

[sel=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-sel.md#reference-01322c58d414481385c29fcdd27a090b),  [attributo::OnFailObj](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailobj.md#reference-4c6ba90418e84da5831f8573bbbf2c8d)
