---
description: I cataloghi dei materiali forniscono diverse impostazioni di configurazione del rendering delle immagini.
seo-description: I cataloghi dei materiali forniscono diverse impostazioni di configurazione del rendering delle immagini.
seo-title: Cataloghi dei materiali
solution: Experience Manager
title: Cataloghi dei materiali
topic: Scene7 Image Serving - Image Rendering API
uuid: 6d209019-f9ca-43e4-900b-3597c7044a79
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 0%

---


# Cataloghi materiali{#material-catalogs}

I cataloghi dei materiali forniscono diverse impostazioni di configurazione del rendering delle immagini.

I cataloghi dei materiali mappano gli ID di vignettatura e materiale utilizzati nelle richieste ai percorsi effettivi dei file, possono memorizzare tutti i metadati associati ai materiali e fornire contenitori per i modelli. Tengono traccia dei profili ICC e delle macro dei comandi.

I cataloghi dei materiali sono accessibili solo dal componente Java di Image Rendering (in collaborazione con Platform Server). I file di attributi del catalogo devono avere un suffisso [!DNL .ini] ed essere inseriti nella cartella del catalogo registrata ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Il catalogo di materiali predefinito ( [!DNL default.ini]) deve essere sempre presente e deve essere compilato con tutti gli attributi per il corretto funzionamento del server immagini.
