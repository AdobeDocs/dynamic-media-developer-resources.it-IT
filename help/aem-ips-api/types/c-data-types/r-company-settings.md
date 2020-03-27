---
description: Impostazioni di configurazione specifiche per la società.
seo-description: Impostazioni di configurazione specifiche per la società.
seo-title: CompanySettings
solution: Experience Manager
title: CompanySettings
topic: Scene7 Image Production System API
uuid: a807d5c1-058d-4313-b4f8-6ee203284003
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# CompanySettings{#companysettings}

Impostazioni di configurazione specifiche per la società.

Sintassi

## Parametri {#section-2fc9bea56b6d4b72b80d4f04c5f9b862}

| Nome | Tipo | Descrizione |
|---|---|---|
| ` *`overwriteMode`*` | `xsd:string` | Specifica se sovrascrivere le immagini nella cartella corrente con lo stesso nome e estensione dell’immagine di base. |
| ` *`keepPublishState`*` | `xsd:boolean` | Specifica se un&#39;immagine sostitutiva caricata in IPS deve mantenere l&#39;impostazione &quot;Pronto per la pubblicazione&quot; esistente o se deve essere come specificato dal caricamento. |
| ` *`defaultSourceProfile`*` | `types:Asset` | Specifica il profilo colore sorgente predefinito (Coated FOGRA27 (ISO 126472:2004) applicato automaticamente come parte del parametro &quot;Use default Color Behavior&quot; (Usa comportamento colore predefinito) quando si aggiungono file di immagine CMYK. |
| ` *`defaultDisplayProfile`*` | `types:Asset` | Specifica il profilo colore interno predefinito (US Web Coated (SWOP) v2) applicato automaticamente come parte del &quot;Use default Color Behavior&quot; (Usa comportamento colore predefinito) quando si aggiungono file di immagine CMYK. |
| ` *`iptcExifMappingXslt`*` | `types:Asset` | L&#39;estrazione dei dati dell&#39;intestazione immagine IPTC e EXIF in IPS richiede una conversione dai nomi dei campi interni ai nomi dei campi definiti dall&#39;utente per la società. Determina una tabella di conversione XSL (il valore predefinito è &quot;Non estrarre alcun campo IPTC o EXIF&quot;) per le immagini caricate. |
| ` *`xmpMappingXslt`*` | `types:Asset` | L&#39;estrazione dei dati dell&#39;intestazione immagine XMP in IPS richiede una conversione dai nomi dei campi interni ai nomi dei campi definiti dall&#39;utente per la società. Determina una tabella di conversione XSL (il valore predefinito è &quot;Non estrarre campi XMP&quot;) per le immagini caricate. |
| ` *`diskSpaceWarningMin`*` | `xsd:int` | Quantità minima di spazio libero su disco nella directory delle immagini prima che venga inviato un avviso. |
| ` *`emailTrashCleanupWarning`*` | `xsd:boolean` | Determina se inviare e-mail prima che gli elementi inseriti nel cestino possano essere eliminati automaticamente. |
| ` *`javascriptUploadEnabled`*` | `types:Asset` | Determina se caricare i file JavaScript. Questo è un potenziale rischio per la sicurezza, quindi utilizzate questa opzione con attenzione. |

