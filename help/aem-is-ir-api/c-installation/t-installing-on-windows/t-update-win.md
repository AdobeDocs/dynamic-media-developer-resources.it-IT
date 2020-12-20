---
description: Utilizzate questa procedura per aggiornare Scene7 Image Server.
seo-description: Utilizzate questa procedura per aggiornare Scene7 Image Server.
seo-title: Aggiornamento da IS 4.7.4 o successivo
solution: Experience Manager
title: Aggiornamento da IS 4.7.4 o successivo
topic: Scene7 Image Serving - Image Rendering API
uuid: 3d23f13a-a9be-45ff-9765-c71bdeb77c5f
translation-type: tm+mt
source-git-commit: edb21832b3e36a6498c6aad27813cd4b3032b48f
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 0%

---


# Aggiornamento da IS 4.7.4 o successivo{#updating-from-is-or-later}

Utilizzate questa procedura per aggiornare Scene7 Image Server.

Se state effettuando l’aggiornamento da una versione precedente di Image Server, contattate il supporto per il processo corretto.

>[!NOTE]
>
>La cartella [!DNL webapps] potrebbe essere eliminata al momento dell&#39;aggiornamento. Esegui il backup della cartella [!DNL webapps] prima dell&#39;aggiornamento.

1. Accedete all&#39;host del server con privilegi amministrativi.
1. Estrarre il contenuto del file zip di distribuzione Image Server.
1. Per avviare la procedura guidata di installazione, eseguite setup/setup.exe.
1. Fare clic su **[!UICONTROL Next]** per avanzare al contratto di licenza per l&#39;utente finale (EULA), leggere il contratto di licenza e fare clic su **[!UICONTROL Yes]**.

   Nella pagina successiva vengono visualizzate le impostazioni di configurazione precedenti.
1. Fare clic su **[!UICONTROL Next]** per avviare l&#39;installazione dell&#39;aggiornamento.

   >[!NOTE]
   >
   >Il programma di installazione esegue il backup dei vecchi file di configurazione del server nella cartella [!DNL BACKUP/].

1. Al termine dell&#39;installazione, fare clic su &quot;Fine&quot; per uscire dalla procedura guidata di installazione.

   In alcuni casi, la procedura guidata di installazione potrebbe richiedere il riavvio del sistema.

Durante un aggiornamento, il file [!DNL ImageServing/conf/server.xml] viene aggiornato alle impostazioni più recenti. Se hai modificato o aggiunto dei valori, devi salvare la [!DNL server.xml] esistente e riimplementare le modifiche dopo l&#39;aggiornamento.

Dopo un&#39;installazione di aggiornamento, prendete in considerazione il riscaldamento della cache delle risposte HTTP prima di rendere attivo il server. Per ulteriori informazioni, fare riferimento alla descrizione dell&#39;utility `playlog`.
