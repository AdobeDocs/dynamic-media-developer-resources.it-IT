---
description: In questo esempio viene utilizzato Image Server per colorare un oggetto e applicare un decal contenente testo personalizzato in una delle serie di vignettature.
seo-description: In questo esempio viene utilizzato Image Server per colorare un oggetto e applicare un decal contenente testo personalizzato in una delle serie di vignettature.
seo-title: Esempi
solution: Experience Manager
title: Esempi
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 9f8e4346-6efe-4f21-982d-613328bd708d
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 0%

---


# Esempi{#examples}

In questo esempio viene utilizzato Image Server per colorare un oggetto e applicare un decal contenente testo personalizzato in una delle serie di vignettature.

Le variabili IR vengono utilizzate per identificare la vignettatura, l’immagine del logo e il testo personalizzato.

Il campo `vignette::Modifier` nel record denominato *template* nella mappa di vignettatura del catalogo materiali `myCat` contiene quanto segue:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Tutte le vignettature che verranno utilizzate sono elencate nella mappa di vignettatura del catalogo materiali `myCat`.

Ora il client può effettuare la seguente richiesta per recuperare l’immagine predefinita (utilizzando le variabili definite all’inizio del modello):

[!DNL `https://server/myCat/template`]

La richiesta seguente specifica alcuni contenuti da sottoporre a rendering:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Per informazioni sul comando Image Server `text=`, consultate la documentazione di Image Server.
