---
description: I file di dati di origine di Image Server includono file immagine e maschera, font e profili ICC.
solution: Experience Manager
title: Dati di origine
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator,Business Practitioner
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 0%

---

# Dati di origine{#source-data}

I file di dati di origine di Image Server includono file immagine e maschera, font e profili ICC.

Tutti i file di dati di origine devono essere accessibili al server di immagini. Image Serving fornisce una serie di alternative per specificare la posizione dei file di dati:

`*`install_`*/ *``*/ *`folderrootPathfilePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath  </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogo::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> percorso e nome del file immagine relativo specificati in una richiesta HTTP di Image Server</span> </p></td> 
 </tr> 
</table>

Il server combina i segmenti di percorso da destra a sinistra fino a quando non viene stabilito un percorso di file assoluto.

Tutti i segmenti `*`rootPath`*` possono essere vuoti, relativi o assoluti.

`*``*` catalogPath un percorso/nome file assoluto o relativo. `*``*` requestPathdeve essere un percorso/nome di file relativo.

`Multiple IS::RootPath` I valori possono essere definiti in ImageServerRegistry.xml (o tramite l&#39;interfaccia di amministrazione). Ciò consente la distribuzione dei file di dati di origine su più file system. Il server immagini proverà percorsi alternativi nell&#39;ordine specificato fino a quando il file di dati non viene trovato.

È possibile aggiungere nuovi file di dati di qualsiasi tipo in qualsiasi momento senza interrompere il server.
