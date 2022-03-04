---
title: Opacità materiale variabile
description: L'opacità variabile è supportata per i colori solidi e le texture ripetibili applicate agli oggetti sovrapposti, nonché per i decali e i materiali di rivestimento per finestre.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 65f4b578-0c64-4515-8184-2908b317a983
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '134'
ht-degree: 0%

---

# Opacità materiale variabile{#varying-material-opacity}

L&#39;opacità variabile è supportata per i colori solidi e le texture ripetibili applicate agli oggetti sovrapposti, nonché per i decali e i materiali di rivestimento per finestre.

Le informazioni sull’opacità possono essere fornite semplicemente utilizzando un’immagine di RGB con un canale alfa. Inoltre, l&#39;opacità complessiva può essere variata con il `opacity=` (sia per le immagini RGB che RGBA).

I bordi a parete supportano anche le immagini RGBA, principalmente per supportare i bordi di stampa.

La [!DNL vnw] i file che definiscono i rivestimenti delle finestre possono includere un canale di opacità. È combinato dal renderer con il canale alfa della texture ripetibile e il `opacity=` valore per fornire una gamma completa di effetti di opacità per i trattamenti di finestre semplici e traslucide.
