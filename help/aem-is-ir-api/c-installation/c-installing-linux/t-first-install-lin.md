---
title: Prima installazione
description: Questa procedura mostra come installare Image Server per la prima volta su Linux®.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f27e6b27-641c-4a88-9ed0-94ada9ba75a9
source-git-commit: 3be1d948ac22f907169ef09b509f1cebceaec5c4
workflow-type: tm+mt
source-wordcount: '380'
ht-degree: 0%

---

# Prima installazione{#installing-for-the-first-time}

Questa procedura mostra come installare Image Server per la prima volta su Linux®.

1. Accedi all’host del server con autorizzazioni root.
1. Creare la cartella [!DNL /usr/local/scene7/licenses].

   Se il file della chiave di licenza di Image Server e/o Image Rendering (con [!DNL .sc8] file), copiarlo in questa cartella. In caso contrario, procedere con l&#39;installazione e installare il codice di licenza in un secondo momento.
1. Decomprimi e cancella il file tar di distribuzione di Image Server.
1. In [!DNL Setup] cartella, avviare l&#39;installazione guidata eseguendo [!DNL ./install-is].

   Se non viene trovata alcuna chiave di licenza, vengono visualizzate le istruzioni che descrivono come ottenere un file di licenza. Eseguire questa operazione o procedere con l&#39;installazione di Image Server e installare il codice di licenza in un secondo momento.
1. Quando viene visualizzato il Contratto di licenza con l&#39;utente finale (EULA), leggere il contratto di licenza e immettere `y` per procedere.

   Il programma di installazione visualizza i prompt elencati nella tabella seguente.

<table id="table_0E7B673CAD8E4C5EB72F8283A0DDEFC8"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Porta di ascolto principale [8080]:</span> </p> </td>
   <td colname="col2"> <p>Porta di ascolto HTTP principale per Image Server e Image Rendering. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Porta di ascolto amministratore [8083]:</span> </p> </td> 
   <td colname="col2"> <p>Porta di ascolto amministratore. </p> </td>
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Dimensione massima cache HTTP (MB) [2000]:</span> </p> </td> 
   <td colname="col2"> <p>Dimensione iniziale della cache di risposta principale. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> Cartella principale cache [/usr/local/scene7/ImageServing/cache]:</span> </p> </td> 
   <td colname="col2"> <p>Cartella cache PS. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID proprietario server immagini [root]:</span> </p> </td>
   <td colname="col2"> <p>Account utente in cui deve essere installato il server Image Server. </p> </td>
  </tr>
  <tr> 
   <td colname="col1"> <p><span class="codeph"> ID gruppo server immagini [root]:</span> </p> </td>
   <td colname="col2"> <p>Account di gruppo in cui deve essere installato il server Image Server. </p> </td>
  </tr>
 </tbody>
</table>

1. Premi **[!UICONTROL Invio]** per accettare il valore di default o specificare un valore diverso.

   Verificare che tutti i numeri di porta specificati siano univoci e non vengano utilizzati in altro modo in questo host.

   >[!IMPORTANT]
   >
   >Se si specifica un account diverso da root, è necessario assicurarsi che le autorizzazioni di accesso per tutti i file e le cartelle che il server immagini deve leggere e scrivere siano impostate correttamente quando tali cartelle vengono riconfigurate nei file di configurazione.
   >
   >Image Server è ora installato in [!DNL /usr/local/Scene7/ImageServing]. Alcuni contenuti di Image Rendering vengono installati in [!DNL /usr/local/Scene7/ImageRendering].
   >
   >Verso la fine dell&#39;installazione, l&#39;installazione guidata tenta di avviare Image Server. Se non viene trovata alcuna chiave di licenza valida, il server immagini non può avviarsi. Se è disponibile una licenza valida e Image Server non è ancora in fase di avvio, consultare i file di registro.

>[!NOTE]
>
>Se la licenza viene installata dopo l&#39;installazione di Image Server, quest&#39;ultimo deve essere avviato manualmente prima dell&#39;uso.
