---
title: Esempi
description: In questo esempio viene utilizzato Image Serving per colorare un oggetto e applicare una decal contenente testo personalizzato in uno di un set di vignette.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---

# Esempi{#examples}

In questo esempio viene utilizzato Image Serving per colorare un oggetto e applicare una decal contenente testo personalizzato in uno di un set di vignette.

Le variabili IR vengono utilizzate per identificare la vignetta, l’immagine del logo e il testo personalizzato.

La `vignette::Modifier` nel record denominato *template* nella mappa della vignetta del catalogo dei materiali `myCat` contiene quanto segue:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Tutte le vignette usate sono elencate nella mappa della vignetta del catalogo del materiale `myCat`.

Il client ora può effettuare la seguente richiesta per recuperare l’immagine predefinita (utilizza le variabili definite all’inizio del modello):

[!DNL `https://server/myCat/template`]

La richiesta seguente specifica alcuni contenuti da riprodurre:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Per informazioni dettagliate su Image Serving, consulta la documentazione di Image Serving `text=` comando.
