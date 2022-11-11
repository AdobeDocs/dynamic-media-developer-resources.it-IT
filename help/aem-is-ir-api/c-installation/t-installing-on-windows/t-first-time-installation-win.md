---
title: Installazione per la prima volta
description: Utilizzare questi passaggi per installare Image Server per la prima volta su Windows.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Installazione per la prima volta{#installing-for-the-first-time}

Utilizzare questi passaggi per installare Image Server per la prima volta su Windows.

1. Accedi all&#39;host del server con privilegi amministrativi.
1. Se hai già ricevuto una licenza, copiala sul tuo server, quindi esegui l&#39;installazione della licenza facendo doppio clic sul file.

   Se non si dispone ancora di una licenza, è possibile procedere con l&#39;installazione e installare la licenza in un secondo momento.

1. Estrarre il contenuto del file zip di distribuzione Image Serving.
1. Avvia l&#39;installazione guidata, eseguendo [!DNL setup]/ [!DNL setup.exe].
1. Seleziona **[!UICONTROL Successivo]** per avanzare al contratto di licenza con l’utente finale (EULA), leggere il contratto di licenza e selezionare **[!UICONTROL Sì]**.

   La [!DNL Authentication] viene visualizzata la finestra di dialogo successiva.
1. Se una licenza è già installata e le informazioni sulla licenza vengono visualizzate nella [!DNL Authentication] finestra di dialogo, seleziona **[!UICONTROL Successivo]** per continuare.

   Se non si dispone di una licenza, selezionare **[!UICONTROL Richiedi licenza]**. Nella finestra di dialogo successiva viene visualizzato uno degli indirizzi MAC della scheda di interfaccia di rete del computer. Invia un&#39;e-mail a questo indirizzo MAC, al nome dell&#39;azienda e al prodotto da installare come indicato dal prompt.

   **Importante:** La licenza si basa sull&#39;indirizzo MAC di una delle schede di interfaccia di rete installate su questo host. Se disattivi, rimuovi o sostituisci questa scheda, la licenza non viene più riconosciuta come valida. Assicurati di ottenere una licenza per la configurazione hardware utilizzata per Image Serving.

   È possibile continuare a installare IS senza una licenza valida e installare la licenza in un secondo momento. Per continuare, seleziona **[!UICONTROL Indietro]** per tornare al [!DNL Authentication] finestra di dialogo, quindi selezionare **[!UICONTROL Successivo]**.
1. Procedi al &quot;[!DNL Platform Server] Impostazioni amministratore&quot;. Immetti i nuovi valori desiderati oppure accetta i valori predefiniti.

   Puoi configurare i seguenti elementi:

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] Porta di connessione HTTP </p> </td>
      <td> <p>Porta di ascolto HTTP principale per Image Server e Image Rendering </p> </td>
   </tr> 
   <tr> 
      <td> <p> Porta di ascolto amministratore </p> </td>
      <td> <p>Porta di ascolto amministratore </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server] Dimensioni cache in MB </p> </td>
      <td> <p>Dimensione iniziale della cache di risposta principale </p> </td>
   </tr>
   <tr> 
      <td> <p> [!DNL Platform Server] Posizione cache </p> </td>
      <td> <p>Cartella cache PS </p> </td>
   </tr>
   </tbody>
   </table>

   I numeri di porta specificati devono essere univoci e non devono essere utilizzati da altre applicazioni o servizi.

   La schermata successiva offre l’opportunità di rivedere le impostazioni selezionate.

1. Seleziona **[!UICONTROL Indietro]** per apportare modifiche, oppure seleziona **[!UICONTROL Successivo]** per avviare l&#39;installazione.

1. Seleziona **[!UICONTROL Fine]** per uscire dalla procedura guidata di installazione.
