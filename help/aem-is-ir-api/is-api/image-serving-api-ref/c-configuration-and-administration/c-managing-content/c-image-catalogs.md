---
description: I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.
seo-description: I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.
seo-title: Cataloghi di immagini
solution: Experience Manager
title: Cataloghi di immagini
uuid: 7d7285e2-ee9c-4e88-b270-b686d1984d82
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 0%

---


# Cataloghi di immagini{#image-catalogs}

I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.

Mappano gli ID di contenuto immagine e statico utilizzati nelle richieste a percorsi di file effettivi, memorizzano vari metadati immagine, come le mappe immagine, e forniscono contenitori per modelli e set di immagini.

I cataloghi di immagini sono accessibili solo da Platform Server, mai da Image Server. I file di attributi del catalogo devono avere un suffisso .ini ed essere inseriti nella cartella del catalogo del server Platform ( `PS::CatalogFolder`). Almeno il catalogo immagini predefinito è obbligatorio e deve essere compilato con tutti gli attributi per il corretto funzionamento del server Platform.
