---
description: In questo esempio viene utilizzato Image Serving per colorare un oggetto e applicare una decal contenente testo personalizzato in uno di un set di vignette.
solution: Experience Manager
title: Esempi
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 0%

---


# Esempi{#examples}

In questo esempio viene utilizzato Image Serving per colorare un oggetto e applicare una decal contenente testo personalizzato in uno di un set di vignette.

Le variabili IR vengono utilizzate per identificare la vignetta, l’immagine del logo e il testo personalizzato.

Il campo `vignette::Modifier` nel record denominato *template* nella mappa della vignetta del catalogo dei materiali `myCat` contiene quanto segue:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Tutte le vignette che verranno utilizzate sono elencate nella mappa della vignetta del catalogo dei materiali `myCat`.

Il client ora può effettuare la seguente richiesta per recuperare l’immagine predefinita (utilizzando le variabili definite all’inizio del modello):

[!DNL `https://server/myCat/template`]

La richiesta seguente specifica alcuni contenuti da riprodurre:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Per informazioni dettagliate sul comando Image Serving `text=` , consulta la documentazione Image Serving .
