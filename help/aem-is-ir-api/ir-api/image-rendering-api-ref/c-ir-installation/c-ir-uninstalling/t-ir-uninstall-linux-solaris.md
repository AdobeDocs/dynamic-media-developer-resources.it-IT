---
description: Seguite queste istruzioni per disinstallare Image Rendering su un sistema Linux o Solaris.
seo-description: Seguite queste istruzioni per disinstallare Image Rendering su un sistema Linux o Solaris.
seo-title: Disinstallazione su Linux e Solaris
solution: Experience Manager
title: Disinstallazione su Linux e Solaris
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 80c0d6ec-985b-4596-bd67-22e5029f7b37
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Disinstallazione su Linux e Solaris{#uninstalling-on-linux-and-solaris}

Seguite queste istruzioni per disinstallare Image Rendering su un sistema Linux o Solaris.

Esistono due modi per disinstallare Image Rendering su un sistema Linux o Solaris.

**Metodo 1**

1. Trova [!DNL uninstall.sh].

   Si trova nella directory da cui è stato installato ImageRendering. Se questa directory è stata rimossa, il pacchetto di installazione originale deve essere non compresso e non deve essere utilizzato per estrarre [!DNL uninstall.sh].
1. Eseguire [!DNL uninstall.sh] e seguire le istruzioni sullo schermo.

>**Metodo 2**
>
>1. Interrompi ImageRendering con: ` *[!DNL install_folder]*/bin/ImageRendering.sh stop.`
>1. Rimuovete ImageRendering dal sistema.

>
>   
Il comando per rimuovere ImageRendering dipende dal sistema in uso:
>
>   Linux: `rpm -e ImageRendering`
>
>   Solaris: `pkgrm ImageRendering`
>
>1. Eliminate le directory o i file che non sono stati rimossi nel passaggio 2.

>



