---
description: Requisiti simili a quelli dell'esempio A, ma con sfondo a tinta unita e possibilità di variare l'altezza del composito, per adattare le immagini con proporzioni diverse.
solution: Experience Manager
title: Esempio B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# Esempio B{#example-b}

Requisiti simili a quelli dell&#39;esempio A, ma con sfondo a tinta unita e possibilità di variare l&#39;altezza del composito, per adattare le immagini con proporzioni diverse.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalogo::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalogo::Modificatore</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

L&#39;immagine viene inserita nel livello 0 e il valore di altezza è `size=` è impostato su 0. Questa impostazione fa sì che l&#39;altezza effettiva sia determinata dall&#39;altezza dell&#39;immagine dopo averla ridimensionata a 800 pixel di larghezza.

La variabile `extend=` aggiunge 100 pixel in alto e in basso e 200 pixel a destra.

Le origini del livello 0 e del livello 1 vengono posizionate al centro a destra dell&#39;area di composizione per ottenere la posizione di testo desiderata.

L’immagine seguente mostra il risultato composito per diverse proporzioni dell’immagine e diverse stringhe di testo.

![Esempio B immagine](assets/exampleb.png)
