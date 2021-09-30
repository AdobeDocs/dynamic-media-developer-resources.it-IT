---
title: Posizionamento del testo
description: Il modulo di rendering text= posiziona il testo in modo fondamentalmente diverso dal modulo di rendering textPs= quando viene applicato a livelli predefiniti (ovvero quando è specificato anche size=).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# Posizionamento del testo{#text-positioning}

Il modulo di rendering `text=` posiziona il testo in modo fondamentalmente diverso rispetto al modulo di rendering textPs= quando viene applicato a livelli predefiniti (ad esempio se è specificato anche size=).

I livelli di ridimensionamento `text=`e `textPs=` hanno aspetto e posizionamento simili.

La sezione `textPs=` allinea la parte superiore della cella di carattere con la parte superiore della casella di testo (assumendo `\vertalt`), anche se comporta l’estensione parziale di parti dei glifi di testo sottoposti a rendering al di fuori del bordo della casella di testo. Anche i glifi sottoposti a rendering di determinati font possono sporgere leggermente oltre i bordi sinistro e destro della casella di testo. Per le applicazioni che richiedono che tutto il testo sottoposto a rendering sia contenuto all&#39;interno del rettangolo di livello, è possibile utilizzare i comandi RTF `\marg*` o `textFlowPath=` per regolare l&#39;area di rendering del testo.

Al contrario, `text=` sposta il testo di cui è stato effettuato il rendering in base alle esigenze e garantisce che tutti i glifi di cui è stato effettuato il rendering rientrino completamente nella casella di testo specificata.

Mentre `text=` può essere un po&#39; più facile da usare per le applicazioni semplici, `textPs=` offre un posizionamento preciso indipendente dalle facce di font e dagli effetti di testo.

## Esempi {#section-1b6bdf2ea34447528188ae4e1430ee71}

Gli esempi seguenti sono relativi al testo di dimensioni predefinite. Il comportamento per il ridimensionamento automatico del testo è diverso.

** `Text=` fornisce sempre un margine stretto nella parte superiore:**

![Esempio di posizionamento del testo in un’immagine](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` esegue il rendering del testo allineato rigorosamente nella parte superiore della casella di testo, con conseguente lieve ritaglio, anche per i font comuni come Arial®:**

![Esempio di posizionamento del testo: due immagini](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` sposta automaticamente il testo di cui è stato effettuato il rendering verso il basso per evitare il ritaglio:**

![Esempio di posizionamento del testo tre immagini](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` non sposta il testo contenente parti alzate, con conseguente ritaglio significativo se il testo è sul livello 0:**

![Esempio di posizionamento del testo quattro immagini](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Un margine di 10 pt (200 twip) in alto esegue il rendering di questo testo senza ritaglio:**

![Esempio di posizionamento del testo cinque immagini](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**I glifi sottoposti a rendering di alcuni font di script possono estendersi in modo significativo al di fuori della casella di testo:**

![Esempio di posizionamento del testo sei immagini](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
