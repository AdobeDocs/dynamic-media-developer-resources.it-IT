---
description: Image Serving implementa una semplice struttura di watermarking visiva.
solution: Experience Manager
title: Filigrane
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 1%

---


# Filigrane{#watermarks}

Image Serving implementa una semplice struttura di watermarking visiva.

Una filigrana è in genere un&#39;immagine semitrasparente, ma può essere un testo o un&#39;immagine composita a livelli più complessi. Il server posizionerà la filigrana sull&#39;immagine di risposta dopo l&#39;applicazione di tutti gli attributi di visualizzazione ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`).

La filigrana viene abilitata impostando `attribute::Watermark` su una voce di catalogo valida che conterrebbe l&#39;immagine o il modello della filigrana. Se `attribute::Watermark` è impostato in un catalogo denominato, il server aggiungerà la filigrana a tutte le richieste di immagini che fanno riferimento all’ID catalogo nell’URL della richiesta. Se `default::Watermark` è impostato (nel catalogo predefinito, [!DNL default.ini]), la filigrana verrà applicata a tutte le richieste di immagini, indipendentemente dal fatto che facciano riferimento o meno a un catalogo.

Le filigrane non vengono applicate alle immagini restituite in risposta a richieste di miniature ( `req=tmb`) e a determinate richieste dei visualizzatori Dynamic Media.

## Ridimensionamento e allineamento {#section-89ef9e5926ae438abbd8e70332749b76}

Quando viene specificata una filigrana, il server genera prima l&#39;immagine composita (l&#39; *immagine di destinazione*) a cui deve essere applicata la filigrana (prima di applicare le trasformazioni di visualizzazione). Il server genera quindi l&#39;immagine composita per la filigrana come qualsiasi altra immagine (l&#39; *immagine filigrana*).

A differenza delle immagini standard, è possibile specificare `sizeN=` per layer=0 o layer=comp dell’immagine della filigrana. Questo consente di ridimensionare l’immagine della filigrana rispetto all’immagine di destinazione. Se `sizeN=` non è specificato, l&#39;immagine della filigrana mantiene le sue dimensioni in pixel quando viene unita all&#39;immagine di destinazione.

I comandi di richiesta (come `fmt=`) e di visualizzazione (come `wid=`) vengono ignorati nei record di filigrana, ad eccezione di `align=`. `align=` può essere utilizzato per posizionare l&#39;immagine della filigrana rispetto all&#39;immagine della filigrana relativa all&#39;immagine di destinazione. Questo consente di posizionare la filigrana rispetto a un angolo o a un bordo dell&#39;immagine di destinazione.

Dopo il ridimensionamento e l’allineamento, il server posizionerà l’immagine della filigrana sull’immagine di destinazione utilizzando i valori `blendMode=` e `opac=` specificati per `layer=0` o `layer=comp` dell’immagine della filigrana. Infine, i comandi di richiesta e visualizzazione specificati per l&#39;immagine di destinazione vengono applicati per costruire l&#39;immagine di risposta.

L&#39;immagine della filigrana non si estenderà mai su uno spazio vuoto aggiunto all&#39;immagine di risposta dai comandi `wid=` e `hei=`.

## Esempio {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Una tipica filigrana può essere costituita da una semplice immagine RGBA contenente un logo o un avviso di copyright. Creiamo un record nel catalogo immagini (o nel catalogo predefinito) con `catalog::Id` impostato su `watermark` e specifichiamo il file immagine della filigrana in `catalog::Path`. Vogliamo allungare la filigrana in modo da adattarla all&#39;immagine della vista (senza distorcere la filigrana) lasciando un po&#39; più di margine, e ridurre l&#39;opacità al 20% della filigrana originale, quindi impostiamo `catalog::Modifier` su `sizeN=0.9,0.9&opac=20`. Per attivare la filigrana, impostare `attribute::Watermark` sull&#39;id della voce del catalogo della filigrana, &quot;watermark&quot; in questo esempio. Vorremmo sperimentare diverse `blendMode=` scelte per ottenere diversi effetti di watermarking.

## Consultate anche {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attributo::Filigrana](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
