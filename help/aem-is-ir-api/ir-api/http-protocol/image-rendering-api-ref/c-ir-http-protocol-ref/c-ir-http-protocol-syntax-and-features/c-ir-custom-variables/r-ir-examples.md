---
title: Esempi
description: In questo esempio viene utilizzato Image Server per colorare un oggetto e applicare una decalcomania contenente testo personalizzato in una delle serie di vignettature.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 85f11642-e1ff-4bf0-bd21-d419805cff4a
TQID: 'https://experienceleague.adobe.com/GMzKDuP-wzTrPJQbxpXc0M08BjCQdWCkGo5jOUiWipU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 137
ht-degree: 0%

---

# Esempi{#examples}

In questo esempio viene utilizzato Image Server per colorare un oggetto e applicare una decalcomania contenente testo personalizzato in una delle serie di vignettature.

Le variabili IR vengono utilizzate per identificare la vignettatura, l&#39;immagine del logo e il testo personalizzato.

Il campo `vignette::Modifier` nel record denominato *modello* nella mappa di vignettatura del catalogo dei materiali `myCat` contiene quanto segue:

`$vig=defaultVignette&$text=text_goes_here&$color=220,220,220&vignette=myCat/$vig$&obj=group/object&color=$color$&decal&src=is{?size=300,100&text={\qc\fs36 $text$}}`

Tutte le vignettature utilizzate sono elencate nella mappa di vignettatura del catalogo dei materiali `myCat`.

Il client può ora effettuare la seguente richiesta per recuperare l’immagine predefinita (utilizza le variabili definite all’inizio del modello):

[!DNL `https://server/myCat/template`]

La richiesta seguente specifica un determinato contenuto da riprodurre:

[!DNL `https://server/myCat/template?$vig=specialCup&$text=Happy%20Birthday!\line%20Pauline&$color=230,20,20`]

Per informazioni dettagliate sul comando Image Server `text=`, consultare la documentazione di Image Server.
