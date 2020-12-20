---
description: Prima di utilizzare Scene7 Image Server, accertatevi che il sistema soddisfi i requisiti di sistema.
seo-description: Prima di utilizzare Scene7 Image Server, accertatevi che il sistema soddisfi i requisiti di sistema.
seo-title: Requisiti di sistema e prerequisiti
solution: Experience Manager
title: Requisiti di sistema e prerequisiti
topic: Scene7 Image Serving - Image Rendering API
uuid: 80196574-f5a2-4298-880a-cc36f90b6e21
translation-type: tm+mt
source-git-commit: e8e5b07329bde3e23ee095d5022da62d67e9478c
workflow-type: tm+mt
source-wordcount: '411'
ht-degree: 0%

---


# Requisiti di sistema e prerequisiti{#system-requirements-and-prerequisites}

Prima di utilizzare Scene7 Image Server, accertatevi che il sistema soddisfi i requisiti di sistema.

## Hardware del server {#section-f3c14a7bc1b745118602659628df779f}

Il server deve soddisfare i seguenti requisiti hardware.

>[!NOTE]
>
>I sistemi con processori con AMD64 e Intel® EM64T sono generalmente configurati come piattaforme NUMA (non Uniform Memory Architecture). Ciò significa che il kernel costruisce più nodi di memoria in fase di avvio anziché costruire un singolo nodo di memoria. Il costrutto a più nodi può determinare l&#39;esaurimento della memoria su uno o più nodi prima che gli altri si esauriscano. Quando si verifica l’esaurimento della memoria, il kernel può decidere di interrompere i processi (ad esempio, Image Server o Platform Server) anche se è disponibile memoria. Pertanto,  Adobe Systems consiglia di disattivare la funzione NUMA se si esegue un sistema di questo tipo. Utilizzare l&#39;opzione di avvio `numa=off` per evitare che il kernel interrompa tali processi.

**Windows**

* CPU Intel Xeon® o AMD® Opteron con almeno 4 core.
* Almeno 16 GB di RAM.
* Spazio di scambio pari ad almeno il doppio della quantità di memoria fisica (RAM).
* 2 GB di spazio disponibile su disco rigido per l&#39;installazione e il funzionamento di base, è necessario ulteriore spazio su disco per le immagini sorgente, i file di registro, le cache dei dati e i file manifest.
* Scheda di interfaccia di rete Fast Ethernet

**Linux**

* CPU Intel Xeon® o AMD® Opteron con almeno 4 core.
* Almeno 16 GB di RAM.
* Scambio disattivato (consigliato).
* 2 GB di spazio disponibile su disco rigido per l&#39;installazione e il funzionamento di base, è necessario ulteriore spazio su disco per le immagini sorgente, i file di registro, le cache dei dati e i file manifest.
* Scheda di interfaccia di rete Fast Ethernet

**Nota (Linux):** Image Server non funziona con SELLinux attivato. Questa opzione è attivata per impostazione predefinita. Per disattivare SELLinux, modificate il file [!DNL /etc/selinux/config] e modificate il valore SELLinux da:

`SELINUX=enforcing`

a

`SELINUX=disabled`

**Nota (Linux):** accertatevi che il nome host del server sia risolvibile a un indirizzo IP. Se ciò non è possibile, aggiungete il nome host completo e l&#39;indirizzo IP a [!DNL /etc/hosts] come nell&#39;esempio seguente.

`<ip address> <fully qualified hostname>`

## Software del server {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Scene7 Image Server richiede il seguente software server.

**Windows**

* Microsoft® Windows 2008 Server.
* Sistema operativo a 64 bit.

**Linux**

* Red Hat® Enterprise 5 o CentOS 5.5 e versioni successive, con patch di correzione più recenti.
* Sistema operativo a 64 bit.

**Nota:** per utilizzare Image Server in Windows, è necessario installare Microsoft Visual Studio 2010 redistributable. La ridistribuibile è disponibile nel seguente percorso:

[http://www.microsoft.com/en-us/download/details.aspx?id=13523](http://www.microsoft.com/en-us/download/details.aspx?id=13523)

