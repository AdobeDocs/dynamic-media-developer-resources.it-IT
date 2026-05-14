---
title: Elaborazione delle variabili nelle richieste esterne incorporate
description: I riferimenti $var$ che si verificano in qualsiasi punto all'interno delle parentesi graffe di una richiesta esterna incorporata vengono sostituiti con valori di definizione della variabile corrispondenti.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: a87bb2a0-0554-4978-982d-b6617925cd53
TQID: 'https://experienceleague.adobe.com/-0KT9d6qz9-8d41vKNgbCYUKQQLBRaLE-0TFmyIvRCM'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 98
ht-degree: 0%

---

# Elaborazione delle variabili nelle richieste esterne incorporate{#variable-processing-in-embedded-foreign-requests}

I riferimenti `$var$` che si verificano in qualsiasi punto all&#39;interno delle parentesi graffe di una richiesta esterna incorporata vengono sostituiti con i valori di definizione della variabile corrispondenti.

Consente di inserire richieste esterne incorporate in un modello in un catalogo immagini.

I valori delle variabili che devono essere sostituiti in richieste esterne in genere devono avere una doppia codifica, perché non viene applicata alcuna nuova codifica prima che il server tenti di trasmettere l’URL esterno finale.
