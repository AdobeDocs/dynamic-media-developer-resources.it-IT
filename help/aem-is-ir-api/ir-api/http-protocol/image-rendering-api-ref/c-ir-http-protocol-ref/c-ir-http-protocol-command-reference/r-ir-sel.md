---
title: sel
description: Selezionare l'oggetto in base alla posizione dei pixel.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fac33287-ebcc-4995-b968-ac377065fdd4
TQID: 'https://experienceleague.adobe.com/nmXZZFxdpxJTY4j12JRyhCe-sOZIjajFSfzmPId9X3g'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 190
ht-degree: 1%

---

# sel{#sel}

Selezionare l&#39;oggetto in base alla posizione dei pixel.

` sel= *`x`*, *`y`*[, *`livello`*]`

<table id="simpletable_247FF35D791C43D3AB433B8CF49F8C91"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> x,y </span> </p> </td> 
  <td class="stentry"> <p>Scegli le coordinate di posizione in pixel (int, int). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="varname"> livello </span> </p> </td> 
  <td class="stentry"> <p>Livello di gruppo (int). </p> </td> 
 </tr> 
</table>

Seleziona il gruppo o l&#39;oggetto alle coordinate in pixel specificate da *`x, y`* e avvia un nuovo MSS. Se nella posizione di prelievo non è presente alcun oggetto selezionabile o se la posizione di prelievo non è valida, viene eseguita l&#39;azione specificata da `attribute::OnFailSel`.

*`level`* Specifica se selezionare il gruppo più esterno o eseguire il drill-down a un gruppo o a un oggetto nidificato. Se *`level`* non è specificato, viene selezionato il gruppo più esterno. Impostate questo valore su 1 per selezionare un livello di gruppo al di sotto del gruppo più esterno. Impostate un numero elevato (ad esempio 99) per selezionare l&#39;oggetto o il gruppo più interno selezionabile.

## Proprietà {#section-8f27e84d88734a62a5e398e0c9972bdc}

Comando di selezione; delimitatore MSS. La selezione dell&#39;oggetto è permanente finché non viene selezionato un altro oggetto, con `obj=` o `sel=`.

*`x, y`* Deve essere compreso tra 0, 0 (angolo in alto a sinistra dell&#39;immagine) e *`wid`*-1, *`hei`*-1 (angolo in basso a destra dell&#39;immagine), dove *`wid`* e *`hei`* sono le dimensioni della visualizzazione vignettatura non in scala.

Se specificato, *`level`* deve essere maggiore o uguale a 0.

## Predefinito {#section-e13c705a3e76468894b4ec190ed8a893}

Nessuna per *`x, y`*. *`level`* Il valore predefinito è 0.

## Consultate anche {#section-486842570b4e4bf895f6ccc172ebd8b2}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a) , [wid=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-wid.md#reference-b7e691b0624941168c94b2749ae233ec), [hei=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-hei.md#reference-1c08f60365a94417a39867c09cac5478), [attributo::DefaultPix](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-defaultpix.md#reference-102c98f9b5d24d2aaaeb756653fb0e6f), [attributo::OnFailSel](../../../../../ir-api/material-cat/image-rendering-api-ref/c-ir-material-catalog/c-ir-attributes-reference/r-ir-onfailsel.md#reference-f95e4a4a3c02412b87a2b0acca8a5513)
