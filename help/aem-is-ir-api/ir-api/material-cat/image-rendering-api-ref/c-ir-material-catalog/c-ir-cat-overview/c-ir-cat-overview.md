---
title: Panoramica del catalogo dei materiali
description: I cataloghi dei materiali forniscono al server informazioni su vignettature, materiali e dati di supporto, ad esempio profili ICC.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
TQID: 'https://experienceleague.adobe.com/wMShsstpVRBE4JNSUshejo0Qn6NXVB85YbLx5Pf9PEI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 0%

---

# Panoramica del catalogo dei materiali{#material-catalog-overview}

I cataloghi dei materiali forniscono al server informazioni su vignettature, materiali e dati di supporto, ad esempio profili ICC.

Ogni catalogo dei materiali è costituito da un *file degli attributi del catalogo* obbligatorio e da un set di *file dei dati del catalogo* facoltativi:

* Il file di mappa vignettatura, che elenca in dettaglio vignettature e modelli e i metadati associati.
* Il file di dati dei materiali, che descrive i materiali e specifica i file di immagine della trama e i metadati associati.
* Il file delle definizioni delle macro, che fornisce le definizioni per le macro di richiesta.
* Il file di mappa del profilo, che specifica i profili colore ICC.

I file di dati del catalogo sono associati ai cataloghi di materiale tramite riferimenti di file nel file di attributi del catalogo. Lo stesso file di dati di catalogo può essere condiviso da più cataloghi di materiale.

I file degli attributi del catalogo devono avere un suffisso di file [!DNL `.ini`] e trovarsi nella cartella del catalogo *di Image Rendering (*) ( [!DNL PlatformServer::ir.catalogRootPath]). I file di dati del catalogo possono trovarsi nella stessa cartella o in qualsiasi altra cartella accessibile al server di rendering.

**Aggiornamento dei cataloghi dei materiali**

Il server controlla continuamente la cartella del catalogo. Ricarica automaticamente un catalogo dei materiali, inclusi i file di dati del catalogo associati, quando rileva che il file di attributi del catalogo principale è stato modificato. Pertanto, per aggiornare i cataloghi di materiale sul server, sostituisci prima tutti i file di dati del catalogo che devono essere modificati, quindi sostituisci (o &quot;tocca&quot;) il file degli attributi del catalogo per attivare il ricaricamento del catalogo.

**Catalogo predefinito**

Il catalogo predefinito fornisce i valori predefiniti per tutti gli attributi del catalogo per tutti i cataloghi di materiale. Se non è possibile trovare un attributo specifico in un catalogo dei materiali specifico, il server utilizza il valore corrispondente del catalogo predefinito. Analogamente, il catalogo predefinito può essere utilizzato per fornire valori predefiniti per record di dati di catalogo specifici (materiali e profili ICC). Se non è possibile trovare un record di dati specifico in un catalogo di materiali specifico, il server tenta di trovarlo nel catalogo predefinito. Ciò consente di compilare i cataloghi di materiale in modo limitato e semplifica la gestione di attributi e dati globali, ad esempio modelli condivisi, macro e font.

Inoltre, il catalogo predefinito fornisce tutti gli attributi e i record di dati (profili ICC) quando non è coinvolto alcun catalogo di materiale specifico in un&#39;operazione.

Per il corretto funzionamento del server di rendering, il file degli attributi del catalogo predefinito deve essere denominato [!DNL default.ini]. Deve inoltre essere sempre presente nella cartella del catalogo e deve essere compilato completamente con tutti gli attributi richiesti, esclusi `attribute::RootId` e i riferimenti ai vari file di dati del catalogo, che sono tutti facoltativi.

<!--
 **See also**

`PlatformServer::ir.catalogRootPath`
-->
