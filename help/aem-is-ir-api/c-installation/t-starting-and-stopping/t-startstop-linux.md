---
title: Avvio o arresto su Linux®
description: Sono disponibili due opzioni per avviare o arrestare Image Server su Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Avvio o arresto su Linux® {#starting-or-stopping-on-linux}

Sono disponibili due opzioni per avviare o arrestare Image Server su Linux®.

* Lo script per verificare lo stato di Image Server o per avviare e arrestare Image Server si trova in [!DNL ImageServing/bin] cartella:

   `ImageServing.sh {start|stop|restart|status}`
* La seguente alternativa deve essere nota agli amministratori di sistema:

   `/sbin/service ImageServing {start|stop|status}`
