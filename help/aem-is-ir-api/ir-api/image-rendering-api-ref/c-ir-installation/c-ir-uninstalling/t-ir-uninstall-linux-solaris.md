---
description: Seguire queste istruzioni per disinstallare Image Rendering su un sistema Linux o Solaris.
solution: Experience Manager
title: Disinstallazione su Linux e Solaris
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '128'
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



