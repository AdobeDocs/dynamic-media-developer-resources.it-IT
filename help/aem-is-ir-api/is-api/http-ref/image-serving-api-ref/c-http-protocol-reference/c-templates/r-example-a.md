---
description: Create un modello a dimensione fissa con un’immagine di sfondo statica, un’immagine variabile allineata con lo sfondo al centro a sinistra e ridimensionata per non superare l’80% della larghezza e dell’altezza dello sfondo, e un livello di testo con testo verticale centrato sul bordo destro del quadro.
seo-description: Create un modello a dimensione fissa con un’immagine di sfondo statica, un’immagine variabile allineata con lo sfondo al centro a sinistra e ridimensionata per non superare l’80% della larghezza e dell’altezza dello sfondo, e un livello di testo con testo verticale centrato sul bordo destro del quadro.
seo-title: Esempio A
solution: Experience Manager
title: Esempio A
topic: Dynamic Media Image Serving - Image Rendering API
uuid: c250dbc8-1e32-46b8-ba55-c1fb0ae62695
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---


# Esempio A{#example-a}

Create un modello a dimensione fissa con un’immagine di sfondo statica, un’immagine variabile allineata con lo sfondo al centro a sinistra e ridimensionata per non superare l’80% della larghezza e dell’altezza dello sfondo, e un livello di testo con testo verticale centrato sul bordo destro del quadro.

![](assets/examplea.png)

## Record di modello {#section-32f54710593e438fa0622224c89380af}

Inserisci oggetto

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogo::Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogo:Modificatore  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text+go&amp;text tf..$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0  </span> </p> </td> 
 </tr> 
</table>

I valori `origin=` di tutti i livelli vengono specificati esplicitamente nel modello per controllare rigorosamente il posizionamento e l’allineamento dei livelli. Ogni origine del livello viene impostata in modo che corrisponda all’allineamento desiderato per quel livello. Il `origin=` per lo sfondo (livello 0) è impostato al centro; ciò è arbitrario perché l&#39;immagine di sfondo non viene modificata in fase di esecuzione; è possibile utilizzare qualsiasi valore per l’origine del livello 0.

I valori `pos=` forniscono gli offset necessari tra i punti di origine del livello, per ottenere il posizionamento desiderato.

L’ancoraggio dell’immagine del livello 1 viene posizionato al centro a sinistra; insieme al valore `pos=`, questo consente di ottenere l&#39;allineamento al centro a sinistra tra lo sfondo e l&#39;immagine del livello 1, indipendentemente dalle proporzioni dell&#39;immagine del livello 1.

Analogamente, l’ancoraggio per il livello di testo è posizionato al centro destro della casella di testo con ridimensionamento automatico. In combinazione con pos=, viene raggiunto l’allineamento desiderato al centro destro per il testo ruotato, indipendentemente dalla dimensione del font e dalla lunghezza della stringa.

Il testo di visualizzazione effettivo verrà fornito in fase di esecuzione, pertanto una variabile viene utilizzata per separare il testo dall&#39;involucro di formattazione rtf. Per l’immagine del livello 1 viene utilizzata la variabile predefinita `$object`. Questo consente di specificare questa immagine nel percorso della richiesta.

Qualsiasi immagine può essere utilizzata per l’immagine di sfondo e l’immagine di livello 1. Se l&#39;immagine di sfondo ha una maschera, le aree non mascherate vengono riempite con il colore di sfondo predefinito ( `attribute::BkgColor`), oppure lasciate trasparenti quando `fmt=png-alpha` o `fmt=tif-alpha`. Se l&#39;immagine di sfondo ha proporzioni non quadrate, viene centrata nell&#39;immagine di risposta e lo spazio aggiuntivo viene riempito con `attribute::BkgColor`. Se l&#39;immagine del livello 1 contiene dati alfa o una maschera, l&#39;immagine di sfondo (o il colore di sfondo) rimarrà visibile nelle aree trasparenti. Se l’immagine non ha una maschera, riempirà l’intero rettangolo allocato.

## Utilizzo del modello {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

L&#39;illustrazione seguente mostra il risultato composito per le diverse proporzioni dell&#39;immagine del livello 1 e per le diverse stringhe di testo.

![](assets/exampleausing.png)

