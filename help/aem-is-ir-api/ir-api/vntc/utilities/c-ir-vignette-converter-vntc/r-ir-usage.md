---
description: Questo argomento descrive la sintassi di utilizzo vntc.
solution: Experience Manager
title: Utilizzo
feature: Dynamic Media Classic, SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 1%

---

# Utilizzo{#usage}

Questo argomento descrive la sintassi di utilizzo vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* è il percorso e il nome del file da elaborare. Può essere un percorso relativo alla directory di lavoro corrente o un percorso assoluto. Deve essere una vignetta, uno stile di archivio o una finestra valida per il file di stile e deve avere uno dei seguenti suffissi: [!DNL .vnt], [!DNL .vnc] o [!DNL .vnw]. Obbligatorio.

*[!DNL destFile]* è il percorso e il nome del file della vignetta di output. Se non viene specificato, il file di output viene posizionato nella cartella specificata con `-destpath`. In questo scenario, il nome del file viene generato automaticamente dal nome del file di input e da un suffisso di dimensione, separati dalla stringa specificata con `-separator`. Per le vignette, il suffisso di dimensione è la larghezza in pixel della vignetta di output a risoluzione singola, la larghezza della prima vista di una vignetta di output a risoluzione multipla o &quot;0&quot; in caso di una vignetta a piramide. Per i file di stile cabinet, la risoluzione di output viene utilizzata come suffisso di file. *[!DNL destFile]* viene ignorato quando  `-info` viene specificato.
