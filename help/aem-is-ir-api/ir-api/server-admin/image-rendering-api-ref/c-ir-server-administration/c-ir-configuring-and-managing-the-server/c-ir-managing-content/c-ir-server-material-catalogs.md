---
description: I cataloghi dei materiali forniscono molte impostazioni di configurazione Image Rendering .
solution: Experience Manager
title: Cataloghi dei materiali
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Cataloghi dei materiali{#material-catalogs}

I cataloghi dei materiali forniscono molte impostazioni di configurazione Image Rendering .

I cataloghi di materiali mappano vignette e ID di materiale utilizzati nelle richieste a percorsi di file effettivi, possono memorizzare tutti i metadati associati ai materiali e fornire contenitori per i modelli. Tengono traccia dei profili ICC e delle macro di comando.

I cataloghi di materiali sono accessibili solo dal componente Java di Image Rendering (co-posizionato con il [!DNL Platform Server]). I file di attributi del catalogo devono avere una [!DNL .ini] da inserire nella cartella del catalogo registrato ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Catalogo dei materiali predefinito ( [!DNL default.ini]) deve essere sempre presente e deve essere compilato con tutti gli attributi per il corretto funzionamento di Image Serving.
