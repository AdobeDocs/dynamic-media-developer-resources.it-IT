---
description: I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.
solution: Experience Manager
title: Cataloghi di immagini
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, amministratore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---


# Cataloghi di immagini{#image-catalogs}

I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.

Mappano gli ID di contenuto immagine e statico utilizzati nelle richieste a percorsi di file effettivi, memorizzano vari metadati immagine, come le mappe immagine, e forniscono contenitori per modelli e set di immagini.

I cataloghi di immagini sono accessibili solo da Platform Server, mai da Image Server. I file di attributi del catalogo devono avere un suffisso .ini ed essere inseriti nella cartella del catalogo del server Platform ( `PS::CatalogFolder`). Almeno il catalogo immagini predefinito è obbligatorio e deve essere compilato con tutti gli attributi per il corretto funzionamento del server Platform.
