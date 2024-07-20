---
description: I cataloghi di materiale forniscono molte impostazioni di configurazione di Image Rendering.
solution: Experience Manager
title: Cataloghi di materiali
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '107'
ht-degree: 0%

---

# Cataloghi di materiali{#material-catalogs}

I cataloghi di materiale forniscono molte impostazioni di configurazione di Image Rendering.

I cataloghi di materiali associano gli ID di vignettatura e materiale utilizzati nelle richieste ai percorsi di file effettivi, possono memorizzare tutti i metadati associati ai materiali e fornire contenitori per i modelli. Tengono traccia dei profili ICC e delle macro di comando.

I cataloghi di materiale sono accessibili solo dal componente Java di Image Rendering (che si trova in combinazione con [!DNL Platform Server]). I file degli attributi del catalogo devono avere un suffisso [!DNL .ini] e devono essere inseriti nella cartella del catalogo registrata ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Il catalogo dei materiali predefinito ( [!DNL default.ini]) deve essere sempre presente e deve essere compilato con tutti gli attributi per il corretto funzionamento di Image Server.
