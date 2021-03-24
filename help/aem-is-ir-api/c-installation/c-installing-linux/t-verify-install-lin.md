---
description: Dopo aver installato Image Serving su Linux, verifica l'installazione.
solution: Experience Manager
title: Verifica dell'installazione
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---


# Verifica dell&#39;installazione{#verifying-the-installation}

Dopo aver installato Image Serving su Linux, verifica l&#39;installazione.

Image Server è installato come daemon Linux.

**Verificare l&#39;installazione**

1. Verifica che Image Server sia configurato per l&#39;avvio automatico e che sia in esecuzione:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Per eseguire questi script è necessario disporre delle autorizzazioni radice.

1. Apri un browser Internet sullo stesso host o su un altro e controlla le risposte del server predefinite:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL http:// *[!DNL server:port]*/ir/render]

Nelle risposte, verifica la presenza di elementi che iniziano con &quot; `imageServer.`&quot;, il che indica che Platform Server è in grado di comunicare con successo con il server immagini.
>Puoi eseguire ulteriori verifiche utilizzando le pagine di esempio dei pacchetti Documentazione e Demo, se installati.

