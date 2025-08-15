---
title: Init
description: JavaScript riferimento API per il visualizzatore Video interattivo.
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Interactive Videos
role: Developer,User
exl-id: 5fcc7dcd-a9a8-4a87-9c8d-42717ced8ae9
source-git-commit: 17556c64af32c957ac25312e2a3288a8d86b5679
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 0%

---

# Init{#init}

JavaScript riferimento API per il visualizzatore Video interattivo.

`init()`

Avvia l&#39;inizializzazione del visualizzatore Video interattivo. A questo punto, l&#39;elemento DOM contenitore deve essere creato in modo che il codice visualizzatore possa trovarlo in base al proprio ID.

Se l&#39;elemento contenitore non fa ancora parte del layout della pagina Web, ad esempio nascosto `display:none` utilizzando lo stile assegnatogli, il visualizzatore sospende il processo di inizializzazione. Lo fa fino al momento in cui la pagina web riporta l&#39;elemento contenitore al layout. Quando si verifica questo evento, il caricamento della visualizzatore riprende automaticamente.

Chiamare questo metodo solo una volta durante visualizzatore ciclo di vita; Le chiamate successive vengono ignorate.

## Parametri {#section-ad069aaaf4f145f2b50ae5ac89ca1ed2}

Nessuno.

## Rendiconto {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}` Un riferimento alla visualizzatore istanza.

## Esempio {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.init()
```
