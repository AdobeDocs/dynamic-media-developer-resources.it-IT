---
description: Dopo aver installato Scene7 Image Server, è necessario verificare l’installazione.
seo-description: Dopo aver installato Scene7 Image Server, è necessario verificare l’installazione.
seo-title: Verifica dell’installazione
solution: Experience Manager
title: Verifica dell’installazione
topic: Scene7 Image Serving - Image Rendering API
uuid: ccc7688d-3d7f-4066-a19e-8a36ca56d711
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 0%

---


# Verifica dell&#39;installazione{#verifying-the-installation}

Dopo aver installato Scene7 Image Server, è necessario verificare l’installazione.

Image Server è installato come servizio Windows.

1. Aprite il Pannello di controllo Campaign Servizi e verificate che &quot;Scene7 Image Serving&quot; sia presente con lo stato &quot;Started&quot;.
1. Aprite un browser Internet sullo stesso host o su un altro host e verificate le risposte predefinite del server:

   `http:// server:port /is/image`

[!DNL http:// *[!DNL server:port]*/ir/rendering]

Verificate la presenza di &quot; `imageServer.`&quot; elementi nella risposta, a indicare che il server immagini è in ascolto.
>È possibile eseguire ulteriori verifiche utilizzando le pagine di esempio dei pacchetti Documentazione e Demo, se installati.

