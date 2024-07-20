---
description: I cataloghi di immagini forniscono molte impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.
solution: Experience Manager
title: Cataloghi immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Cataloghi immagini{#image-catalogs}

I cataloghi di immagini forniscono molte impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.

Mappano gli ID di immagini e contenuti statici utilizzati nelle richieste a percorsi di file effettivi, memorizzano vari metadati di immagini, come mappe di immagini, e forniscono contenitori per modelli e set di immagini.

I cataloghi di immagini sono accessibili solo da [!DNL Platform Server], mai dal server immagini. I file degli attributi del catalogo devono avere un suffisso .ini e devono essere inseriti nella cartella del catalogo di [!DNL Platform Server] ( `PS::CatalogFolder`). È necessario almeno il catalogo immagini predefinito e deve essere compilato con tutti gli attributi per il corretto funzionamento di [!DNL Platform Server].
