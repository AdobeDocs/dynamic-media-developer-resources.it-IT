---
description: Le impostazioni in questa sezione devono essere considerate solo se è richiesto il rendering di SVG.
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# SVG{#svg}

Le impostazioni in questa sezione devono essere considerate solo se è richiesto il rendering di SVG.

## SV::SvgHeapSize - SVG Heap Size {#section-59ab17681daa4be8b5d794713e1a504e}

Dimensione dell’heap Java per SVG Renderer. Il valore predefinito è &quot;200m&quot; (200 Mbyte).

## PS::svgProvider.rootPaths - Cartelle principali dei dati di SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Percorso dei file di dati di origine di SVG. Può essere uno o più percorsi di file assoluti o relativi *[!DNL install_folder]*, separati da punto e virgola. In genere impostato sullo stesso valore di `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Dimensione massima file SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Dimensione massima del file di origine SVG in kBytes. Il server restituisce un errore quando si tenta di eseguire il rendering di un file SVG di dimensioni superiori a questo limite. Il valore predefinito è 1024 kbyte.

## IS::SvgMAxRenderRngPixels - Limite dimensione immagine output SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Limita le dimensioni delle immagini che SVGRender può produrre. Valore intero maggiore di 0 in milioni di pixel. Se un’operazione di rendering supera il limite di dimensioni, viene restituito un errore. Il valore predefinito è 4.

## PS::svgProvider.port - [!DNL Platform Server] Porta di ascolto {#section-f7e42a96c2dd4523b46f0557c239e659}

La porta utilizzata per SvgRender per ottenere immagini dal [!DNL Platform Server] da incorporare nei rendering di SVG.

Importante Per il corretto funzionamento del componente SVGRender, questa opzione di configurazione deve essere impostata sullo stesso valore di `TC::PsPort`.

## PS::svgProvider.fontRoot - Cartella dei file di font di SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Specifica dove verranno trovati i file di font necessari per il rendering del testo di SVG; in genere uno dei percorsi specificati in `IS::RootPaths`. Il valore predefinito è [!DNL  *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Porta di comunicazione SVG {#section-608687123aa644b7b58fe42385d71b79}

Configura la porta sulla quale il server di immagini e il componente SVGRender comunicano.

>[!NOTE]
>
>Per il corretto funzionamento del componente SVGRender, è necessario specificare lo stesso numero di porta per `SVG::SVGRender.port` e `IS::SVGTcpPort`.
