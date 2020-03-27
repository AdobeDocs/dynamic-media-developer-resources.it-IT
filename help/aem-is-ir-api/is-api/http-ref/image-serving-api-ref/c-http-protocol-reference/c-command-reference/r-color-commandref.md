---
description: Colore livello. Specifica il colore di primo piano e l’opacità dei livelli di colore e effetto in tinta unita e il colore di riempimento della casella di testo per i livelli di testo.
seo-description: Colore livello. Specifica il colore di primo piano e l’opacità dei livelli di colore e effetto in tinta unita e il colore di riempimento della casella di testo per i livelli di testo.
seo-title: color
solution: Experience Manager
title: color
topic: Scene7 Image Serving - Image Rendering API
uuid: 46b93609-02c0-47bf-97c0-e7b2e416d292
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# color{#color}

Colore livello. Specifica il colore di primo piano e l’opacità dei livelli di colore e effetto in tinta unita e il colore di riempimento della casella di testo per i livelli di testo.

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> colore </span></span> </p> </td> 
  <td class="stentry"> <p>Valore colore grigio, RGB o CMYK, con o senza alfa. </p> </td> 
 </tr> 
</table>

Nel caso di livelli di immagine e testo, `color=` riempie le aree trasparenti e semi-opache all’interno del rettangolo di selezione del livello con il colore specificato* prima* `rotate=` e `extend=` vengono applicate.

## Proprietà {#section-d6e74c36a49547849212e4db8927e678}

Attributo layer. Si applica al livello corrente o al livello 0, se `layer=comp`.

*`color`* si presume che esista nello spazio colore di lavoro corrispondente al tipo di pixel di *`color`*. *`color`* viene convertita accuratamente se l’immagine del livello ha un diverso tipo di pixel al momento dell’unione.

## Predefinito {#section-60611c72876b4c45b5c85ce35608e5ec}

Nessun valore predefinito per i livelli di colore e effetto in tinta unita; è necessario specificare un colore. Il valore predefinito è 0,0,0,0 (completamente trasparente) per i livelli di immagine e testo.

## Esempio {#section-2d090493f4ec4e188bbc5565aa151a05}

Nel seguente frammento di modello imposta lo sfondo del testo su un colore opaco del 50% e utilizza lo stesso colore per aggiungere un bordo semi-trasparente di 10 pixel attorno all’immagine del livello 2:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Consultate anche {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [span=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), Gestione [del colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
