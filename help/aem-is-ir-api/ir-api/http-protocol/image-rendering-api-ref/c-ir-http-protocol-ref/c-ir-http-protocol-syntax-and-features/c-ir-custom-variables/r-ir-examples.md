---
title: Esempi
description: In questo esempio viene utilizzato Image Server per colorare un oggetto e applicare una decalcomania contenente testo personalizzato in una delle serie di vignettature.
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

In questo esempio viene utilizzato Image Server per colorare un oggetto e applicare una decalcomania contenente testo personalizzato in una delle serie di vignettature.

Le variabili IR vengono utilizzate per identificare la vignettatura, l&#39;immagine del logo e il testo personalizzato.

Il `vignette::Modifier` campo nel record denominato *modello* nella mappa di vignettatura del catalogo dei materiali `myCat` contiene quanto segue:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Tutte le vignettature usate sono elencate nella mappa di vignettatura del catalogo dei materiali `myCat`.

Il client può ora effettuare la seguente richiesta per recuperare l’immagine predefinita (utilizza le variabili definite all’inizio del modello):

[!DNL `https://server/myCat/template`]

La richiesta seguente specifica un determinato contenuto da riprodurre:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Per informazioni dettagliate su Image Server, consulta Documentazione di Image Server `text=` comando.
