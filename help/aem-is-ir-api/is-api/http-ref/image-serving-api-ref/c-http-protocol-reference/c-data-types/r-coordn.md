---
title: coordN
description: Coordinate normalizzate. Utilizzato per specificare le posizioni relative all'interno di un'immagine, ad esempio offset immagine o parametri di ritaglio, normalizzati alle dimensioni dell'immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
TQID: 'https://experienceleague.adobe.com/-dtYByOGK-mNAWc0yQBs4nu5sO1r-Ormq70iwdDZBjg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 155
ht-degree: 0%

---

# coordN{#coordn}

Coordinate normalizzate. Utilizzato per specificare le posizioni relative all&#39;interno di un&#39;immagine, ad esempio offset immagine o parametri di ritaglio, normalizzati alle dimensioni dell&#39;immagine.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>, <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>scostamento coordinate normalizzato alle dimensioni di un'immagine (reale, reale) </p></td> 
 </tr> 
</table>

I valori positivi si spostano verso il basso a destra.

Spesso, la posizione di riferimento è il centro dell&#39;immagine. In questo caso, `0,0` corrisponde al centro dell&#39;immagine, `-0.5,-0.5` all&#39;angolo in alto a sinistra e `0.5,0.5` all&#39;angolo in basso a destra.

Viene utilizzato anche per specificare la dimensione dell&#39;immagine o del rettangolo rispetto alla dimensione del livello 0. In questo caso, il valore deve essere maggiore di 0. 0 può indicare che deve essere utilizzato un valore predefinito specifico. Un valore di `1,1` specifica una dimensione uguale a quella del livello 0.
