---
description: Questa sezione contiene soluzioni ai problemi che si sono verificati occasionalmente con Image Server.
seo-description: Questa sezione contiene soluzioni ai problemi che si sono verificati occasionalmente con Image Server.
seo-title: Risoluzione dei problemi
solution: Experience Manager
title: Risoluzione dei problemi
topic: Scene7 Image Serving - Image Rendering API
uuid: 39fdaf86-004b-4553-bde0-0367f3ef76b8
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 1%

---


# Risoluzione dei problemi{#troubleshooting}

Questa sezione contiene soluzioni ai problemi che si sono verificati occasionalmente con Image Server.

**Generali**

ImageServer ora conserva un registro di installazione e una cartella di backup di tutti i file modificati durante un&#39;installazione di aggiornamento. Questo file e questa cartella si trovano nella directory principale della directory di installazione di Image Server.

**Quando si avvia il server immagini, lo script di avvio si blocca con il messaggio &quot;start pending&quot; (Avvia in sospeso) (solo LINUX)**

Questo può indicare un problema con la licenza Image Server, ad esempio un file di licenza mancante o una licenza temporanea scaduta. Un file di licenza valido deve trovarsi in [!DNL /usr/local/scene7/licenses].

**Image Server blocca o si chiude inaspettatamente e il file di registro Image Server indica spazio insufficiente o &quot;la risorsa temporaneamente non è disponibile nel file  [!DNL IgcVirtualMemory.cpp]&quot;**

Il motivo di questo messaggio di errore è che Image Server non è in grado di allocare la quantità di memoria configurata per l’utilizzo.

* Controllare l&#39;impostazione Memoria fisica in [!DNL ImageServerRegistry.xml]. Non deve superare il 50%, meno se altre applicazioni che richiedono molta memoria sono in esecuzione sullo stesso sistema. Il valore predefinito è 20%.
* Accertatevi che lo spazio di scambio sul server sia almeno doppio della dimensione della RAM fisica. Questo problema può essere causato da impostazioni di spazio di scambio basso.

**Lo spazio su disco effettivo utilizzato dalla cartella della cache supera il  ` *[!DNL cache.maxSize]*`valore impostato in[!DNL PlatformServer.conf]**

Ciò non indica un problema. Il sovraccarico del file system non è incluso nell&#39;impostazione della cache del disco del server della piattaforma. L&#39;importo totale segnalato dal sistema può essere notevolmente superiore all&#39;impostazione. Si consiglia di riservare il doppio dello spazio su disco specificato in ` *[!DNL cache.maxSize]*`.

**Immagini interrotte negli esempi is-docs**

Ciò si verifica se Image Server non è in esecuzione. Si verifica anche se il percorso principale del catalogo o il percorso principale dell’immagine è stato modificato rispetto al percorso predefinito di installazione, ma le immagini e i cataloghi di esempio non sono stati spostati nelle nuove posizioni. Controllate il valore del percorso principale del server immagini nei file di configurazione. Se necessario, spostate la cartella demo che contiene le immagini di esempio nella directory principale dell&#39;immagine corrente e [!DNL sample*.*] nella directory principale del catalogo corrente.

Gli esempi presuppongono inoltre che alcune impostazioni in [!DNL default.ini] siano standard (ad esempio, l&#39;offuscamento o il blocco non devono essere attivati).

**Troppi problemi di cache dopo un notevole tempo di inattività**

A seconda dell&#39;utilizzo del server, le prestazioni possono essere migliorate aumentando la dimensione della cache del disco del server della piattaforma se è disponibile spazio su disco. Le impostazioni possono essere modificate modificando manualmente i file di configurazione. Consulta la documentazione.

**I file di registro occupano troppo spazio su disco**

Image Server e Platform Server avviano ogni giorno un nuovo file di registro. Per impostazione predefinita, questi vengono inseriti in [!DNL *[!DNL install_root]*/ImageServing/logs]. È possibile configurare la dimensione del file di registro, il numero di file di registro conservati e il contenuto del registro. Consulta la documentazione.

**Se sul server è installato un software antivirus**

È consigliabile disattivare la scansione per le directory Image Server. In caso contrario, la scansione di directory di lettura/scrittura a volume elevato (come cache, immagini, font, profili e directory di catalogo) causerà problemi.

**Digimarc causa problemi di prestazioni per le immagini di zoom**

Non utilizzate Digimarc sulle immagini con zoom. Le prestazioni non saranno accettabili. Se necessario, create un catalogo separato per le immagini da utilizzare per lo zoom e disattivate Digimarc per questo catalogo.
