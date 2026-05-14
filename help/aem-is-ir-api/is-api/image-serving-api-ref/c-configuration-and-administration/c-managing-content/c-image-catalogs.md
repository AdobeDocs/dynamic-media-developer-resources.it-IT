---
description: I cataloghi di immagini forniscono molte impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.
solution: Experience Manager
title: Cataloghi immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
TQID: 'https://experienceleague.adobe.com/kfojwk0K5RfRtZdxJmdojqsLirnP6LoXbtFRJ5272lg'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 112
ht-degree: 0%

---

# Cataloghi immagini{#image-catalogs}

I cataloghi di immagini forniscono molte impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.

Mappano gli ID di immagini e contenuti statici utilizzati nelle richieste a percorsi di file effettivi, memorizzano vari metadati di immagini, come mappe di immagini, e forniscono contenitori per modelli e set di immagini.

I cataloghi di immagini sono accessibili solo da [!DNL Platform Server], mai dal server immagini. I file degli attributi del catalogo devono avere un suffisso .ini e devono essere inseriti nella cartella del catalogo di [!DNL Platform Server] ( `PS::CatalogFolder`). È necessario almeno il catalogo immagini predefinito e deve essere compilato con tutti gli attributi per il corretto funzionamento di [!DNL Platform Server].
