---
description: Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di immagini.
solution: Experience Manager
title: Catalogo predefinito
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 0%

---

# Catalogo predefinito{#default-catalog}

Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di immagini.

Se non è possibile trovare un attributo specifico in un catalogo di immagini specifico, il server utilizza invece il valore corrispondente del catalogo predefinito. Analogamente, il catalogo predefinito può essere utilizzato per fornire impostazioni predefinite per record di dati di catalogo specifici (immagini, definizioni di macro, font e profili ICC). Se non è possibile trovare un record di dati specifico in un catalogo di immagini specifico, il server tenta di trovarlo nel catalogo predefinito. Questo consente di popolare i cataloghi di immagini e semplifica la gestione di attributi e dati globali, come modelli condivisi, macro, font, ecc.

Inoltre, il catalogo predefinito fornisce tutti gli attributi e i record di dati (macro, font, profili ICC, richieste di regole di pre-elaborazione) quando non è coinvolto in un’operazione un catalogo di immagini specifico.

Per il corretto funzionamento del [!DNL Platform Server] il file degli attributi del catalogo per il catalogo predefinito deve essere denominato [!DNL default.ini], deve esistere sempre nella cartella del catalogo e deve essere compilato completamente con tutti gli attributi richiesti, escludendo `attribute::RootId` e i riferimenti ai vari file di dati del catalogo, tutti facoltativi.

>[!NOTE]
>
>Tutti i file di attributi del catalogo tranne [!DNL default.ini] deve contenere un `attribute::RootId` valore. `attribute::RootId` in [!DNL default.ini] deve essere vuoto.
