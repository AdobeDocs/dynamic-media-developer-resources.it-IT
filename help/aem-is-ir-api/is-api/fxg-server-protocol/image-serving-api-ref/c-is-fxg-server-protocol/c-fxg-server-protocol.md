---
title: Protocollo server FXG
description: Per manipolare un elemento grafico, potete usare punti di riferimento simili ai punti cardinali.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 57d9ba37-819e-455f-9b22-bd7aabffe007
TQID: 'https://experienceleague.adobe.com/DXmhIshiUYoP-BlVe5cJFXbII9sEIdyo5YDkoKP-t0w'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 28%

---

# Protocollo server FXG{#fxg-server-protocol}

Per manipolare un elemento grafico, potete usare punti di riferimento simili ai punti cardinali.

Questi consentono di ruotare o ridimensionare un elemento grafico rispetto a un particolare punto di riferimento. I punti di riferimento sono `northWest`, `north`, `northEast`, `west`, `center`, `east`, `southWest`, `south` e `southeast`. Ad esempio, utilizzando il punto di riferimento centrale, potete ruotare un&#39;immagine di 45° rispetto al centro. L&#39;immagine seguente mostra la posizione dei punti di riferimento, un elemento grafico, l&#39;elemento grafico ruotato di 20° dal punto di riferimento `northWest` e l&#39;elemento grafico ruotato di 20° dal punto di riferimento `east`.

![Immagine punti di riferimento](assets/wp_ref_points.png)

* A. Posizioni dei punti di riferimento
* B. Elemento grafico
* C. L&#39;immagine è ruotata di 20° rispetto al punto di riferimento `northWest`
* D. L&#39;immagine è ruotata di 20° rispetto al punto di riferimento `east`

È richiesta la seguente sintassi:

`referencePoint <string> (northWest, north, northEast, west, center, east, southWest, south, southEast, none, inherit)`

Il valore predefinito è none. Il valore `inherit` passa il valore `s7:referencePoint`, purché non sia `none`, dalla parte superiore della pagina o del livello del gruppo a tutti gli elementi figlio. L&#39;impostazione `none` indica che non esiste alcun punto di riferimento per l&#39;oggetto e che viene utilizzato il sistema di coordinate FXG.

>[!NOTE]
>
>per usare un punto di riferimento ma non produrre alcuno spostamento nell’oggetto dopo che è stato manipolato, aggiornare i valori x e y dell’oggetto dopo averlo manipolato.

Quando un valore di `s7:referencePoint` viene utilizzato con gruppi (o percorsi, elementi di linea o qualsiasi elemento che non dispone di definizioni esplicite di larghezza e altezza), il valore viene applicato al riquadro limite cumulativo del gruppo. Ad esempio, il punto in alto a sinistra del rettangolo di selezione di tutti gli oggetti del gruppo funge da punto di riferimento `northWest` per il gruppo; il punto in basso a destra funge da punto di riferimento `southEast`.
