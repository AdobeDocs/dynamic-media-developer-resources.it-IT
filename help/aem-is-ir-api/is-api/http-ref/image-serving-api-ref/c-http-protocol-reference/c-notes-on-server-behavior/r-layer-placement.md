---
title: Posizionamento livello
escription: Layers are positioned by aligning the layer origin (origin=) with the background layer origin at an offset specified by pos=.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1ce7bef3-a0f8-44fc-a146-7e819c30eee8
TQID: https://experienceleague.adobe.com/SMf4V0AmxYIi0o0FZhMkRx9pprIxjJjEcCWT2agF1Bo
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 0f5947b3f28ba40cd479df463c843f7e99155d5e
workflow-type: tm+mt
source-wordcount: 91
ht-degree: 0%

---

# Posizionamento livello{#layer-placement}

I livelli vengono posizionati allineando l&#39;origine del livello (origine=) con l&#39;origine del livello di sfondo in corrispondenza di un offset specificato da pos=.

Se l&#39;origine del livello non è specificata in modo esplicito per un livello immagine, viene calcolata come segue:

1. Determinate l&#39;ancoraggio dell&#39;immagine. Utilizzare `anchor=` o, se non specificato, `catalog::Anchor`.
1. Se l&#39;ancoraggio immagine è definito, applicare il livello trasforma e `extend=` per convertirlo in un valore origin=.
1. Se non è definito alcun ancoraggio immagine, l&#39;origine del livello viene posizionata al centro del rettangolo del livello (dopo aver applicato `extend=`).

![Immagine posizionamento livello](assets/layerplacement.png)
