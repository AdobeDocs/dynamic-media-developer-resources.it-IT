---
description: In questo esempio viene utilizzato Image Server per colorare un oggetto e applicare un decal contenente testo personalizzato in una delle serie di vignettature.
seo-description: In questo esempio viene utilizzato Image Server per colorare un oggetto e applicare un decal contenente testo personalizzato in una delle serie di vignettature.
seo-title: Esempi
solution: Experience Manager
title: Esempi
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
translation-type: tm+mt
source-git-commit: b27327f940202b1883a654702aa386c7ae83c856

---


# Esempi{#examples}

In questo esempio viene utilizzato Image Server per colorare un oggetto e applicare un decal contenente testo personalizzato in una delle serie di vignettature.

Le variabili IR vengono utilizzate per identificare la vignettatura, l’immagine del logo e il testo personalizzato.

Il `vignette::Modifier` campo nel record denominato *template* nella mappa di vignettatura del catalogo dei materiali `myCat` contiene quanto segue:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Tutte le vignettature che verranno utilizzate sono elencate nella mappa di vignettatura del catalogo dei materiali `myCat`.

Ora il client può effettuare la seguente richiesta per recuperare l’immagine predefinita (utilizzando le variabili definite all’inizio del modello):

[!DNL `https://server/myCat/template`]

La richiesta seguente specifica alcuni contenuti da sottoporre a rendering:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Per informazioni sul `text=` comando Image Server, consultate la documentazione di Image Server.
