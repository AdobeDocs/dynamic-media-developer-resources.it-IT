---
title: Aggiornamento da IS 4.7.4 o successivo
description: Utilizzare questa procedura per aggiornare Dynamic Media Image Serving su Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 54733fcc-c4e3-4501-8a3d-000778678bdb
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Aggiornamento da IS 4.7.4 o successivo{#updating-from-is-or-later}

Utilizzare questa procedura per aggiornare Dynamic Media Image Serving su Linux®.

Se stai eseguendo l&#39;aggiornamento da una versione precedente di Image Serving, contatta il supporto per il processo corretto.

La [!DNL webapps] La cartella può essere eliminata al momento dell’aggiornamento. Esegui il backup [!DNL webapps] prima dell’aggiornamento.

1. Accedi all&#39;host del server con privilegi di root.
1. Decomprimi e cancella il file tar di distribuzione Image Serving.
1. In [!DNL setup] cartella, eseguire [!DNL `./install-is`] per avviare l&#39;installazione guidata.

   Il programma di installazione dell&#39;aggiornamento verifica l&#39;integrità e la versione del pacchetto installato. In caso di esito positivo, viene visualizzato il contratto di licenza con l’utente finale (&quot;EULA&quot;).
1. Leggere il contratto di licenza e quindi immettere **[!UICONTROL y]** per procedere con l&#39;installazione.

   Il programma di installazione esegue il backup dei vecchi file di configurazione del server nel [!DNL BACKUP/] cartella.

   Al termine dell’installazione, viene visualizzato il seguente messaggio:

   `Image Server was started successfully`

Durante un aggiornamento, il [!DNL ImageServing/conf/server.xml] viene aggiornato alle impostazioni più recenti. Se hai modificato o aggiunto dei valori, salva i valori esistenti [!DNL server.xml] e reimplementare le modifiche dopo l&#39;aggiornamento.

Dopo un&#39;installazione di aggiornamento, considera il riscaldamento della cache di risposta HTTP prima di avviare il server. Fai riferimento alla descrizione del [!DNL playlog] utilità per i dettagli.
