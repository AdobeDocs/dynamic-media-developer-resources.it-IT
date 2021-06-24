---
description: Crea un modello a dimensione fissa con un’immagine di sfondo statica, un’immagine variabile allineata con lo sfondo al centro a sinistra e ridimensionata per non superare l’80% della larghezza e dell’altezza dello sfondo e un livello di testo con testo verticale centrato sul bordo destro dell’area di lavoro.
solution: Experience Manager
title: Esempio A
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# Esempio A{#example-a}

Crea un modello a dimensione fissa con un’immagine di sfondo statica, un’immagine variabile allineata con lo sfondo al centro a sinistra e ridimensionata per non superare l’80% della larghezza e dell’altezza dello sfondo e un livello di testo con testo verticale centrato sul bordo destro dell’area di lavoro.

![](assets/examplea.png)

## Record del modello {#section-32f54710593e438fa0622224c89380af}

Inserisci oggetto

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogo::Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> catalogo::Modificatore  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp; layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp; layer=2&amp;$text=layer+2+text+go&amp;text=text tf..$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0  </span> </p> </td> 
 </tr> 
</table>

I valori `origin=` di tutti i livelli sono specificati esplicitamente nel modello per controllare rigorosamente il posizionamento e l&#39;allineamento dei livelli. Ogni origine del livello viene impostata in modo che corrisponda all&#39;allineamento desiderato per quel livello. Il `origin=` per lo sfondo (livello 0) è impostato sul centro; ciò è arbitrario perché l&#39;immagine di sfondo non cambierà in fase di esecuzione; è possibile utilizzare qualsiasi valore per l&#39;origine del livello 0.

I valori `pos=` forniscono gli offset necessari tra i punti di origine del livello per ottenere il posizionamento desiderato.

L&#39;ancoraggio dell&#39;immagine di livello 1 viene posizionato al centro a sinistra; insieme al valore `pos=`, questo consente di ottenere l&#39;allineamento al centro a sinistra tra lo sfondo e l&#39;immagine di livello 1, indipendentemente dalle proporzioni dell&#39;immagine di livello 1.

Analogamente, l’ancoraggio per il livello di testo è posizionato al centro destro della casella di testo con ridimensionamento automatico. Insieme a pos= questo consente di ottenere l’allineamento al centro destro desiderato per il testo ruotato, indipendentemente dalle dimensioni del font e dalla lunghezza della stringa.

Il testo da visualizzare effettivo verrà fornito in fase di esecuzione, in modo che venga utilizzata una variabile per separare il testo dall’involucro di formattazione rtf. Usiamo la variabile predefinita `$object` per l&#39;immagine di livello 1. Questo consente di specificare questa immagine nel percorso della richiesta.

Qualsiasi immagine può essere utilizzata per l&#39;immagine di sfondo e l&#39;immagine di livello 1. Se l&#39;immagine di sfondo ha una maschera, le aree non mascherate vengono riempite con il colore di sfondo predefinito ( `attribute::BkgColor`) o lasciate trasparenti quando `fmt=png-alpha` o `fmt=tif-alpha`. Se l&#39;immagine di sfondo ha proporzioni non quadrate, viene centrata nell&#39;immagine di risposta e lo spazio aggiuntivo viene riempito con `attribute::BkgColor`. Se l&#39;immagine di livello 1 ha dati alfa o una maschera, l&#39;immagine di sfondo (o colore di sfondo) rimarrà visibile nelle aree trasparenti. Se l&#39;immagine non ha una maschera, riempirà l&#39;intero rettangolo allocato.

## Utilizzo del modello {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`server`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

L&#39;illustrazione seguente mostra il risultato composito per le diverse proporzioni dell&#39;immagine di livello 1 e diverse stringhe di testo.

![](assets/exampleausing.png)
