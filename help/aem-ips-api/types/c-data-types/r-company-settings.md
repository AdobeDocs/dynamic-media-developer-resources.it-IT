---
description: Impostazioni di configurazione specifiche per l’azienda.
solution: Experience Manager
title: ImpostazioniSocietà
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 1%

---

# [!DNL CompanySettings]{#companysettings}

Impostazioni di configurazione specifiche per l’azienda.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| overwriteMode | `xsd:string` | Determina se sovrascrivere le immagini nella cartella corrente con lo stesso nome immagine di base e la stessa estensione. |
| keepPublishState | `xsd:boolean` | Specifica se un&#39;immagine sostitutiva caricata in IPS deve mantenere l&#39;impostazione &quot;Pronto per la pubblicazione&quot; esistente o deve corrispondere a quella specificata per il caricamento. |
| defaultSourceProfile | `types:Asset` | Specifica il profilo colore di origine predefinito (Coated FOGRA27 (ISO 126472:2004)) applicato automaticamente come parte del comando &quot;Usa comportamento colore predefinito&quot; quando si aggiungono file CMYK di immagini. |
| defaultDisplayProfile | `types:Asset` | Specifica il profilo colore interno predefinito (SWOP (U.S. Web Coated) v2) applicato automaticamente come parte del comando &quot;Usa comportamento colore predefinito&quot; quando si aggiungono file CMYK di immagini. |
| iptcExifMappingXslt | `types:Asset` | L&#39;estrazione di dati di intestazione immagine IPTC ed EXIF in IPS richiede una conversione dai nomi di campi interni ai nomi di campi definiti dall&#39;utente per la società. Determina una tabella di traduzione XSL (l&#39;impostazione predefinita è &quot;Non estrarre alcun campo IPTC o EXIF&quot;) per le immagini caricate. |
| xmpMappingXslt | `types:Asset` | L’estrazione di dati di intestazione immagine XMP in IPS richiede una conversione dai nomi di campi interni ai nomi di campi definiti dall’utente per l’azienda. Determina una tabella di traduzione XSL (l&#39;impostazione predefinita è &quot;Non estrarre campi XMP&quot;) per le immagini caricate. |
| diskSpaceWarningMin | `xsd:int` | Quantità minima di spazio libero su disco nella directory delle immagini prima dell&#39;invio di un avviso. |
| emailTrashCleanupWarning | `xsd:boolean` | Determina se inviare e-mail prima dell&#39;eliminazione automatica degli elementi del cestino. |
| javascriptUploadEnabled | `types:Asset` | Determina se caricare i file JavaScript. Questa opzione rappresenta un potenziale rischio per la sicurezza, pertanto utilizza con cautela. |
