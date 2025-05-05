---
title: Verifica dell'installazione
description: Dopo aver installato Image Server su Linux®, verificare l'installazione.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 0%

---

# Verifica dell&#39;installazione{#verifying-the-installation}

Dopo aver installato Image Server su Linux®, verificare l&#39;installazione.

Il server immagini è installato come daemon Linux®.

**Per verificare l&#39;installazione**

1. Verifica che Image Server sia configurato per l&#39;avvio automatico e che sia in esecuzione:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Per eseguire questi script è necessario disporre delle autorizzazioni radice.

1. Aprire un browser Internet sullo stesso host o su un host diverso e verificare le risposte predefinite del server:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL &#x200B; http:// *[!DNL server:port]*/ir/render]

Nelle risposte, verificare la presenza di elementi che iniziano con `imageServer`, il che indica che [!DNL Platform Server] è riuscito a comunicare con il server immagini.

>Puoi eseguire ulteriori verifiche utilizzando le pagine di esempio dei pacchetti Documentazione e Demo, se installati.
