---
description: Sottoselezione. Consente di applicare materiali diversi a diverse aree dell'oggetto o del gruppo selezionato, nonché di rimuovere i materiali precedentemente applicati.
solution: Experience Manager
title: sub
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 6%

---


# sub{#sub}

Sottoselezione. Consente di applicare materiali diversi a diverse aree dell&#39;oggetto o del gruppo selezionato, nonché di rimuovere i materiali precedentemente applicati.

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>Selezionare l'intera parete. </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>Selezionare la metà superiore del muro. </p> </td> 
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
  <td class="stentry"> <p>Selezionare l'area del bordo della parete inferiore. </p> </td> 
 </tr> 
</table>

Attualmente supportato solo per gli oggetti wall. Termina un MSS precedente e avvia un nuovo MSS per il materiale da applicare alla sottoselezione specificata.

Un materiale specificato per la parete superiore o inferiore si applica all&#39;intera parete a meno che non sia stato specificato un materiale diverso anche per l&#39;altra metà della parete.

## Proprietà {#section-b202139d6d0847cc8d520a154104ab9d}

comando di selezione; delimitatore MSS.

## Predefinito {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## Consultate anche {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
