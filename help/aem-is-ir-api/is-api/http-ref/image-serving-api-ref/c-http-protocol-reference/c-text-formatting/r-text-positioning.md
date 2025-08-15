---
title: Posizionamento testo
description: Il renderer text= posiziona il testo in modo fondamentalmente diverso dal renderer textPs= quando viene applicato a livelli pre-dimensionati (vale a dire, quando è specificato anche size=).
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# Posizionamento testo{#text-positioning}

Il renderer `text=` posiziona il testo in modo fondamentalmente diverso dal renderer textPs= quando viene applicato a livelli pre-dimensionati (vale a dire, quando si specifica anche size=).

I livelli di ridimensionamento autonomo `text=` e `textPs=` hanno un aspetto e un posizionamento simili.

`textPs=` allinea la parte superiore della cella carattere con la parte superiore della casella di testo (presupponendo `\vertalt`), anche se provoca l&#39;estensione parziale di parti dei glifi di testo renderizzati al di fuori del limite della casella di testo. I glifi con rendering di alcuni tipi di carattere possono anche sporgere leggermente oltre i bordi sinistro e destro della casella di testo. Per le applicazioni che richiedono che tutto il testo sottoposto a rendering sia contenuto all&#39;interno del rettangolo di livello, è possibile utilizzare i comandi RTF `\marg*` o `textFlowPath=` per regolare l&#39;area di rendering del testo.

Al contrario, `text=` sposta il testo sottoposto a rendering in base alle esigenze e garantisce che tutti i glifi sottoposti a rendering rientrino completamente nella casella di testo specificata.

Sebbene `text=` possa essere leggermente più semplice da utilizzare per applicazioni semplici, `textPs=` offre un posizionamento preciso indipendente dalle facce dei font e dagli effetti di testo.

## Esempi {#section-1b6bdf2ea34447528188ae4e1430ee71}

Gli esempi seguenti sono per il testo pre-ridimensionato. Il comportamento del testo con ridimensionamento automatico è diverso.

**&#x200B; `Text=` fornisce sempre un margine stretto nella parte superiore:**

![Esempio di posizionamento del testo con un&#39;immagine](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

**&#x200B; `textPs=` esegue il rendering del testo strettamente allineato alla parte superiore della casella di testo, con conseguente lieve ritaglio, anche per i font comuni come Arial®:**

![Esempio di posizionamento testo due immagini](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

**&#x200B; `text=` sposta automaticamente il testo sottoposto a rendering verso il basso per evitare il ritaglio:**

![Esempio di posizionamento del testo tre immagini](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

Il **&#x200B; `textPs=` non sposta il testo contenente porzioni in rilievo, causando ritagli significativi se il testo si trova sul livello 0:**

![Esempio di posizionamento del testo quattro immagini](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**Un margine di 10 pt (200 twip) nella parte superiore esegue il rendering del testo senza ritaglio:**

![Esempio di posizionamento del testo: cinque immagini](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**I glifi con rendering di alcuni tipi di carattere di script possono estendersi in modo significativo al di fuori della casella di testo:**

![Esempio di posizionamento del testo sei immagini](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
