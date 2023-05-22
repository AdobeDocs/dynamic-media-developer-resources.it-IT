---
title: Prima installazione
description: Per installare Image Server per la prima volta in Windows, segui la procedura riportata di seguito.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 4e34d78c-1b5b-45cf-acc5-ff12cbc6ed01
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '366'
ht-degree: 0%

---

# Prima installazione{#installing-for-the-first-time}

Per installare Image Server per la prima volta in Windows, segui la procedura riportata di seguito.

1. Accedi all’host del server con privilegi di amministratore.
1. Se è già stata ricevuta una licenza, copiarla sul server, quindi eseguire l&#39;installazione della licenza facendo doppio clic sul file.

   Se non si dispone ancora di una licenza, è possibile procedere con l&#39;installazione e installare la licenza in un secondo momento.

1. Estrai il contenuto del file zip di distribuzione di Image Server.
1. Avvia l&#39;installazione guidata eseguendo [!DNL setup]/ [!DNL setup.exe].
1. Seleziona **[!UICONTROL Successivo]** per passare al Contratto di licenza con l&#39;utente finale (EULA), leggere il contratto di licenza e selezionare **[!UICONTROL Sì]**.

   Il [!DNL Authentication] viene visualizzata la finestra di dialogo successiva.
1. Se una licenza è già installata e le informazioni sulla licenza vengono visualizzate nella [!DNL Authentication] finestra di dialogo, seleziona **[!UICONTROL Successivo]** per continuare.

   Se non si dispone di una licenza, selezionare **[!UICONTROL Richiedi licenza]**. Nella finestra di dialogo successiva viene visualizzato uno degli indirizzi MAC della scheda di interfaccia di rete del computer. Inviate un&#39;e-mail a questo indirizzo MAC, al nome della vostra società e al prodotto che state installando come indicato dal prompt.

   **Importante:** La licenza si basa sull&#39;indirizzo MAC di una delle schede di interfaccia di rete installate nell&#39;host. Se si disattiva, rimuove o sostituisce questa scheda, la licenza non verrà più riconosciuta come valida. Assicurati di ottenere una licenza per la configurazione hardware utilizzata per Image Server.

   È possibile continuare a installare IS senza una licenza valida e installare la licenza in un secondo momento. Per procedere, seleziona **[!UICONTROL Indietro]** per tornare al [!DNL Authentication] e quindi selezionare **[!UICONTROL Successivo]**.
1. Procedi a &quot;[!DNL Platform Server] Admin Settings&quot;. Immettete nuovi valori in base alle esigenze o accettate i valori predefiniti.

   Puoi configurare i seguenti elementi:

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> [!DNL Platform Server] Porta di connessione HTTP </p> </td>
      <td> <p>Porta di ascolto HTTP principale per Image Server e Image Rendering </p> </td>
   </tr> 
   <tr> 
      <td> <p> Admin Listening Port </p> </td>
      <td> <p>Admin Listening Port </p> </td>
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

   Nella schermata successiva è possibile rivedere le impostazioni selezionate.

1. Seleziona **[!UICONTROL Indietro]** per apportare modifiche o selezionare **[!UICONTROL Successivo]** per avviare l&#39;installazione.

1. Seleziona **[!UICONTROL Fine]** per uscire dall&#39;installazione guidata.
