---
title: Colore
description: Livello Colore. Specifica il colore di primo piano e l'opacità dei livelli a tinta unita e degli effetti, nonché il colore di riempimento delle caselle di testo per i livelli di testo.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b937e699-8e1e-4211-86a6-fdc155a0e3ed
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---

# Colore{#color}

Livello Colore. Specifica il colore di primo piano e l&#39;opacità dei livelli a tinta unita e degli effetti, nonché il colore di riempimento delle caselle di testo per i livelli di testo.

` color= *`color`*`

<table id="simpletable_68645167998A42229CEF858909FD447E"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"><span class="varname"> Colore </span> </span> </p> </td> 
  <td class="stentry"> <p>Valore di colore grigio, RGB o CMYK, con o senza alfa. </p> </td> 
 </tr> 
</table>

Se sono presenti livelli di immagine e testo, `color=` riempie le aree trasparenti e semi-opache all&#39;interno del rettangolo di delimitazione del livello con il colore specificato* prima* `rotate=` e `extend=` vengono applicate.

## Proprietà {#section-d6e74c36a49547849212e4db8927e678}

Attributo livello. Si applica al livello corrente o al livello 0 se `layer=comp`.

Si presume che il modificatore *`color`* esista nello spazio colore di lavoro corrispondente al tipo di pixel di *`color`*. E *`color`* viene convertita con precisione se l&#39;immagine del livello ha un tipo di pixel diverso al momento dell&#39;unione.

## Predefinito {#section-60611c72876b4c45b5c85ce35608e5ec}

Nessuna impostazione predefinita per i livelli a tinta unita e degli effetti; È necessario specificare un colore. Valore predefinito di 0,0,0,0 (completamente trasparente) per i livelli immagine e testo.

## Esempio {#section-2d090493f4ec4e188bbc5565aa151a05}

Nel seguente frammento di modello, lo sfondo del testo è impostato su un colore opaco del 50% e usa lo stesso colore per aggiungere un bordo semitrasparente di 10 pixel intorno all&#39;immagine del livello 2:

`…&$color=214,245,130,128& layer=1&text=my-text-string&color=$color$&… layer=2&src=myRootId/myImageId&extend=10,10,10,10&bgColor=$color$&…`

## Consultate anche {#section-f0e059f857b64b61ab4f23312b8dc619}

[color](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md#reference-0fdb264a3aed4bd78451bb55311f6e93), [bgColor=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgcolor.md#reference-441371ba4ef54fe781887c5ae448f6ab), [opac=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5), [extend=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-extend.md#reference-7e9156beb285459d830e2d56782a74ac), [bgc=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-bgc.md#reference-53376175f617446fbe5c69120f834b88), [Gestione colore](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/r-color-management.md#reference-c7e4a72d589145189f7e4bcb6b4544d7)
