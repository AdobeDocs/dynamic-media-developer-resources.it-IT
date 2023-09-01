---
title: Utilizzo
description: In questo argomento viene descritta la sintassi di utilizzo vntc.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---

# Utilizzo{#usage}

In questo argomento viene descritta la sintassi di utilizzo vntc.

`vntc [ *[!DNL options]*] *[!DNL sourceFile]* [ *[!DNL destFile]*]`

*[!DNL sourceFile]* è il percorso e il nome del file da elaborare. Può essere un percorso relativo alla directory di lavoro corrente o un percorso assoluto. Deve essere un file di stile di vignettatura, uno stile di archivio o una finestra valida e deve avere uno dei seguenti suffissi:

* [!DNL .vnt]
* [!DNL .vnc]
* [!DNL .vnw]

Obbligatorio.

*[!DNL destFile]* è il percorso e il nome del file di vignettatura di output. Se non viene specificato, il file di output viene inserito nella cartella specificata con `-destpath`. In questo scenario, il nome del file viene generato automaticamente dal nome del file di input e da un suffisso di dimensione, separato dalla stringa specificata con `-separator`. Per le vignettature, il suffisso dimensione corrisponde alla larghezza in pixel della vignettatura di output a risoluzione singola, alla larghezza della prima visualizzazione di una vignettatura di output a più risoluzioni o a &#39;0&#39; se è presente una vignettatura piramidale. Per i file di stile cabinet, la risoluzione di output viene utilizzata come suffisso del file. *[!DNL destFile]* viene ignorato quando `-info` è specificato.
