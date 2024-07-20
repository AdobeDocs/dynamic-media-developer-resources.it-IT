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
1. Avviare l&#39;installazione guidata eseguendo [!DNL setup]/ [!DNL setup.exe].
1. Selezionare **[!UICONTROL Avanti]** per passare al contratto di licenza con l&#39;utente finale, leggere il contratto di licenza e selezionare **[!UICONTROL Sì]**.

   Verrà visualizzata la finestra di dialogo [!DNL Authentication].
1. Se una licenza è già installata e le informazioni sulla licenza vengono visualizzate nella finestra di dialogo [!DNL Authentication], selezionare **[!UICONTROL Avanti]** per continuare.

   Se non si dispone di una licenza, selezionare **[!UICONTROL Richiedi licenza]**. Nella finestra di dialogo successiva viene visualizzato uno degli indirizzi MAC della scheda di interfaccia di rete del computer. Inviate un&#39;e-mail a questo indirizzo MAC, al nome della vostra società e al prodotto che state installando come indicato dal prompt.

   **Importante:** la licenza si basa sull&#39;indirizzo MAC di una delle schede di interfaccia di rete installate nell&#39;host. Se si disattiva, rimuove o sostituisce questa scheda, la licenza non verrà più riconosciuta come valida. Assicurati di ottenere una licenza per la configurazione hardware utilizzata per Image Server.

   È possibile continuare a installare IS senza una licenza valida e installare la licenza in un secondo momento. Per continuare, selezionare **[!UICONTROL Indietro]** per tornare alla finestra di dialogo [!DNL Authentication], quindi selezionare **[!UICONTROL Avanti]**.
1. Passare alla pagina &quot;[!DNL Platform Server] Impostazioni amministratore&quot;. Immettete nuovi valori in base alle esigenze o accettate i valori predefiniti.

   Puoi configurare i seguenti elementi:

   <table id="table_AA5D7674BBBE4AD4B373066AEF413FFD"> 
   <tbody> 
   <tr> 
      <td> <p> Porta di connessione HTTP [!DNL Platform Server] </p> </td>
      <td> <p>Porta di ascolto HTTP principale per Image Server e Image Rendering </p> </td>
   </tr> 
   <tr> 
      <td> <p> Admin Listening Port </p> </td>
      <td> <p>Admin Listening Port </p> </td>
   </tr> 
   <tr> 
      <td> <p> [!DNL Platform Server] dimensioni cache in MB </p> </td>
      <td> <p>Dimensione iniziale della cache di risposta principale </p> </td>
   </tr>
   <tr> 
      <td> <p> Percorso cache [!DNL Platform Server] </p> </td>
      <td> <p>Cartella cache PS </p> </td>
   </tr>
   </tbody>
   </table>

   I numeri di porta specificati devono essere univoci e non devono essere utilizzati da altre applicazioni o servizi.

   Nella schermata successiva è possibile rivedere le impostazioni selezionate.

1. Seleziona **[!UICONTROL Indietro]** per apportare modifiche, oppure seleziona **[!UICONTROL Avanti]** per avviare l&#39;installazione.

1. Selezionare **[!UICONTROL Fine]** per uscire dall&#39;installazione guidata.
