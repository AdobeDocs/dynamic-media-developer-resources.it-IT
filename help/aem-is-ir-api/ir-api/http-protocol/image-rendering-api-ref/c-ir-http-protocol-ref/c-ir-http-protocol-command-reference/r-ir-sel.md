---
description: Selezionare l'oggetto per posizione in pixel.
seo-description: Selezionare l'oggetto per posizione in pixel.
seo-title: sel
solution: Experience Manager
title: sel
topic: Scene7 Image Serving - Image Rendering API
uuid: 2a679284-9da4-44b6-b495-8e1a47296e7c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sel{#sel}

Selezionare l&#39;oggetto per posizione in pixel.

` sel= *``*, *``*[, *`xylevel`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>Scegliete le coordinate di posizione in pixel (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> level </span> </p> </td> 
  <td class="stentry"> <p>Livello gruppo (int). </p> </td> 
 </tr> 
</table>

Seleziona il gruppo o l&#39;oggetto in corrispondenza delle coordinate pixel specificate da *`x, y`* e avvia un nuovo MSS. Se nessun oggetto selezionabile si trova nella posizione di prelievo, o se la posizione di prelievo non è valida, `attribute::OnFailSel` viene eseguita l&#39;azione specificata da.

*`level`* specifica se selezionare il gruppo più esterno o eseguire il drill-down a un gruppo o a un oggetto nidificato. Se non *`level`* viene specificato, viene selezionato il gruppo più esterno. Impostate su 1 per selezionare un livello di gruppo sotto il gruppo più esterno. Impostare su un numero elevato (ad esempio 99) per selezionare l&#39;oggetto o il gruppo più interno selezionabile.

## Proprietà {#section-8f27e84d88734a62a5e398e0c9972bdc}

Selezione, comando; delimitatore MSS. La selezione dell&#39;oggetto è persistente finché non viene selezionato un altro oggetto, con `obj=` o `sel=`.

*`x, y`* deve essere compreso tra 0, 0 (angolo in alto a sinistra dell’immagine) e *`wid`*-1, *`hei`*-1 (angolo in basso a destra dell’immagine), dove *`wid`* ed *`hei`* è la dimensione della vista vignettatura non ridimensionata.

Se specificato, *`level`* deve essere 0 o superiore.

## Predefinito {#section-e13c705a3e76468894b4ec190ed8a893}

Nessuno per *`x, y`*. *`level`* il valore predefinito è 0.

## Consultate anche {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
