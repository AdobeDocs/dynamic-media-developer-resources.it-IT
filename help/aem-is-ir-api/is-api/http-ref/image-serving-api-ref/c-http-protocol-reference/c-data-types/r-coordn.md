---
description: Coordinate normalizzate. Utilizzato per specificare le posizioni relative all’interno di un’immagine, ad esempio offset immagine o parametri di ritaglio, normalizzati in base alle dimensioni dell’immagine.
solution: Experience Manager
title: coordN
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: 3a97a520-5049-4b26-826e-ae913f0ac511
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '150'
ht-degree: 0%

---

# coordN{#coordn}

Coordinate normalizzate. Utilizzato per specificare le posizioni relative all’interno di un’immagine, ad esempio offset immagine o parametri di ritaglio, normalizzati in base alle dimensioni dell’immagine.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>offset delle coordinate normalizzato in base alle dimensioni di un'immagine (reale, reale) </p></td> 
 </tr> 
</table>

I valori positivi si spostano verso il basso a destra.

In molti casi, la posizione di riferimento è il centro dell&#39;immagine. In questo caso, 0,0 corrisponde al centro dell’immagine, -0,5,-0,5 corrisponde all’angolo in alto a sinistra e 0,5,0,5 corrisponde all’angolo in basso a destra.

Utilizzato anche per specificare le dimensioni dell&#39;immagine o del rettangolo rispetto alle dimensioni del livello 0. In questo caso, i valori devono essere maggiori di 0. 0 può indicare che deve essere utilizzato un valore predefinito specifico. 1,1 specifica una dimensione uguale a quella del livello 0.
