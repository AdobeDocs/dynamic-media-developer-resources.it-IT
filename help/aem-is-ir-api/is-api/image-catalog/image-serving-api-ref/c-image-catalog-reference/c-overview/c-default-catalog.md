---
description: Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di immagini.
solution: Experience Manager
title: Catalogo predefinito
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---

# Catalogo predefinito{#default-catalog}

Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di immagini.

Se non è possibile trovare un particolare attributo in un catalogo di immagini specifico, il server utilizza il valore corrispondente del catalogo predefinito. Analogamente, il catalogo predefinito può essere utilizzato per fornire impostazioni predefinite per record di dati di catalogo specifici (immagini, definizioni di macro, font e profili ICC). Se non è possibile trovare un particolare record di dati in un catalogo di immagini specifico, il server tenta di trovarlo nel catalogo predefinito. Ciò consente ai cataloghi di immagini di essere scarsamente popolati e semplifica la gestione di attributi e dati globali, come modelli condivisi, macro, font e così via.

Inoltre, il catalogo predefinito fornisce tutti gli attributi e i record di dati (macro, font, profili ICC richiesta regole di pre-elaborazione) quando nessun catalogo di immagini specifico è coinvolto in un&#39;operazione.

Per il corretto funzionamento del [!DNL Platform Server] file degli attributi del catalogo per il catalogo predefinito deve essere denominato [!DNL default.ini], deve sempre esistere nella cartella del catalogo, e deve essere completamente popolato con tutti gli attributi richiesti, esclusi `attribute::RootId` e i riferimenti ai vari file di dati del catalogo, che sono tutti facoltativi.

>[!NOTE]
>
>Tutti i file di attributi del catalogo, ad eccezione di [!DNL default.ini] quelli devono contenere un valore univoco `attribute::RootId` . `attribute::RootId` in [!DNL default.ini] deve essere vuoto.
