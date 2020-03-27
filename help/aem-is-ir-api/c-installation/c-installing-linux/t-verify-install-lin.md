---
description: Dopo aver installato Image Server su Linux, verificate l'installazione.
seo-description: Dopo aver installato Image Server su Linux, verificate l'installazione.
seo-title: Verifica dell’installazione
solution: Experience Manager
title: Verifica dell’installazione
topic: Scene7 Image Serving - Image Rendering API
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Verifica dell’installazione{#verifying-the-installation}

Dopo aver installato Image Server su Linux, verificate l&#39;installazione.

Image Server è installato come demone Linux.

**Per verificare l&#39;installazione**

1. Verificate che Image Server sia configurato per l’avvio automatico e che sia in esecuzione:

   `> /sbin/service ImageServing status`

   >[!NOTE] {class=&quot;- topic/note &quot;}
   >
   >Per eseguire questi script è necessario disporre delle autorizzazioni di livello principale.

1. Aprite un browser Internet sullo stesso host o su un altro host e verificate le risposte server predefinite:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/rendering]

Nelle risposte, verificate la presenza di elementi che iniziano con &quot; `imageServer.`&quot;, il che indica che il server piattaforme può comunicare con il server immagini.
>È possibile eseguire ulteriori verifiche utilizzando le pagine di esempio dei pacchetti Documentazione e Demo, se installati.

