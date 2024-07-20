---
title: Disinstallazione su Linux® e Solaris™
description: Seguire queste istruzioni per disinstallare Image Rendering su un sistema Linux® o Solaris™.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 8454991568374ecd1c4babdd3210250ea7988c4c
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 4%

---

# Disinstallazione su Linux® e Solaris™{#uninstalling-on-linux-and-solaris}

Seguire queste istruzioni per disinstallare Image Rendering su un sistema Linux® o Solaris™. È possibile utilizzare due metodi diversi. Effettuate una delle seguenti operazioni:

## Metodo 1

1. Trova [!DNL uninstall.sh].

   Si trova nella directory da cui è stato installato ImageRendering. Se la directory è stata rimossa, il pacchetto di installazione originale deve essere decompresso e non archiviato per estrarre [!DNL uninstall.sh].
1. Eseguire [!DNL uninstall.sh] e seguire le istruzioni visualizzate.

## Metodo 2

1. Interrompi ImageRendering con quanto segue:

   ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`

1. Rimuovere ImageRendering dal sistema. Il comando utilizzato dipende dal sistema.
   * Linux®: `rpm -e ImageRendering`

   * Solaris™: `pkgrm ImageRendering`

1. Eliminare le directory o i file non rimossi al passaggio 2.

