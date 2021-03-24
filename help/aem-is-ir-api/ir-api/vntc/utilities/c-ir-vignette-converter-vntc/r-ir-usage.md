---
description: Questo argomento descrive la sintassi di utilizzo vntc.
solution: Experience Manager
title: Utilizzo
feature: Dynamic Media Classic, SDK/API
role: Sviluppatore, Business Practices
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 1%

---


# Utilizzo{#usage}

Questo argomento descrive la sintassi di utilizzo vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* è il percorso e il nome del file da elaborare. Può essere un percorso relativo alla directory di lavoro corrente o un percorso assoluto. Deve essere una vignetta, uno stile di archivio o una finestra valida per il file di stile e deve avere uno dei seguenti suffissi: [!DNL .vnt], [!DNL .vnc] o [!DNL .vnw]. Obbligatorio.

*[!DNL destFile]* è il percorso e il nome del file della vignetta di output. Se non viene specificato, il file di output viene posizionato nella cartella specificata con `-destpath`. In questo scenario, il nome del file viene generato automaticamente dal nome del file di input e da un suffisso di dimensione, separati dalla stringa specificata con `-separator`. Per le vignette, il suffisso di dimensione è la larghezza in pixel della vignetta di output a risoluzione singola, la larghezza della prima vista di una vignetta di output a risoluzione multipla o &quot;0&quot; in caso di una vignetta a piramide. Per i file di stile cabinet, la risoluzione di output viene utilizzata come suffisso di file. *[!DNL destFile]* viene ignorato quando  `-info` viene specificato.
