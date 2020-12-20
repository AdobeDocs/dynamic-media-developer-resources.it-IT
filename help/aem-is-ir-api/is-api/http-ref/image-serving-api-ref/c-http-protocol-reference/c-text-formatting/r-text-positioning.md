---
description: Il renderer text= posiziona il testo in modo fondamentalmente diverso dal renderer textPs= quando viene applicato ai livelli predimensionati (ovvero quando è specificato anche size=).
seo-description: Il renderer text= posiziona il testo in modo fondamentalmente diverso dal renderer textPs= quando viene applicato ai livelli predimensionati (ovvero quando è specificato anche size=).
seo-title: Posizionamento del testo
solution: Experience Manager
title: Posizionamento del testo
topic: Scene7 Image Serving - Image Rendering API
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 0%

---


# Posizionamento del testo{#text-positioning}

Il renderer text= posiziona il testo in modo fondamentalmente diverso dal renderer textPs= quando viene applicato ai livelli predimensionati (ovvero quando è specificato anche size=).

I livelli `text=`e `textPs=` di ridimensionamento automatico hanno un aspetto e un posizionamento simili.

`textPs=` allinea la parte superiore della cella di carattere con la parte superiore della casella di testo (assumendo  `\vertalt`), anche se in questo modo alcune parti dei glifi di testo sottoposti a rendering si estendono parzialmente al di fuori del limite della casella di testo. I glifi di cui è stato effettuato il rendering di alcuni font possono sporgere leggermente oltre i bordi sinistro e destro della casella di testo. Per le applicazioni che richiedono che tutto il testo di cui è stato effettuato il rendering sia contenuto nel rettangolo di livello, i comandi RTF `\marg*` o `textFlowPath=` possono essere utilizzati per regolare l’area di rendering del testo.

Al contrario, `text=` sposterà il testo renderizzato in base alle esigenze e garantirà che tutti i glifi sottoposti a rendering rientrino completamente nella casella di testo specificata.

Anche se `text=` può essere leggermente più semplice da usare per applicazioni semplici, `textPs=` offre un posizionamento preciso, indipendente dalle facce dei font e dagli effetti di testo.

## Esempi {#section-1b6bdf2ea34447528188ae4e1430ee71}

Gli esempi seguenti sono per il testo in formato predimensionale. Il comportamento per il ridimensionamento automatico del testo è diverso.

** `Text=` fornisce sempre un margine stretto nella parte superiore:**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` esegue il rendering del testo strettamente allineato alla parte superiore della casella di testo, con conseguente lieve ritaglio, anche per i font comuni come Arial:**

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` sposterà automaticamente verso il basso il testo di cui è stato effettuato il rendering per evitare il ritaglio:**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` non sposta il testo contenente porzioni alzate, con conseguente taglio significativo se il testo si trova sul livello 0:**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Un margine di 10 pt (200 twip) nella parte superiore esegue il rendering del testo senza ritaglio:**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**I glifi di cui è stato effettuato il rendering di alcuni font di script possono estendersi in modo significativo al di fuori della casella di testo:**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
