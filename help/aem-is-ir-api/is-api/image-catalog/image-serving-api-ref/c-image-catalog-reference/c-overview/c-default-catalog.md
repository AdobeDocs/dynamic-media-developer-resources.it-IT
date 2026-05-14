---
description: Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di immagini.
solution: Experience Manager
title: Catalogo predefinito
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: db42fb67-aa6f-4217-bc69-45b01bbd0b10
TQID: 'https://experienceleague.adobe.com/qbfEwBJ-eQmCbBR0MJQhP7x3ZEd30nfLJHWjBVoXIjc'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 215
ht-degree: 0%

---

# Catalogo predefinito{#default-catalog}

Il catalogo predefinito fornisce valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di immagini.

Se non è possibile trovare un attributo specifico in un catalogo immagini specifico, il server utilizza il valore corrispondente del catalogo predefinito. Analogamente, il catalogo predefinito può essere utilizzato per fornire valori predefiniti per record di dati di catalogo specifici (immagini, definizioni di macro, font e profili ICC). Se non è possibile trovare un record di dati specifico in un catalogo immagini specifico, il server tenta di trovarlo nel catalogo predefinito. Questo consente di popolare i cataloghi di immagini in modo sparso e semplifica la gestione di attributi e dati globali, come modelli condivisi, macro, font e così via.

Inoltre, il catalogo predefinito fornisce tutti gli attributi e i record di dati (macro, font, profili ICC, regole di pre-elaborazione richieste) quando non è coinvolto un catalogo di immagini specifico in un’operazione.

Per il corretto funzionamento di [!DNL Platform Server], il file degli attributi del catalogo per il catalogo predefinito deve essere denominato [!DNL default.ini], deve sempre esistere nella cartella del catalogo e deve essere compilato completamente con tutti gli attributi richiesti, esclusi `attribute::RootId` e i riferimenti ai vari file di dati del catalogo, che sono tutti facoltativi.

>[!NOTE]
>
>Tutti i file di attributi del catalogo, tranne [!DNL default.ini], devono contenere un valore `attribute::RootId` univoco. `attribute::RootId` in [!DNL default.ini] deve essere vuoto.
