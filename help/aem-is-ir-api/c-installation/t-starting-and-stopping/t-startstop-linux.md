---
description: Ci sono due opzioni per avviare o arrestare Image Serving su Linux.
solution: Experience Manager
title: Avvio o arresto su Linux
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '64'
ht-degree: 0%

---

# Avvio o arresto su Linux{#starting-or-stopping-on-linux}

Ci sono due opzioni per avviare o arrestare Image Serving su Linux.

* Lo script per avviare, interrompere e verificare lo stato di Image Server si trova nella cartella [!DNL ImageServing/bin] :

   `ImageServing.sh {start|stop|restart|status}`
* L’alternativa seguente dovrebbe essere familiare agli amministratori di sistema:

   `/sbin/service ImageServing {start|stop|status}`
