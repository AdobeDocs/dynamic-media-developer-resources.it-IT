---
title: SVG
description: Le impostazioni di questa sezione devono essere considerate solo se è richiesto il rendering SVG.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 1%

---

# SVG{#svg}

Le impostazioni di questa sezione devono essere considerate solo se è richiesto il rendering SVG.

## SV::SvgHeapSize - Dimensione heap SVG {#section-59ab17681daa4be8b5d794713e1a504e}

Dimensione heap Java per SVG Renderer. Impostazione predefinita: &quot;200m&quot; (200 MB).

## PS::svgProvider.rootPaths - Cartelle radice dati SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Percorso dei file di dati di origine di SVG. Può essere uno o più percorsi di file assoluti o relativi a *[!DNL install_folder]*, separati da punto e virgola. In genere è impostato sullo stesso valore di `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Dimensione massima file SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Dimensione massima del file di origine SVG in KB. Il server restituisce un errore quando si tenta di eseguire il rendering di un file SVG che supera questo limite. Il valore predefinito è 1024 kbyte.

## IS::SvgMAxRenderRgnPixels - Limite dimensioni immagine di output SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Limita le dimensioni delle immagini che SVGRender può produrre. Valore intero maggiore di 0 in milioni di pixel. Se un’operazione di rendering supera il limite di dimensioni, viene restituito un errore. Il valore predefinito è 4.

## PS::svgProvider.port - [!DNL Platform Server] Porta di ascolto {#section-f7e42a96c2dd4523b46f0557c239e659}

Porta utilizzata per SvgRender per ottenere immagini dalla [!DNL Platform Server] da incorporare nei rendering SVG.

Importante Per il corretto funzionamento del componente SVGRender, questa opzione di configurazione deve essere impostata sullo stesso valore di `TC::PsPort`.

## PS::svgProvider.fontRoot - Cartella file di font SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Specifica dove SvgRender trova i file di font necessari per il rendering del testo SVG; in genere uno dei percorsi specificati in `IS::RootPaths`. Il valore predefinito è [!DNL  *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Porta di comunicazione SVG {#section-608687123aa644b7b58fe42385d71b79}

Configura la porta su cui comunicano il server immagini e il componente SVGRender.

>[!NOTE]
>
>Per il corretto funzionamento del componente SVGRender, è necessario specificare lo stesso numero di porta per `SVG::SVGRender.port` e `IS::SVGTcpPort`.
