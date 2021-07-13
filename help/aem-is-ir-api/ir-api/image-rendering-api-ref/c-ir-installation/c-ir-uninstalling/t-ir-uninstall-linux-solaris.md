---
description: Seguire queste istruzioni per disinstallare Image Rendering su un sistema Linux o Solaris.
solution: Experience Manager
title: Disinstallazione su Linux e Solaris
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: c81feaba-18da-441a-bfd5-40275558a384
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '125'
ht-degree: 0%

---

# Disinstallazione su Linux e Solaris{#uninstalling-on-linux-and-solaris}

Seguire queste istruzioni per disinstallare Image Rendering su un sistema Linux o Solaris.

Esistono due modi per disinstallare Image Rendering su un sistema Linux o Solaris.

**Metodo 1**

1. Trova [!DNL uninstall.sh].

   Si trova nella directory da cui è stato installato ImageRendering. Se questa directory è stata rimossa, il pacchetto di installazione originale deve essere non compresso e non gestito per estrarre [!DNL uninstall.sh].
1. Esegui [!DNL uninstall.sh] e segui le istruzioni sullo schermo.

>**Metodo 2**
>
>1. Interrompi ImageRendering con: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Rimuovi ImageRendering dal sistema.

>
>   
Il comando per rimuovere ImageRendering dipende dal sistema in uso:
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. Elimina le directory o i file che non sono stati rimossi nel passaggio 2.

>


