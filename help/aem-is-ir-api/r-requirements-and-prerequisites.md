---
description: Prima di utilizzare Dynamic Media Image Serving, assicurati che il sistema soddisfi i requisiti di sistema.
solution: Experience Manager
title: Requisiti di sistema e prerequisiti
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# Requisiti di sistema e prerequisiti{#system-requirements-and-prerequisites}

Prima di utilizzare Dynamic Media Image Serving, assicurati che il sistema soddisfi i requisiti di sistema.

## Hardware del server {#section-f3c14a7bc1b745118602659628df779f}

Il server deve soddisfare i seguenti requisiti hardware.

>[!NOTE]
>
>I sistemi con processori con AMD64 e Intel® EM64T sono in genere configurati come piattaforme NUMA (Non-Uniform Memory Architecture). Ciò significa che il kernel costruisce più nodi di memoria in fase di avvio anziché costruire un singolo nodo di memoria. Il costrutto a più nodi può causare esaurimento della memoria su uno o più nodi prima che gli altri nodi si esauriscano. Quando si verifica l&#39;esaurimento della memoria, il kernel può decidere di interrompere i processi (ad esempio, il server di immagini o [!DNL Platform Server]) anche se è disponibile memoria. Pertanto, Adobe Systems consiglia di disattivare NUMA se si utilizza un sistema di questo tipo. Utilizza la `numa=off` opzione di avvio per evitare che il kernel interrompa questi processi.

**Windows**

* CPU Intel Xeon® o AMD® Opteron con almeno 4 core.
* Almeno 16 GB di RAM.
* Spazio di scambio pari almeno al doppio della quantità di memoria fisica (RAM).
* 2 GB di spazio disponibile su disco rigido per l&#39;installazione e il funzionamento di base, è necessario ulteriore spazio su disco per le immagini di origine, i registri, le cache dei dati e i file manifest.
* Scheda di interfaccia di rete Fast Ethernet

**Linux**

* CPU Intel Xeon® o AMD® Opteron con almeno 4 core.
* Almeno 16 GB di RAM.
* Scambio disattivato (consigliato).
* 2 GB di spazio disponibile su disco rigido per l&#39;installazione e il funzionamento di base, è necessario ulteriore spazio su disco per le immagini di origine, i registri, le cache dei dati e i file manifest.
* Scheda di interfaccia di rete Fast Ethernet

**Nota (Linux):** Image Server non funziona con SELinux attivato. Questa opzione è attivata per impostazione predefinita. Per disabilitare SELinux, modifica il [!DNL /etc/selinux/config] e modifica il valore SELinux da:

`SELINUX=enforcing`

a

`SELINUX=disabled`

**Nota (Linux):** Assicurati che il nome host del server sia risolvibile in un indirizzo IP. Se ciò non è possibile, aggiungi il nome host completo e l’indirizzo IP a [!DNL /etc/hosts] come nell’esempio seguente.

`<ip address> <fully qualified hostname>`

## Software server {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Media Image Serving richiede il seguente software server.

**Windows**

* Server Microsoft® Windows 2008.
* Sistema operativo a 64 bit.

**Linux**

* Red Hat® Enterprise 5 o CentOS 5.5 e versioni successive, con patch di correzione più recenti.
* Sistema operativo a 64 bit.

**Nota:** Per utilizzare Image Server su Windows, è necessario installare Microsoft Visual Studio 2010 ridistribuibile.
