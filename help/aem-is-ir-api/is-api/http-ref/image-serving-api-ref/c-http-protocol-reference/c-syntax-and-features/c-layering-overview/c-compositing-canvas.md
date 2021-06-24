---
description: I livelli sono composti nell'ordine specificato dal comando layer=, dove i livelli numerati più alti nascondono quelli numerati più in basso.
solution: Experience Manager
title: Il quadro di composizione
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 2455d07f-a158-4335-a14c-213f8b3dd265
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Il quadro di composizione{#the-compositing-canvas}

I livelli sono composti nell&#39;ordine specificato dal comando layer=, dove i livelli numerati più alti nascondono quelli numerati più in basso.

Il livello 0 costituisce il livello di sfondo, che è sempre richiesto e che definisce le dimensioni dell&#39;immagine composita. Per il livello 0 è consentito qualsiasi tipo di livello. Le dimensioni del livello 0 devono essere definite, in modo esplicito utilizzando `size=` o implicitamente, in base all&#39;immagine o al testo del contenuto. Tutte le aree di altri livelli che non rientrano nell&#39;area del livello 0 non saranno incluse nell&#39;immagine di output.

>[!NOTE]
>
>Dopo che tutti i livelli sono appiattiti, l&#39;immagine composita viene convertita nell&#39;immagine di risposta finale, come specificato con i comandi e gli attributi [visualizza](../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-syntax-and-features/c-command-overview/r-view-commands-and-attributes.md#reference-8b3d637d080a47a4ba669a7f0de2ba90).
