---
title: Avvio o arresto su Linux®
description: Sono disponibili due opzioni per avviare o arrestare Image Server su Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: eb4c60b2-5491-40e9-b105-d4b05006a9ca
TQID: 'https://experienceleague.adobe.com/i3Ai03O29-qmhMpCRNl7MZkqXjRDnQT1M2sVX-Z3eho'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 64
ht-degree: 0%

---

# Avvio o arresto su Linux® {#starting-or-stopping-on-linux}

Sono disponibili due opzioni per avviare o arrestare Image Server su Linux®.

* Lo script per verificare lo stato di Image Server o per avviare e arrestare Image Server si trova nella cartella [!DNL ImageServing/bin]:

  `ImageServing.sh {start|stop|restart|status}`
* La seguente alternativa deve essere nota agli amministratori di sistema:

  `/sbin/service ImageServing {start|stop|status}`
