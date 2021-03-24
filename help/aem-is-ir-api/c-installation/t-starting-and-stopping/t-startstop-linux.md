---
description: Ci sono due opzioni per avviare o arrestare Image Serving su Linux.
solution: Experience Manager
title: Avvio o arresto su Linux
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
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
