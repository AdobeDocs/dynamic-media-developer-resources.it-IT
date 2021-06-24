---
description: Dimensioni del livello. Specifica la dimensione o la dimensione massima del livello per un livello, prima che rota=, prospettiva= e estendi= vengano applicati al livello.
solution: Experience Manager
title: size
feature: Dynamic Media Classic, SDK/API
role: Developer,Business Practitioner
exl-id: 55feeb32-b69d-4b95-80fb-c77f2612d255
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 1%

---

# size{#size}

Dimensioni del livello. Specifica la dimensione o la dimensione massima del livello per un livello, prima che rota=, prospettiva= e estendi= vengano applicati al livello.

` size= *``*, *`larghezza`*`

` sizeN= *``*, *`widthNheightN`*`

<table id="simpletable_FBE17D736F93485AA0053BF447B4CC9F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> larghezza  </span>,  <span class="varname"> altezza  </span> </span> </p> </td> 
  <td class="stentry"> <p>Vincolo di dimensione del livello in pixel (int, int, 0 o superiore). </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> larghezzaN  </span>,  <span class="varname"> altezzaN  </span> </span> </p> </td> 
  <td class="stentry"> <p>Vincolo dimensione livello normalizzato rispetto alla dimensione 0 del livello (reale, reale, 0.0...1.0). </p> </td> 
 </tr> 
</table>

Se specificato per un livello immagine, size= limita la larghezza, l&#39;altezza o l&#39;altezza dell&#39;immagine del livello. L’immagine verrà ridimensionata in modo da non essere più grande di `size=`. Se viene specificata una dimensione normalizzata, questa è relativa alla dimensione del livello 0. Se sono specificati sia *`width`* che *`height`*, l’immagine sorgente viene ridimensionata (dopo l’applicazione di `crop=`) in modo che nessuna delle due dimensioni superi le dimensioni specificate. Le proporzioni del rettangolo di origine vengono mantenute in tutti i casi. È possibile impostare *`width`* o *`height`* su 0; in questo caso il valore viene calcolato dal server in base alle proporzioni dell&#39;immagine.

Se specificato per un livello di testo, `size=` specifica le dimensioni della casella di testo. *`width`* è obbligatorio;  *`height`* può essere impostato su 0, nel qual caso l&#39;altezza del testo disposto viene utilizzata come altezza del livello. Per impostazione predefinita, i motori di layout di testo inseriscono interruzioni di riga per garantire che il testo si adatti sempre in orizzontale allo spazio disponibile. Se si specifica *`height`*, le righe che non rientrano nello spazio disponibile vengono ritagliate ( `text=`) o omesse ( `textPs=`). `text=` supporta ulteriori modalità di adattamento; fare riferimento a  `textAttr=` per ulteriori informazioni.

Se specificato per un livello di colore solido, `size=` definisce la dimensione esatta del livello; è necessario specificare entrambi i valori (a meno che non sia fornita una maschera). Se è specificato anche `mask=`, l&#39;immagine della maschera verrà ridimensionata in modo da adattarsi a `size=` nello stesso modo in cui le immagini vengono ridimensionate nei livelli dell&#39;immagine.

## Proprietà {#section-5f254b66fcba49bcb63f9c9ea40b230c}

Attributo livello. Si applica al livello 0 se `layer=comp`. `sizeN=` non è consentito per  `layer=0` o  `layer=comp`. `sizeN=` è consentito per  `layer=0` e  `layer=comp` solo nei record di catalogo che definiscono immagini di filigrana. In questo caso, `sizeN` definisce la scala dell&#39;immagine della filigrana rispetto all&#39;immagine composita a cui viene applicata la filigrana. Se è specificato `size=`, `res=` e `scale=` vengono ignorati per questo livello. Ignorato dai livelli di effetto.

## Predefinito {#section-43d129deba6a441da66a1fdb63d1c85c}

`size=0,0`, le dimensioni del livello non sono vincolate. Per i livelli immagine, la dimensione del livello viene quindi determinata in base alle dimensioni dell&#39;immagine del livello dopo l&#39;applicazione di eventuali operazioni `crop=`, `scale=` o `res=`. Per i livelli di testo, se `size=` non è specificato, il livello viene ridimensionato automaticamente per adattarsi al testo sottoposto a rendering.

I livelli a colori solidi richiedono un `size=` completamente specificato, un `mask=` o `clipPath=`.

## Esempio {#section-d1adaddd9e0b4ca881fd8e0a7541e5d9}

Vedere [Esempio A](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/r-example-a.md#reference-c78ea82e8a1646738e764fa6685dfbac) in [Modelli](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-templates/c-templates.md#concept-3cd2d2adae0e41b2979b9640244d4d3e).

## Consultate anche {#section-63dfdf3750e249d2ab4c825ccd2e7181}

[scale=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-is-http-scale.md#reference-098c30cea1764f189e6f7c7e400cc065) ,  [res=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-res.md#reference-3d6fe416801148dea0f786f2b5169e55),  [textAttr=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-textattr.md#reference-ff00484fa3244286abeff34911f7ec0d),  [mask=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-mask.md#reference-922254e027404fb890b850e2723ee06e),  [clipPath=](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-clippath.md#reference-8139b1b52dc54749b51b109521ddf83d), livelli  [di testo](../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-text-formatting/r-text-layers.md#reference-47e78cfb18134db5ab09e17af14a6a8f)
