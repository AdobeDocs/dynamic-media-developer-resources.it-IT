---
title: coordN
description: Coordinate normalizzate. Utilizzato per specificare le posizioni relative all'interno di un'immagine, ad esempio offset immagine o parametri di ritaglio, normalizzati alle dimensioni dell'immagine.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '148'
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

Spesso, la posizione di riferimento è il centro dell&#39;immagine. In questo caso, `0,0` corrisponde al centro dell’immagine, `-0.5,-0.5` in alto a sinistra, e `0.5,0.5` nell’angolo in basso a destra.

Viene utilizzato anche per specificare la dimensione dell&#39;immagine o del rettangolo rispetto alla dimensione del livello 0. In questo caso, il valore deve essere maggiore di 0. 0 può indicare che deve essere utilizzato un valore predefinito specifico. Un valore di `1,1` specifica una dimensione uguale a quella del livello 0.
