---
description: Image Serving implementa una semplice struttura di watermarking visiva.
solution: Experience Manager
title: Filigrane
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 1%

---

# Filigrane{#watermarks}

Image Serving implementa una semplice struttura di watermarking visiva.

Una filigrana è in genere un&#39;immagine semitrasparente, ma può essere un testo o un&#39;immagine composita a livelli più complessi. Il server posizionerà la filigrana sull&#39;immagine di risposta dopo tutti gli attributi di visualizzazione ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`).

La filigrana viene attivata impostando `attribute::Watermark` a una voce di catalogo valida che contenga l&#39;immagine o il modello della filigrana. Se `attribute::Watermark` è impostato in un catalogo denominato; il server aggiungerà la filigrana a tutte le richieste di immagini che fanno riferimento all’id del catalogo nell’URL della richiesta. Se `default::Watermark` è impostato (nel catalogo predefinito, [!DNL default.ini]), la filigrana viene applicata a tutte le richieste di immagini indipendentemente dal fatto che facciano riferimento o meno a un catalogo.

Le filigrane non vengono applicate alle immagini restituite in risposta a richieste di miniature ( `req=tmb`) e alcune richieste dai visualizzatori Dynamic Media.

## Scala e allineamento {#section-89ef9e5926ae438abbd8e70332749b76}

Quando viene specificata una filigrana, il server genera prima l&#39;immagine composita (il *immagine target*) a cui deve essere applicata la filigrana (prima di applicare le trasformazioni di visualizzazione). Il server genera quindi l&#39;immagine composita per la filigrana come qualsiasi altra immagine (il *immagine filigrana*).

A differenza delle immagini standard, `sizeN=` possono essere specificati per layer=0 o layer=comp dell&#39;immagine della filigrana. Questo consente di ridimensionare l’immagine della filigrana rispetto all’immagine di destinazione. Se `sizeN=` non viene specificata, l&#39;immagine della filigrana mantiene le sue dimensioni in pixel quando viene unita all&#39;immagine di destinazione.

Comandi di richiesta (ad esempio `fmt=`) e visualizza i comandi (ad esempio `wid=`) vengono ignorati nei record di filigrana, ad eccezione di `align=`. `align=` può essere utilizzato per posizionare l&#39;immagine della filigrana rispetto all&#39;immagine della filigrana relativa all&#39;immagine di destinazione. Questo consente di posizionare la filigrana rispetto a un angolo o a un bordo dell&#39;immagine di destinazione.

Dopo il ridimensionamento e l&#39;allineamento, il server posizionerà l&#39;immagine della filigrana sull&#39;immagine di destinazione utilizzando `blendMode=` e `opac=` valori specificati per `layer=0` o `layer=comp` dell&#39;immagine della filigrana. Infine, i comandi di richiesta e visualizzazione specificati per l&#39;immagine di destinazione vengono applicati per costruire l&#39;immagine di risposta.

L&#39;immagine della filigrana non si estenderà mai su uno spazio vuoto aggiunto all&#39;immagine di risposta dal `wid=` e `hei=` comandi.

## Esempio {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Una tipica filigrana può essere costituita da una semplice immagine RGBA contenente un logo o un avviso di copyright. Creiamo un record nel catalogo immagini (o nel catalogo predefinito) con `catalog::Id` impostato su `watermark` e specifica il file immagine della filigrana in `catalog::Path`. Vogliamo allungare la filigrana in modo da adattarla all&#39;immagine della vista (senza distorcere la filigrana) lasciando un po&#39; più di margine, e ridurre l&#39;opacità al 20% della filigrana originale, quindi impostiamo `catalog::Modifier` a `sizeN=0.9,0.9&opac=20`. Per attivare la filigrana, impostare `attribute::Watermark` all&#39;id della voce del catalogo filigrana, in questo esempio &quot;watermark&quot;. Potremmo voler sperimentare con diversi `blendMode=` scelte per ottenere diversi effetti di watermarking.

## Consultate anche {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attributo::Filigrana](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
