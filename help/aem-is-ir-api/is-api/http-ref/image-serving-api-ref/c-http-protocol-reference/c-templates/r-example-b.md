---
description: Requisiti simili all’esempio A, ma con uno sfondo a colori in tinta unita e l’altezza del composito può variare per contenere immagini con proporzioni diverse.
seo-description: Requisiti simili all’esempio A, ma con uno sfondo a colori in tinta unita e l’altezza del composito può variare per contenere immagini con proporzioni diverse.
seo-title: Esempio B
solution: Experience Manager
title: Esempio B
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 13120562-9201-4733-bd9d-4a54eac913e9
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# Esempio B{#example-b}

Requisiti simili all’esempio A, ma con uno sfondo a colori in tinta unita e l’altezza del composito può variare per contenere immagini con proporzioni diverse.

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> catalogo::Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> catalogo:Modificatore</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+go+here&amp; layer=0&amp;size=800,0&amp;extension=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp; layer=1&amp;text=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;originD=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

L’immagine viene inserita nel livello 0 e il valore di altezza di `size=` è impostato su 0, il che determina l’altezza effettiva in base all’altezza dell’immagine dopo averla ridimensionata a 800 pixel di larghezza.

`extend=` aggiunge 100 pixel in alto e in basso e 200 pixel a destra.

Le origini dei livelli 0 e 1 vengono posizionate al centro a destra dell’area di composizione, in modo da ottenere la posizione desiderata.

L&#39;illustrazione seguente mostra il risultato composito per le diverse proporzioni dell&#39;immagine e per diverse stringhe di testo.

![](assets/exampleb.png)

