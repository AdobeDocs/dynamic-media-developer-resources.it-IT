---
title: Verifica dell'installazione
description: Dopo aver installato Image Serving su Linux®, verifica l'installazione.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '120'
ht-degree: 0%

---

# Verifica dell&#39;installazione{#verifying-the-installation}

Dopo aver installato Image Serving su Linux®, verifica l&#39;installazione.

Image Server è installato come daemon Linux®.

**Verificare l&#39;installazione**

1. Verifica che Image Server sia configurato per l&#39;avvio automatico e che sia in esecuzione:

   `> /sbin/service ImageServing status`

   >[!NOTE]
   >
   >Per eseguire questi script è necessario disporre delle autorizzazioni radice.

1. Apri un browser Internet sullo stesso host o su un altro e controlla le risposte del server predefinito:

[!DNL http:// *[!DNL server:port]*/is/image]

[!DNL  http:// *[!DNL server:port]*/ir/render]

Nelle risposte, controlla la presenza di elementi che iniziano con `imageServer`, che indica che Platform Server è in grado di comunicare correttamente con Image Server.

>Puoi eseguire ulteriori verifiche utilizzando le pagine di esempio dei pacchetti Documentazione e Demo, se installati.
