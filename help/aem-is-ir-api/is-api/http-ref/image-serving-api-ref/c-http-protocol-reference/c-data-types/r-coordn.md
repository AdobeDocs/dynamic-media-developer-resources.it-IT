---
description: Coordinate normalizzate. Viene usato per specificare le posizioni relative all’interno di un’immagine, ad esempio gli offset dell’immagine o i parametri di ritaglio, normalizzati in base alle dimensioni dell’immagine.
seo-description: Coordinate normalizzate. Viene usato per specificare le posizioni relative all’interno di un’immagine, ad esempio gli offset dell’immagine o i parametri di ritaglio, normalizzati in base alle dimensioni dell’immagine.
seo-title: coordN
solution: Experience Manager
title: coordN
topic: Scene7 Image Serving - Image Rendering API
uuid: e182650b-aff6-4dd2-8edb-cd0d361865fd
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 0%

---


# coordN{#coordn}

Coordinate normalizzate. Viene usato per specificare le posizioni relative all’interno di un’immagine, ad esempio gli offset dell’immagine o i parametri di ritaglio, normalizzati in base alle dimensioni dell’immagine.

<table id="simpletable_EFA3111DC4B94BAF94715500DB4DD8FB"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> coordN</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> nx</span> </span>,  <span class="codeph"><span class="varname"> ny</span></span> </p></td> 
  <td class="stentry"> <p>offset delle coordinate normalizzato in base alle dimensioni di un’immagine (reale, reale) </p></td> 
 </tr> 
</table>

I valori positivi si spostano verso il basso a destra.

In molti casi, la posizione di riferimento è il centro dell’immagine. In questo caso, 0,0 corrisponde al centro dell’immagine, -0,5,-0,5 all’angolo in alto a sinistra e 0,5,0,5 all’angolo in basso a destra.

Usato anche per specificare le dimensioni dell’immagine o del rettangolo in relazione alle dimensioni del livello 0. In questo caso, i valori devono essere maggiori di 0. 0 può indicare che deve essere utilizzato un valore predefinito specifico. 1,1 specifica una dimensione uguale a quella del livello 0.
