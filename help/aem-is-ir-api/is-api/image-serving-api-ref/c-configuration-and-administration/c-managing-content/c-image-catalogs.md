---
description: I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comandi.
seo-description: I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comandi.
seo-title: Cataloghi delle immagini
solution: Experience Manager
title: Cataloghi delle immagini
topic: Scene7 Image Serving - Image Rendering API
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---


# Cataloghi di immagini{#image-catalogs}

I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comandi.

Le mappe immagine e gli ID di contenuto statici utilizzati nelle richieste per percorsi di file effettivi, memorizzano vari metadati immagine, come le mappe immagine, e forniscono contenitori per modelli e set di immagini.

I cataloghi di immagini sono accessibili solo dal server piattaforme, mai dal server immagini. I file di attributi del catalogo devono avere un suffisso .ini ed essere inseriti nella cartella del catalogo del server piattaforme ( `PS::CatalogFolder`). Almeno il catalogo di immagini predefinito è obbligatorio e deve essere popolato con tutti gli attributi per il corretto funzionamento del server piattaforma.
