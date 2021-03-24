---
description: Ci sono due opzioni per avviare o arrestare Image Serving su Linux.
solution: Experience Manager
title: Avvio o arresto su Linux
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '67'
ht-degree: 0%

---


# Avvio o arresto su Linux{#starting-or-stopping-on-linux}

Ci sono due opzioni per avviare o arrestare Image Serving su Linux.

* Lo script per avviare, interrompere e verificare lo stato di Image Server si trova nella cartella [!DNL ImageServing/bin] :

   `ImageServing.sh {start|stop|restart|status}`
* L’alternativa seguente dovrebbe essere familiare agli amministratori di sistema:

   `/sbin/service ImageServing {start|stop|status}`
