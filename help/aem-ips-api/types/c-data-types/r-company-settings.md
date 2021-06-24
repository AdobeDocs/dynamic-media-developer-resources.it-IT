---
description: Impostazioni di configurazione specifiche per azienda.
solution: Experience Manager
title: ImpostazioniSocietà
feature: Dynamic Media Classic, SDK/API
role: Developer,Administrator
exl-id: 82e6362d-beab-47ff-bb20-11047f0d8787
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 1%

---

# ImpostazioniSocietà{#companysettings}

Impostazioni di configurazione specifiche per azienda.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| `*`overwriteMode`*` | `xsd:string` | Determina se sovrascrivere le immagini nella cartella corrente con lo stesso nome e estensione dell&#39;immagine di base. |
| `*`keepPublishState`*` | `xsd:boolean` | Specifica se un&#39;immagine sostitutiva caricata in IPS deve mantenere l&#39;impostazione &quot;Ready to Publish&quot; esistente o se deve essere come specificato dal caricamento. |
| `*`defaultSourceProfile`*` | `types:Asset` | Specifica il profilo colore sorgente predefinito (Coated FOGRA27 (ISO 126472:2004)) applicato automaticamente come parte del &quot;Use default Color Behavior&quot; (Usa comportamento colore predefinito) quando si aggiungono file immagine CMYK. |
| `*`defaultDisplayProfile`*` | `types:Asset` | Specifica il profilo colore interno predefinito (SWOP, US Web Coated) v2) applicato automaticamente come parte del &quot;Use default Color Behavior&quot; (Usa comportamento colore predefinito) quando si aggiungono file immagine CMYK. |
| `*`iptcExifMappingXslt`*` | `types:Asset` | L’estrazione dei dati di intestazione immagine IPTC e EXIF in IPS richiede una conversione dai nomi di campo interni ai nomi di campo definiti dall’utente per l’azienda. Determina una tabella di traduzione XSL (l&#39;impostazione predefinita è &quot;Non estrarre campi IPTC o EXIF&quot;) per le immagini caricate. |
| `*`xmpMappingXslt`*` | `types:Asset` | L’estrazione XMP dati di intestazione immagine in IPS richiede una conversione dai nomi di campo interni ai nomi di campo definiti dall’utente per l’azienda. Determina una tabella di traduzione XSL (l’impostazione predefinita è &quot;Non estrarre campi XMP&quot;) per le immagini caricate. |
| `*`diskSpaceWarningMin`*` | `xsd:int` | Quantità minima di spazio libero su disco della directory dell&#39;immagine prima dell&#39;invio di un avviso. |
| `*`emailTrashCleanupWarning`*` | `xsd:boolean` | Determina se inviare e-mail prima che gli elementi inseriti nel cestino possano essere eliminati automaticamente. |
| `*`javascriptUploadEnabled`*` | `types:Asset` | Determina se caricare i file JavaScript. Questo è un potenziale rischio per la sicurezza, quindi utilizza questa opzione con attenzione. |
