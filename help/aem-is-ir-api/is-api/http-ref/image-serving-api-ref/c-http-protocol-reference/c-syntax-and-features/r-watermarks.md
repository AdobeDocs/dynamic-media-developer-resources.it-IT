---
description: Image Serving implementa una semplice funzione di filigrana visiva.
solution: Experience Manager
title: Filigrane
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e744be3f-9753-4513-8f37-055fa03077cc
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# Filigrane{#watermarks}

Image Serving implementa una semplice funzione di filigrana visiva.

Una filigrana è in genere un&#39;immagine semitrasparente, ma può essere costituita da testo o da un&#39;immagine composita a livelli più complessa. Il server posizionerà la filigrana sull&#39;immagine di risposta dopo tutti gli attributi di visualizzazione ( `wid=`, `hei=`, `align=`, `scl=`, `bgc=`) sono state applicate.

La filigrana è abilitata dall’impostazione `attribute::Watermark` a una voce di catalogo valida che conterrebbe l’immagine o il modello della filigrana. Se `attribute::Watermark` è impostato in un catalogo denominato, il server aggiungerà la filigrana a tutte le richieste di immagini che fanno riferimento all’id catalogo nell’URL della richiesta. Se `default::Watermark` è impostato (nel catalogo predefinito, [!DNL default.ini]), la filigrana viene applicata a tutte le richieste di immagini che facciano riferimento o meno a un catalogo.

Le filigrane non vengono applicate alle immagini restituite in risposta alle richieste di miniature ( `req=tmb`) e alcune richieste provenienti dai visualizzatori Dynamic Media.

## Ridimensionamento e allineamento {#section-89ef9e5926ae438abbd8e70332749b76}

Quando viene specificata una filigrana, il server genera prima l&#39;immagine composita (l&#39; *immagine di destinazione*) a cui deve essere applicata la filigrana (prima di applicare le trasformazioni di visualizzazione). Il server genera quindi l&#39;immagine composita per la filigrana come qualsiasi altra immagine (il *immagine filigrana*).

A differenza delle immagini standard, `sizeN=` può essere specificato per layer=0 o layer=comp dell’immagine della filigrana. Ciò consente di ridimensionare l’immagine della filigrana rispetto all’immagine di destinazione. Se `sizeN=` non è specificato, l&#39;immagine della filigrana mantiene le dimensioni in pixel quando viene unita all&#39;immagine di destinazione.

Comandi di richiesta (come `fmt=`) e i comandi di visualizzazione (come `wid=`) vengono ignorate nei record delle filigrane, ad eccezione `align=`. `align=` può essere utilizzato per posizionare l’immagine della filigrana rispetto all’immagine della filigrana rispetto all’immagine di destinazione. Ciò consente di posizionare la filigrana rispetto a un angolo o a un bordo dell’immagine di destinazione.

Dopo il ridimensionamento e l&#39;allineamento, il server posizionerà l&#39;immagine della filigrana sull&#39;immagine di destinazione utilizzando `blendMode=` e `opac=` valori specificati per `layer=0` o `layer=comp` dell&#39;immagine della filigrana. Infine, i comandi di richiesta e di visualizzazione specificati per l’immagine di destinazione vengono applicati per costruire l’immagine di risposta.

L’immagine della filigrana non si estenderà mai oltre gli spazi vuoti aggiunti all’immagine di risposta da `wid=` e `hei=` comandi.

## Esempio {#section-0408c977d7324d4cb0e76a91cdfa2acd}

Una filigrana tipica può essere costituita da una semplice immagine RGBA contenente un logo o un avviso di copyright. Creiamo un record nel catalogo immagini (o nel catalogo predefinito) con `catalog::Id` imposta su `watermark` e specificare il file di immagine della filigrana in `catalog::Path`. Vogliamo estendere la filigrana per adattarla all&#39;immagine di visualizzazione (senza distorcere la filigrana) lasciando un po&#39; di margine in più, e ridurre l&#39;opacità al 20% della filigrana originale, quindi impostiamo `catalog::Modifier` a `sizeN=0.9,0.9&opac=20`. Per attivare la filigrana, imposta `attribute::Watermark` all&#39;id della voce di catalogo filigrana, &quot;filigrana&quot; in questo esempio. Potremmo voler sperimentare con diversi `blendMode=` scelte per ottenere diversi effetti filigrana.

## Consultate anche {#section-4d66713abacb42c7b6a0c93cbf966a97}

[attributo::filigrana](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-attributes-reference/r-watermark.md#reference-942b50acb2dd43a5ae498dc41ea9ac9b)
