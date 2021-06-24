---
description: Le impostazioni in questa sezione devono essere considerate solo se è richiesto il rendering SVG.
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 1%

---

# SVG{#svg}

Le impostazioni in questa sezione devono essere considerate solo se è richiesto il rendering SVG.

## SV::SvgHeapSize - SVG Heap Size {#section-59ab17681daa4be8b5d794713e1a504e}

Dimensione dell’heap Java per il modulo di rendering SVG. Il valore predefinito è &quot;200m&quot; (200 Mbyte).

## PS::svgProvider.rootPaths - Cartelle principali dei dati SVG {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

Posizione dei file di dati di origine SVG. Può essere uno o più percorsi di file assoluti o percorsi relativi a *[!DNL install_folder]*, separati da punto e virgola. In genere impostato sullo stesso valore di `IS::RootPath`.

## PS::svgProvider.SVGFileSizeLimit - Dimensione massima file SVG {#section-b9c81e3e104642ebbdd9f000843d3256}

Dimensione massima del file sorgente SVG in kBytes. Il server restituisce un errore quando si tenta di eseguire il rendering di un file SVG superiore a questo limite. Il valore predefinito è 1024 kbyte.

## IS::SvgMAxRenderRngPixels - Limite dimensione immagine di uscita SVG {#section-5be1fd9639424d878a5ffd11736d3920}

Limita le dimensioni delle immagini che SVGRender può produrre. Valore intero maggiore di 0 in milioni di pixel. Se un’operazione di rendering supera il limite di dimensioni, viene restituito un errore. Il valore predefinito è 4.

## PS::svgProvider.port - Porta di ascolto del server della piattaforma {#section-f7e42a96c2dd4523b46f0557c239e659}

Porta utilizzata per SvgRender per ottenere immagini dal server Platform da incorporare nei rendering SVG.

Importante Per il corretto funzionamento del componente SVGRender, questa opzione di configurazione deve essere impostata sullo stesso valore di `TC::PsPort`.

## PS::svgProvider.fontRoot - Cartella File di font SVG {#section-a8d45b0d68504945b8780f5eac351b0d}

Specifica dove verranno trovati i file di font necessari per il rendering del testo SVG; in genere uno dei percorsi specificati in `IS::RootPaths`. Il valore predefinito è [!DNL *[!DNL install_folder]*/images].

## SVG::SVGRender.port, IS::SVGTcpPort - Porta di comunicazione SVG {#section-608687123aa644b7b58fe42385d71b79}

Configura la porta sulla quale il server di immagini e il componente SVGRender comunicano.

>[!NOTE]
>
>Per il corretto funzionamento del componente SVGRender, è necessario specificare lo stesso numero di porta per `SVG::SVGRender.port` e `IS::SVGTcpPort`.
