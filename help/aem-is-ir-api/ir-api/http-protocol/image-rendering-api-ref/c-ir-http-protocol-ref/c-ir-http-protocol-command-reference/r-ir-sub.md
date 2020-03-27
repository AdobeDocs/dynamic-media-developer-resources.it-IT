---
description: Sottoselezione. Consente di applicare materiali diversi a diverse aree dell'oggetto o del gruppo selezionato, nonché di rimuovere i materiali precedentemente applicati.
seo-description: Sottoselezione. Consente di applicare materiali diversi a diverse aree dell'oggetto o del gruppo selezionato, nonché di rimuovere i materiali precedentemente applicati.
seo-title: sub
solution: Experience Manager
title: sub
topic: Scene7 Image Serving - Image Rendering API
uuid: cb9f4dc5-9d89-483a-ae72-b9076b27c57e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# sub{#sub}

Sottoselezione. Consente di applicare materiali diversi a diverse aree dell&#39;oggetto o del gruppo selezionato, nonché di rimuovere i materiali precedentemente applicati.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Selezionate l'intera parete. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Selezionare la metà superiore della parete. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>Selezionare la metà inferiore della parete. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>Selezionare l'area del bordo della parete superiore. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>Selezionare l'area del bordo della parete centrale. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>Selezionare l'area del bordo inferiore della parete. </p> </td> 
 </tr> 
</table>

Attualmente supportato solo per gli oggetti muro. Termina un MSS precedente e avvia un nuovo MSS per il materiale da applicare alla sottoselezione specificata.

Un materiale specificato per la parete superiore o inferiore si applicherà all&#39;intera parete a meno che non sia stato specificato un altro materiale anche per l&#39;altra metà della parete.

## Proprietà {#section-b202139d6d0847cc8d520a154104ab9d}

Selezione, comando; delimitatore MSS.

## Predefinito {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Consultate anche {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
