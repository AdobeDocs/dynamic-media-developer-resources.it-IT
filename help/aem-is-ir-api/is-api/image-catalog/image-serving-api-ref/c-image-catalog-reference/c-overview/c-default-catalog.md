---
description: Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di immagini.
seo-description: Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di immagini.
seo-title: Catalogo predefinito
solution: Experience Manager
title: Catalogo predefinito
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f0c967e-a2fa-4ef0-bacb-3dcfb06a8027
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---


# Catalogo predefinito{#default-catalog}

Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di immagini.

Se non è possibile trovare un attributo specifico in un catalogo di immagini specifico, il server utilizza invece il valore corrispondente dal catalogo predefinito. Analogamente, il catalogo predefinito può essere utilizzato per fornire impostazioni predefinite per record di dati del catalogo specifici (immagini, definizioni di macro, font e profili ICC). Se non è possibile trovare un record di dati specifico in un catalogo di immagini specifico, il server tenta di trovarlo nel catalogo predefinito. Questo consente di compilare i cataloghi di immagini in modo sparso e semplifica la gestione di attributi e dati globali, come modelli condivisi, macro, font ecc.

Inoltre, il catalogo predefinito fornisce tutti gli attributi e i record di dati (macro, font, profili ICC, regole di pre-elaborazione richieste) quando non è coinvolto in un&#39;operazione alcun catalogo di immagini specifico.

Per il corretto funzionamento del server piattaforme, il file degli attributi del catalogo per il catalogo predefinito deve essere denominato [!DNL default.ini], deve sempre esistere nella cartella del catalogo e deve essere compilato con tutti gli attributi richiesti, ad eccezione di `attribute::RootId` e i riferimenti ai vari file di dati del catalogo, tutti facoltativi.

>[!NOTE]
>
>Tutti i file di attributi del catalogo tranne [!DNL default.ini] devono contenere un valore `attribute::RootId` univoco. `attribute::RootId` deve  [!DNL default.ini] essere vuoto.

