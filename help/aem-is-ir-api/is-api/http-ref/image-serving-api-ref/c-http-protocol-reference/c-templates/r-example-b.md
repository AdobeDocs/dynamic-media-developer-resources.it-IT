---
description: Requisiti simili all'esempio A, ma utilizzare uno sfondo a colori solidi e consentire la variazione dell'altezza del composito per adattarsi alle immagini con proporzioni diverse.
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

Requisiti simili all&#39;esempio A, ma utilizzare uno sfondo a colori solidi e consentire la variazione dell&#39;altezza del composito per adattarsi alle immagini con proporzioni diverse.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalogo::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalogo::Modificatore</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;extension=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf..$text$..rtf-encoding&amp;rotate=-90&amp;originorigin=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

L&#39;immagine viene inserita nel livello 0 e il valore di altezza di `size=` è impostato su 0. Questa impostazione determina l’altezza effettiva in base all’altezza dell’immagine dopo averla ridimensionata a 800 pixel di larghezza.

La variabile `extend=` aggiunge 100 pixel all’inizio e alla fine e 200 pixel a destra.

Le origini del livello 0 e del livello 1 vengono posizionate al centro a destra dell&#39;area di composizione, in modo da ottenere la posizione del testo desiderata.

L&#39;immagine seguente mostra il risultato composito per diverse proporzioni dell&#39;immagine e diverse stringhe di testo.

![Immagine B di esempio](assets/exampleb.png)
