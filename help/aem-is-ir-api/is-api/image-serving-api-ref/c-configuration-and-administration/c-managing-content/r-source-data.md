---
description: I file di dati di origine di Image Server includono file immagine e maschera, font e profili ICC.
solution: Experience Manager
title: Dati sorgente
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: d7e9c101-8d34-4241-b03c-131f31c25933
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---

# Dati sorgente{#source-data}

I file di dati di origine di Image Server includono file immagine e maschera, font e profili ICC.

Tutti i file di dati di origine devono essere accessibili al server immagini. Image Server offre diverse alternative per specificare la posizione dei file di dati:

`*`install_folder`*/ *`rootPath`*/ *`filePath`*`

<table id="simpletable_26686444C7EF46D6BC4C0490C8010BF9"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> rootPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> IS::RootPath/attribute::RootPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> filePath </span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalogPath|requestPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> catalogPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> catalog::Path|catalog::MaskPath|icc::ProfilePath|font::FontPath|font::MetricsPath</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> requestPath</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> nome e percorso del file immagine relativo specificati in una richiesta HTTP di Image Server</span> </p></td> 
 </tr> 
</table>

Il server combina i segmenti di percorso da destra a sinistra fino a quando non viene stabilito un percorso di file assoluto.

Tutti `*`rootPath`*` i segmenti possono essere vuoti, relativi o assoluti.

`*`catalogPath`*` è un nome o un percorso di file assoluto o relativo. `*`requestPath`*` deve essere un percorso/nome file relativo.

`Multiple IS::RootPath` I valori possono essere definiti in ImageServerRegistry.xml (o tramite l’interfaccia di amministrazione). Questo consente di distribuire i file di dati di origine su più file system. Il server immagini tenta percorsi alternativi nell&#39;ordine specificato finché non viene trovato il file di dati.

È possibile aggiungere nuovi file di dati di qualsiasi tipo in qualsiasi momento senza arrestare il server.
