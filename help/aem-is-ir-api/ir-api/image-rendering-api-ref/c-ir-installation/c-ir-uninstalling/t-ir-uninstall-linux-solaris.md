---
title: Disinstallazione su Linux® e Solaris™
description: Seguire queste istruzioni per disinstallare Image Rendering su un sistema Linux® o Solaris™.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
TQID: 'https://experienceleague.adobe.com/RmD5z5300Nw12kSsOretyAl5p-TeFkox-Cyqm1MrF5w'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 120
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

