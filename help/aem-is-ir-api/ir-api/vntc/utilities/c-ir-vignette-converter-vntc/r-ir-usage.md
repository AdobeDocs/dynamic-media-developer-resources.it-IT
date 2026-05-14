---
title: Utilizzo
description: In questo argomento viene descritta la sintassi di utilizzo vntc.
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: b892fe86-1b7c-4a49-a1cd-473f51d04d10
TQID: 'https://experienceleague.adobe.com/uNh-n1OEJ5gxWBjLbBNutrNJ1Osae-PEOFBmaKNVf6c'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 161
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

*[!DNL destFile]* è il percorso e il nome del file di vignettatura di output. Se non viene specificato, il file di output viene inserito nella cartella specificata con `-destpath`. In questo scenario, il nome del file viene generato automaticamente dal nome del file di input e da un suffisso di dimensione, separato dalla stringa specificata con `-separator`. Per le vignettature, il suffisso dimensione corrisponde alla larghezza in pixel della vignettatura di output a risoluzione singola, alla larghezza della prima visualizzazione di una vignettatura di output a più risoluzioni o a &#39;0&#39; se è presente una vignettatura piramidale. Per i file di stile cabinet, la risoluzione di output viene utilizzata come suffisso del file. *[!DNL destFile]* viene ignorato quando si specifica `-info`.
