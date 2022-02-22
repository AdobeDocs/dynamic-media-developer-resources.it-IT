---
title: venditrice
description: Selezionare l'oggetto in base alla posizione dei pixel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---

# venditrice{#sel}

Selezionare l&#39;oggetto in base alla posizione dei pixel.

` sel= *`x`*, *`y`*[, *`livello`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>Selezionare le coordinate di posizione in pixel (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> livello </span> </p> </td> 
  <td class="stentry"> <p>Livello di gruppo (int). </p> </td> 
 </tr> 
</table>

Seleziona il gruppo o l&#39;oggetto in corrispondenza delle coordinate pixel specificate da *`x, y`* e avvia un nuovo MSS. Se nessun oggetto selezionabile si trova nella posizione di prelievo o se la posizione di prelievo non è valida, l&#39;azione specificata da `attribute::OnFailSel` è preso.

*`level`* Specifica se selezionare il gruppo più esterno o eseguire il drill-down a un gruppo o a un oggetto nidificato. Se *`level`* non è specificato, viene selezionato il gruppo più esterno. Impostare su 1 per selezionare un livello di gruppo al di sotto del gruppo più esterno. Impostare su un numero elevato (ad esempio 99) per selezionare l&#39;oggetto o il gruppo più interno selezionabile.

## Proprietà {#section-8f27e84d88734a62a5e398e0c9972bdc}

comando di selezione; delimitatore MSS. La selezione dell’oggetto è persistente fino a quando non viene selezionato un altro oggetto, con `obj=` o `sel=`.

*`x, y`* Deve essere compreso tra 0, 0 (angolo in alto a sinistra dell’immagine) e *`wid`*-1, *`hei`*-1 (angolo inferiore destro dell&#39;immagine), dove *`wid`* e *`hei`* è la dimensione della visualizzazione della vignetta non ridimensionata.

Se specificato, *`level`* deve essere maggiore o uguale a 0.

## Predefinito {#section-e13c705a3e76468894b4ec190ed8a893}

Nessuno per *`x, y`*. *`level`* Il valore predefinito è 0.

## Consultate anche {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
