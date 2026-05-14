---
description: I cataloghi di materiale forniscono molte impostazioni di configurazione di Image Rendering.
solution: Experience Manager
title: Cataloghi di materiali
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: c0b030b7-bcfb-4e6d-b74a-4533bdb801bf
TQID: 'https://experienceleague.adobe.com/FOwuQrKYaRJ78mdRbPeoy71crT9GHj4R5MXFbMGnrZE'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 108
ht-degree: 0%

---

# Cataloghi di materiali{#material-catalogs}

I cataloghi di materiale forniscono molte impostazioni di configurazione di Image Rendering.

I cataloghi di materiali associano gli ID di vignettatura e materiale utilizzati nelle richieste ai percorsi di file effettivi, possono memorizzare tutti i metadati associati ai materiali e fornire contenitori per i modelli. Tengono traccia dei profili ICC e delle macro di comando.

I cataloghi di materiale sono accessibili solo dal componente Java di Image Rendering (che si trova in combinazione con [!DNL Platform Server]). I file degli attributi del catalogo devono avere un suffisso [!DNL .ini] e devono essere inseriti nella cartella del catalogo registrata ([ir.catalogRootPath](../../../../../../ir-api/server-admin/image-rendering-api-ref/c-ir-server-administration/c-ir-configuration-settings-reference/c-ir-catalog-folder.md#concept-1c1d308112054bb99e3895c3fb8ca5f7)). Il catalogo dei materiali predefinito ( [!DNL default.ini]) deve essere sempre presente e deve essere compilato con tutti gli attributi per il corretto funzionamento di Image Server.
