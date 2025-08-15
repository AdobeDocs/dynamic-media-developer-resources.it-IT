---
title: Aggiornamento da IS 4.7.4 o versione successiva
description: Segui questa procedura per aggiornare Dynamic Media Image Server su Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 0%

---

# Aggiornamento da IS 4.7.4 o versione successiva{#updating-from-is-or-later}

Segui questa procedura per aggiornare Dynamic Media Image Server su Linux®.

Se stai effettuando l’aggiornamento da una versione precedente di Image Server, contatta il supporto per la procedura corretta.

È possibile eliminare la cartella [!DNL webapps] durante l&#39;aggiornamento. Eseguire il backup della cartella [!DNL webapps] prima dell&#39;aggiornamento.

1. Accedi all’host del server con privilegi di root.
1. Decomprimi e cancella il file tar di distribuzione di Image Server.
1. Nella cartella [!DNL setup], eseguire [!DNL `./install-is`] per avviare l&#39;installazione guidata.

   Il programma di installazione dell&#39;aggiornamento controlla l&#39;integrità e la versione del pacchetto installato. In caso di esito positivo, viene visualizzato il Contratto di licenza con l&#39;utente finale (&quot;EULA&quot;).
1. Leggere il contratto di licenza e immettere **[!UICONTROL y]** per continuare l&#39;installazione.

   Il programma di installazione esegue il backup dei vecchi file di configurazione del server nella cartella [!DNL BACKUP/].

   Al termine dell’installazione viene visualizzato il seguente messaggio:

   `Image Server was started successfully`

Durante un aggiornamento, il file [!DNL ImageServing/conf/server.xml] viene aggiornato alle impostazioni più recenti. Se hai modificato o aggiunto dei valori, salva [!DNL server.xml] esistente e reimplementa le modifiche dopo l&#39;aggiornamento.

Dopo un’installazione di aggiornamento, considera di riscaldare la cache di risposta HTTP prima di attivare il server. Per ulteriori informazioni, vedere la descrizione dell&#39;utilità [!DNL playlog].
