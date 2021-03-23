---
description: Ci sono due opzioni per avviare o arrestare Image Serving su Linux.
seo-description: Ci sono due opzioni per avviare o arrestare Image Serving su Linux.
seo-title: Avvio o arresto su Linux
solution: Experience Manager
title: Avvio o arresto su Linux
uuid: 92cf60c4-3f80-42bc-b135-17bc22ba151e
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 0%

---


# Avvio o arresto su Linux{#starting-or-stopping-on-linux}

Ci sono due opzioni per avviare o arrestare Image Serving su Linux.

* Lo script per avviare, interrompere e verificare lo stato di Image Server si trova nella cartella [!DNL ImageServing/bin] :

   `ImageServing.sh {start|stop|restart|status}`
* L’alternativa seguente dovrebbe essere familiare agli amministratori di sistema:

   `/sbin/service ImageServing {start|stop|status}`
