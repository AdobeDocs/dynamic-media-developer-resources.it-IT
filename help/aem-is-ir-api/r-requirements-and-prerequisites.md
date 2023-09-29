---
title: Requisiti di sistema e prerequisiti
description: Prima di utilizzare Dynamic Medie Image Server, verificare che il sistema soddisfi i requisiti di sistema.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ea2dfec9-0a42-4ccb-8442-6f7c4a39eda1
source-git-commit: 163ac6a6f44193f1b66ae24059630521d7247eae
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# Requisiti di sistema e prerequisiti{#system-requirements-and-prerequisites}

Prima di utilizzare Dynamic Medie Image Server, verificare che il sistema soddisfi i requisiti di sistema.

## Hardware del server {#section-f3c14a7bc1b745118602659628df779f}

Il server deve soddisfare i seguenti requisiti hardware.

>[!NOTE]
>
>I sistemi con processori AMD64 e Intel® EM64T sono in genere configurati come piattaforme NUMA (Non-Uniform Memory Architecture). Ciò significa che il kernel costruisce più nodi di memoria in fase di avvio anziché costruire un singolo nodo di memoria. Il costrutto a più nodi può causare esaurimento della memoria su uno o più nodi prima che gli altri nodi si esauriscano. Quando si verifica esaurimento della memoria, il kernel può decidere di terminare i processi (ad esempio, il server immagini o [!DNL Platform Server]) anche se la memoria è disponibile. Pertanto, Adobe consiglia di disattivare NUMA se si utilizza questo tipo di sistema. Utilizza il `numa=off` per evitare che il kernel interrompa questi processi.

**Windows**

* CPU Intel Xeon® o AMD® Opteron con almeno quattro core.
* Almeno 1 GB di RAM.
* Lo spazio di swap è pari ad almeno il doppio della quantità di memoria fisica (RAM).
* 2 GB di spazio disponibile su disco rigido per l&#39;installazione e le operazioni di base, è necessario spazio su disco aggiuntivo per le immagini di origine, i registri, le cache dei dati e i file manifest.
* Scheda di interfaccia di rete Fast Ethernet.

**Linux®**

* CPU Intel Xeon® o AMD® Opteron con almeno quattro core.
* Almeno 16 GB di RAM.
* Scambio disabilitato (consigliato).
* 2 GB di spazio disponibile su disco rigido per l&#39;installazione e le operazioni di base, è necessario spazio su disco aggiuntivo per le immagini di origine, i registri, le cache dei dati e i file manifest.
* Scheda di interfaccia di rete Fast Ethernet.

**Nota (Linux®):** Image Server non funziona con SELinux attivato. Questa opzione è attivata per impostazione predefinita. Per disabilitare SELinux, modifica il [!DNL /etc/selinux/config] e modificare il valore SELinux da:

`SELINUX=enforcing`

A

`SELINUX=disabled`

**Nota (Linux®):** Verificare che il nome host del server sia risolvibile in un indirizzo IP. Se non è possibile, aggiungi il nome host completo e l’indirizzo IP a [!DNL /etc/hosts] come nell’esempio seguente.

`<ip address> <fully qualified hostname>`

## Software server {#section-5c9aad2e6b8a4bca989e17a2c8476fc4}

Dynamic Medie Image Server richiede il seguente software server.

**Windows**

* Microsoft® Windows Server 2008.
* Sistema operativo a 64 bit.

**Linux®**

* Red Hat® Enterprise 5 o CentOS 5.5 e versioni successive, con le ultime patch di correzione.
* Sistema operativo a 64 bit.

**Nota:** Per utilizzare Image Server su Windows, è necessario installare Microsoft® Visual Studio 2010.
