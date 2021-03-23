---
description: Dopo aver installato Image Serving su Linux, verifica l'installazione.
seo-description: Dopo aver installato Image Serving su Linux, verifica l'installazione.
seo-title: Verifica dell'installazione
solution: Experience Manager
title: Verifica dell'installazione
uuid: 4fdf61c7-3c9f-4f3e-9696-60eb7e3f2209
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '150'
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

