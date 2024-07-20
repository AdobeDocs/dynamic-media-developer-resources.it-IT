---
description: Questa sezione contiene soluzioni ai problemi che si sono verificati occasionalmente con Image Server.
solution: Experience Manager
title: Risoluzione dei problemi
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b80d3c9a-a0c4-4944-9f91-e791a072cd5f
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '522'
ht-degree: 0%

---

# Risoluzione dei problemi{#troubleshooting}

Questa sezione contiene soluzioni ai problemi che si sono verificati occasionalmente con Image Server.

**Generale**

ImageServer ora mantiene un registro di installazione e una cartella di backup di tutti i file modificati durante un&#39;installazione di aggiornamento. Il file e la cartella si trovano nella directory principale della directory di installazione di Image Server.

**All&#39;avvio del server immagini, lo script di avvio si arresta con il messaggio &quot;start pending&quot; (solo LINUX)**

Ciò potrebbe indicare un problema con la licenza Image Server, ad esempio un file di licenza mancante o una licenza temporanea scaduta. Un file di licenza valido deve trovarsi in [!DNL /usr/local/scene7/licenses].

**Il server immagini si arresta o si arresta in modo anomalo e il file di registro del server immagini indica che lo spazio o la risorsa non è temporaneamente disponibile nel file [!DNL IgcVirtualMemory.cpp]&quot;**

Il motivo di questo messaggio di errore è che Image Server non è riuscito ad allocare la quantità di memoria configurata per l&#39;utilizzo.

* Verificare l&#39;impostazione della memoria fisica in [!DNL ImageServerRegistry.xml]. Non dovrebbe essere superiore al 50%, in meno se nello stesso sistema sono in esecuzione altre applicazioni che richiedono un uso intensivo della memoria. Il valore predefinito è 20%.
* Verificare che lo spazio di swap sul server sia almeno doppio rispetto alla RAM fisica. Questo problema può essere causato da impostazioni di spazio di swap insufficiente.

**Lo spazio su disco effettivo utilizzato dalla cartella della cache supera ` *[!DNL cache.maxSize]*` impostato in[!DNL PlatformServer.conf]**

Questo non indica un problema. Il sovraccarico del file system non è incluso nell&#39;impostazione della cache del disco di [!DNL Platform Server]. L&#39;importo totale segnalato dal sistema può essere notevolmente superiore all&#39;impostazione. Si consiglia di riservare il doppio dello spazio su disco specificato in ` *[!DNL cache.maxSize]*`.

**Immagini interrotte negli esempi is-docs**

Ciò si verifica se Image Server non è in esecuzione. Si verifica anche se il percorso della directory principale del catalogo o il percorso della directory principale dell’immagine è stato modificato rispetto all’impostazione predefinita di installazione, ma le immagini e i cataloghi di esempio non sono stati spostati nelle nuove posizioni. Controlla il valore del percorso principale del server immagini nei file di configurazione. Se necessario, spostare la cartella demo contenente le immagini di esempio nella directory principale dell&#39;immagine corrente e spostare [!DNL sample*.*] nella directory principale del catalogo corrente.

Negli esempi si presuppone inoltre che alcune impostazioni in [!DNL default.ini] siano standard (ad esempio, l&#39;offuscamento o il blocco non devono essere abilitati).

**Troppi mancati riscontri nella cache dopo un tempo di attività significativo**

A seconda dell&#39;utilizzo del server, le prestazioni possono essere migliorate aumentando la dimensione della cache del disco di [!DNL Platform Server] se lo spazio su disco è disponibile. È possibile modificare le impostazioni modificando manualmente i file di configurazione. Consulta la documentazione.

**I file di registro occupano troppo spazio su disco**

Il server immagini e [!DNL Platform Server] avviano ogni giorno un nuovo file di registro. Per impostazione predefinita, questi sono inseriti in [!DNL *[!DNL install_root]*/ImageServer/logs]. È possibile configurare la dimensione del file di registro, il numero di registri conservati e il contenuto del registro. Consulta la documentazione.

**Se sul server è installato software antivirus**

È consigliabile disattivare la scansione delle directory Image Server. In caso contrario, la scansione di directory di lettura/scrittura di volumi elevati (come cache, immagini, font, profili e directory di catalogo) può causare problemi.

**Digimarc causa problemi di prestazioni per le immagini di zoom**

Non utilizzare Digimarc su immagini ingrandite. Le prestazioni non sono accettabili. Se necessario, crea un catalogo separato per le immagini da utilizzare per lo zoom e disattiva Digimarc per questo catalogo.
