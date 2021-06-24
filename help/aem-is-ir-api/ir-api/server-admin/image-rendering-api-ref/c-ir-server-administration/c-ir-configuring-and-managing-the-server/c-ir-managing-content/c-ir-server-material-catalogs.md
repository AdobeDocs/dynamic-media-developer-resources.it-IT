---
description: I cataloghi dei materiali forniscono molte impostazioni di configurazione Image Rendering .
solution: Experience Manager
title: Cataloghi dei materiali
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# Cataloghi dei materiali{#material-catalogs}

I cataloghi dei materiali forniscono molte impostazioni di configurazione Image Rendering .

I cataloghi di materiali mappano vignette e ID di materiale utilizzati nelle richieste a percorsi di file effettivi, possono memorizzare tutti i metadati associati ai materiali e fornire contenitori per i modelli. Tengono traccia dei profili ICC e delle macro di comando.

I cataloghi di materiali sono accessibili solo dal componente Java di Image Rendering (co-posizionato con Platform Server). I file di attributi del catalogo devono avere un suffisso [!DNL .ini] ed essere inseriti nella cartella del catalogo registrata ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Il catalogo dei materiali predefinito ( [!DNL default.ini]) deve essere sempre presente e deve essere compilato con tutti gli attributi per il corretto funzionamento di Image Server.
