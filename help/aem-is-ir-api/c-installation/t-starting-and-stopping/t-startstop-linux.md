---
description: Ci sono due opzioni per avviare o arrestare Image Serving su Linux.
solution: Experience Manager
title: Avvio o arresto su Linux
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
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
