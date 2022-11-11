---
description: I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.
solution: Experience Manager
title: Cataloghi di immagini
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '112'
ht-degree: 0%

---

# Cataloghi di immagini{#image-catalogs}

I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.

Mappano gli ID di contenuto immagine e statico utilizzati nelle richieste a percorsi di file effettivi, memorizzano vari metadati immagine, come le mappe immagine, e forniscono contenitori per modelli e set di immagini.

I cataloghi di immagini sono accessibili solo dal [!DNL Platform Server], mai dal server di immagini. I file di attributi del catalogo devono avere un suffisso .ini ed essere inseriti nel [!DNL Platform Server]Cartella catalogo di ( `PS::CatalogFolder`). Almeno il catalogo immagini predefinito è obbligatorio e deve essere compilato con tutti gli attributi per il corretto funzionamento del [!DNL Platform Server].
