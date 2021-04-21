---
description: Applica le opzioni di lavoro PDF. Un file di opzioni di lavoro o un predefinito PDF è un file generato da Illustrator nella finestra di dialogo Opzioni Salva come PDF o i predefiniti PDF in InDesign.
solution: Experience Manager
title: joboption
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 46%

---


# joboption{#joboption}

Applica le opzioni di lavoro PDF. Un file di opzioni di lavoro o un predefinito PDF è un file generato da Illustrator nella finestra di dialogo Opzioni Salva come PDF o i predefiniti PDF in InDesign.

` joboption= *`value`*`

<table id="simpletable_BA7B58BE0B0740298D45DDEBE7832D93"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> value</span></span> </p> </td> 
  <td class="stentry"> <p>IPSID del file delle opzioni del processo. </p></td> 
 </tr> 
</table>

Il file delle opzioni di processo può essere caricato e pubblicato da IPS/Dynamic Media Classic. Le opzioni PDF contenute nel file delle opzioni di lavoro vengono utilizzate quando il PDF viene generato.

Sono attualmente supportate le seguenti opzioni:

<table id="simpletable_7E0AE8A06AE54A02AF0107FBEDF73D61"> 
 <tr class="strow"> 
  <td class="stentry"> <p>Generali </p></td> 
  <td class="stentry"> <p> Compatibilità </p> <p> Compressione a livello di oggetto </p> <p> Miniature incorporate </p> <p> Ottimizzazione per accesso rapido sul Web </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Immagini </p></td> 
  <td class="stentry"> <p> Downsampling, risoluzione, soglia e compressione per colore, grigio e mono </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Font </p></td> 
  <td class="stentry"> <p> Incorpora tutti i font </p> <p> Incorporazione dei font OpenType </p> <p> Creazione di sottoinsiemi di font incorporati quando la percentuale di caratteri usati è minore di un determinato valore </p> <p> Elenco dei font da incorporare sempre </p> <p> Elenco dei font da non incorporare mai </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Colore </p></td> 
  <td class="stentry"> <p> Strategia colore (Tag per sole immagini viene trattato come Tag per tutto) </p> <p> Intento di rendering del documento </p> <p> Per 4.2.5 sono supportati solo i seguenti spazi di lavoro. </p> <p> 
    <ul id="ul_3F3EFDFB6A3340978AE31DEDF0FDA2C8"> 
     <li id="li_17A9FA99D6CA4C5182E383A85F0E3C90"> RGB <p> 
       <ul id="ul_1DD0C264DA1248319E751ADD18140C6D"> 
        <li id="li_B91B4D0C1D80442EB8690933AFA1F093"> e-sRGB </li> 
        <li id="li_D7F8C500DF5E4CBC8FFA4FEFB8E4E036"> scRGB con intervallo di codifica [-4,0, 4,0] </li> 
        <li id="li_942CD69732984E16A71C2F75EC5B5245"> Lab D50 </li> 
        <li id="li_7063B9E98D1E4946AC8F0EF7BC988806"> PCS XYZ </li> 
        <li id="li_5809447576B147B68630C4B7EC2E7870"> Flat XYZ </li> 
        <li id="li_3B5DA42A04124A6BAA12343AFC19F620">ROMM-RGB lineare </li> 
        <li id="li_DEC3028FA9C34176B761D12B7179B44F">ROMM-RGB </li> 
        <li id="li_3E7E7C4A680C4E3EADE0A26048ECF1F4"> sYCC a 8 bit </li> 
        <li id="li_16A615C9A74D443AB3C63B3FE3AB5443"> e-sYCC a 8 bit </li> 
       </ul> </p> </li> 
     <li id="li_AFA6D4D8C0624AA495E2EB2F0F0C7F7B">Grigio <p> 
       <ul id="ul_945389DD426F44C09EB9C7F23933CB77"> 
        <li id="li_DB0AE3DFFC184480BB91666FF1BB4776">Grigio gamma 1,8 </li> 
        <li id="li_755C556ED94740D1BD30EBE67018E074">Grigio gamma 2,2 </li> 
        <li id="li_67437440AFB54B7686333A55233AA87F">Ingrossamento punti 10% </li> 
        <li id="li_0D6CA6004EC84048B5F2198406F4F343">Ingrossamento punti 15% </li> 
        <li id="li_1AFD11C23AB147978559D8F00BFB3142">Ingrossamento punti 20% </li> 
        <li id="li_6CD5ACEF6B0B49E8BACA8264FE0E9C44"> Ingrossamento punti 25% </li> 
        <li id="li_AB5F1FA7111041BD82353E02A284A546">Ingrossamento punti 30% </li> 
        <li id="li_7433278AE8054AD28BD38A0A6E4EF7EF"> sGray </li> 
       </ul> </p> </li> 
    </ul> </p> <p> Mantenimento dei valori CMYK per spazi colore CMYK calibrati </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Avanzate </p></td> 
  <td class="stentry"> <p>Mantenimento dei commenti OPI sempre attivo. </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>Standard </p></td> 
  <td class="stentry"> <p>Standard di conformità. </p></td> 
 </tr> 
</table>

