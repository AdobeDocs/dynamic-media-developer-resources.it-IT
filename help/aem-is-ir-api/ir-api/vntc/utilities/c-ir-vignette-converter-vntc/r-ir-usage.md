---
description: In questo argomento viene descritta la sintassi di utilizzo vntc.
seo-description: In questo argomento viene descritta la sintassi di utilizzo vntc.
seo-title: Utilizzo
solution: Experience Manager
title: Utilizzo
topic: Scene7 Image Serving - Image Rendering API
uuid: 251aa1a0-5f19-42ab-b237-3e3b53fe8320
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 2%

---


# Utilizzo{#usage}

In questo argomento viene descritta la sintassi di utilizzo vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* è il percorso e il nome del file da elaborare. Può essere un percorso relativo alla directory di lavoro corrente o un percorso assoluto. Deve essere un file di stile valido per la vignettatura, lo stile del cabinet o la finestra e deve avere uno dei seguenti suffissi: [!DNL .vnt], [!DNL .vnc] o [!DNL .vnw]. Obbligatorio.

*[!DNL destFile]* è il percorso e il nome del file di vignettatura di output. Se non viene specificato, il file di output viene inserito nella cartella specificata con `-destpath`. In questo scenario, il nome del file viene generato automaticamente dal nome del file di input e da un suffisso di dimensione, separati dalla stringa specificata con `-separator`. Per le vignettature, il suffisso delle dimensioni è la larghezza in pixel della vignettatura di output a risoluzione singola, la larghezza della prima visualizzazione di una vignettatura di output a risoluzione multipla o &#39;0&#39; nel caso di una vignettatura a piramide. Per i file di stile dell&#39;archivio, la risoluzione di output viene utilizzata come suffisso del file. *[!DNL destFile]* viene ignorato quando  `-info` viene specificato.
