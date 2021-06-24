---
description: I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.
solution: Experience Manager
title: Cataloghi di immagini
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 70ec4566-a937-464e-8219-b7eda3ab66c1
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 0%

---

# Cataloghi di immagini{#image-catalogs}

I cataloghi di immagini forniscono numerose impostazioni di configurazione del server, nonché font, profili ICC e macro di comando.

Mappano gli ID di contenuto immagine e statico utilizzati nelle richieste a percorsi di file effettivi, memorizzano vari metadati immagine, come le mappe immagine, e forniscono contenitori per modelli e set di immagini.

I cataloghi di immagini sono accessibili solo da Platform Server, mai da Image Server. I file di attributi del catalogo devono avere un suffisso .ini ed essere inseriti nella cartella del catalogo del server Platform ( `PS::CatalogFolder`). Almeno il catalogo immagini predefinito è obbligatorio e deve essere compilato con tutti gli attributi per il corretto funzionamento del server Platform.
