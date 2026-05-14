---
title: Verifica dell'installazione
description: Dopo aver installato Image Server su Linux®, verificare l'installazione.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 273478ab-f245-48ef-a125-fb738054484e
TQID: 'https://experienceleague.adobe.com/LyHlwiFL1b-iwo1kSnUeNfNo3fZY6FZetHgnNFoxGZo'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 118
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

[!DNL  http:// *[!DNL server:port]*/ir/render]

Nelle risposte, verificare la presenza di elementi che iniziano con `imageServer`, il che indica che [!DNL Platform Server] è riuscito a comunicare con il server immagini.

>Puoi eseguire ulteriori verifiche utilizzando le pagine di esempio dei pacchetti Documentazione e Demo, se installati.
