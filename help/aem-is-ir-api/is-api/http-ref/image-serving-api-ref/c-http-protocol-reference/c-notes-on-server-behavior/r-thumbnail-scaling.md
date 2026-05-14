---
title: Ridimensionamento miniature
description: Il passaggio 2 del livello immagine viene modificato come segue per le miniature (ovvero, se req=tmb).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 08290258-4fc8-4a6a-ba8f-6bdcd969fa3c
TQID: 'https://experienceleague.adobe.com/He10BtjrEIOQW6SZcaUhcExDjP05BR-pc3BCj9TRawU'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 79
ht-degree: 0%

---

# Ridimensionamento miniature{#thumbnail-scaling}

Il passaggio 2 del livello immagine viene modificato come segue per le miniature (ovvero, se req=tmb).

* `2.` Se si specifica `size=`, adattare l&#39;immagine (ritagliata) al retto `size=` utilizzando le regole per le miniature. Se `size=` non è specificato, ridimensionare in base a `res=` oppure, se `res=` non è specificato, adattare l&#39;immagine (ritagliata) all&#39;area di lavoro utilizzando le regole di miniatura descritte di seguito.
