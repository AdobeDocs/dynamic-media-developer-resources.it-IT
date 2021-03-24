---
description: Questa sezione contiene soluzioni ai problemi che si sono verificati occasionalmente con Image Serving.
solution: Experience Manager
title: Risoluzione dei problemi
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 1%

---


# Risoluzione dei problemi{#troubleshooting}

Questa sezione contiene soluzioni ai problemi che si sono verificati occasionalmente con Image Serving.

**Generali**

ImageServer ora mantiene un registro di installazione e una cartella di backup di tutti i file modificati durante un&#39;installazione di aggiornamento. Questo file e questa cartella si trovano nella directory principale della directory di installazione di Image Server.

**Quando si avvia il server di immagini, lo script di avvio si arresta con il messaggio &quot;start pending&quot; (in attesa) (solo LINUX)**

Questo può indicare un problema con la Licenza Image Serving, ad esempio un file di licenza mancante o una licenza temporanea scaduta. Un file di licenza valido deve trovarsi in [!DNL /usr/local/scene7/licenses].

**Image Server si blocca o si blocca e il file di registro Image Server indica spazio insufficiente o &quot;risorsa temporaneamente non disponibile nel file  [!DNL IgcVirtualMemory.cpp]&quot;**

Il motivo di questo messaggio di errore è che Image Server non è in grado di allocare la quantità di memoria configurata per l&#39;utilizzo.

* Controllare l&#39;impostazione Memoria fisica in [!DNL ImageServerRegistry.xml]. Non dovrebbe superare il 50%, meno se altre applicazioni a uso intensivo di memoria sono in esecuzione sullo stesso sistema. Il valore predefinito è 20%.
* Assicurati che lo spazio di scambio sul server sia almeno doppio della dimensione della RAM fisica. Questo problema può essere causato da basse impostazioni dello spazio di scambio.

**Lo spazio su disco effettivo utilizzato dalla cartella cache supera  ` *[!DNL cache.maxSize]*`l&#39;impostazione in[!DNL PlatformServer.conf]**

Questo non indica un problema. Il sovraccarico del file system non è incluso nell&#39;impostazione della cache del disco di Platform Server. L&#39;importo totale segnalato dal sistema può essere notevolmente superiore all&#39;impostazione. Si consiglia di riservare il doppio dello spazio su disco specificato in ` *[!DNL cache.maxSize]*`.

**Immagini interrotte negli esempi is-docs**

Ciò si verifica se Image Server non è in esecuzione. Si verifica anche se il percorso principale del catalogo o il percorso principale dell’immagine è stato modificato rispetto al valore predefinito di installazione, ma le immagini e i cataloghi di esempio non sono stati spostati nelle nuove posizioni. Controlla il valore del percorso principale del server immagini nei file di configurazione. Se necessario, sposta la cartella demo contenente le immagini di esempio nella directory principale dell&#39;immagine corrente e sposta [!DNL sample*.*] nella directory principale del catalogo corrente.

Gli esempi presuppongono inoltre che alcune impostazioni in [!DNL default.ini] siano standard (ad esempio, l&#39;offuscamento o il blocco non devono essere attivati).

**Troppe mancate cache dopo un notevole tempo di attività**

A seconda dell’utilizzo del server, le prestazioni possono essere migliorate aumentando la dimensione della cache del disco del server Platform se è disponibile spazio su disco. Le impostazioni possono essere modificate manualmente modificando i file di configurazione. Consulta la documentazione .

**I file di registro occupano troppo spazio su disco**

Image Server e Platform Server avviano ogni giorno un nuovo file di registro. Per impostazione predefinita questi vengono inseriti in [!DNL *[!DNL install_root]*/ImageServing/logs]. È possibile configurare la dimensione del file di registro, il numero di registri conservati e il contenuto del registro. Consulta la documentazione .

**Se sul server è installato un software antivirus**

Si consiglia di disattivare la scansione per le directory Image Serving. In caso contrario, la scansione di directory di lettura/scrittura a volume elevato (come cache, immagini, font, profili e directory di catalogo) causerà problemi.

**Digimarc causa problemi di prestazioni per le immagini zoom**

Non utilizzare Digimarc sulle immagini che verranno ingrandite. Le prestazioni non saranno accettabili. Se necessario, crea un catalogo separato per le immagini da utilizzare per lo zoom e disabilita Digimarc per questo catalogo.
