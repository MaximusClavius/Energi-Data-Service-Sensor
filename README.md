# Energi-Data-Service-Sensor

Der findes en løsning lavet af Malene Trab i Python til installation i HACS, https://github.com/MTrab/energidataservice

Dog kan man lave samme i HA med en enkel og simpel sensor, som selv indsætte start- og slutdato. Desuden kan man selv bestemme hvor tit der skal scanne efter nye data, samt at man kan udvide historikken ved at ændre days i start-parameter i cURL'en. Ønsker man data fra andre områder, så skal PriceArea ændres fra DK1 til eksempelvis DK2. Ønsker man flere så giv lyd, så skal jeg vise hvordan man kØRL'er sådan en.

TO-DO:
1) Tilføj sensor
2) Tilføj kort (Søjlediagram)
3) Tilføj aktuel pris som gauge-kort
4) Tilføj kort (De 3 billigste priser i nærmeste fremtid)

Ad 1:
Hele koden til sensor smides ind i configuration.yaml eller bruger du separat fil til sensorer, så alle linjer undtagende den første (som starter med sensor). Eventuel "TJEK KONFIGURATION" og derefter "GENSTART"! Alternativt kan man nøjes med "GENINDLÆS KOMMANDOLINJE ENTITETER", hvis denne funktionalitet er aktiveret.

Ad 2:
"Tilføj kort" til din brugergrænseflade/dashboard, og vælg apexcharts-card. Så kopier du koden ind vinduet til venstre, så skulle diagrammet komme til syne i højre vindue. Priserne er med tarif, abonnement og moms. Diagramet bruger grøn, gul og rød farve for at markere forskelle pris, hvor grøn er lavest og rød højest. Er man mere til et linjediagram, så skal linjen "type: column" ændres til "type: line". Beskrevet diagram ligner dette:

![image](https://user-images.githubusercontent.com/103023823/183419890-0737c639-06cf-4959-8c0c-ecc75de36407.png)

![image](https://user-images.githubusercontent.com/103023823/189534752-a431daf2-fab4-454d-b315-f1037b5b599a.png)

PS
Viser diagrammet "Loading" i stedet for data fra sensor, så er formentlig noget gal med formattering af koden eller ikke komplet kopiering. Vælg ikon "Copy raw content" på Github, og brug Ctrl+a for at markere al tekst og indsæt/erstat med Ctrl+v...

Ad 3:
Den aktuelle pris med markering af prisintervaller i forskellige farver.

![image](https://user-images.githubusercontent.com/103023823/206850966-839c8d47-3994-4e18-aadd-fbddf7ee01e8.png)

Der skal laves en sensor til kortet, og det er en template, som: https://github.com/MaximusClavius/Energi-Data-Service-Sensor/blob/main/energinet%20aktuel%20pris%20sensor. Eventuel "TJEK KONFIGURATION" og derefter "GENSTART"! Alternativt kan man nøjes med "GENINDLÆS TEMPLATE ENTITETER", hvis denne funktionalitet er aktiveret. Tilføj et Gauge-kortkonfiguration, og og smid yaml/koden ind i fra https://github.com/MaximusClavius/Energi-Data-Service-Sensor/blob/main/energinet%20aktuel%20pris%20gauge

Ad 4:
Ønsker du en mere tekstuel fremstilling og indeholdende tarif og abonnement, som:

![image](https://user-images.githubusercontent.com/103023823/189045731-00e8d17b-dbb0-4f1b-ad4d-960e3adfaa0e.png)

Tilføj et Markdown-kortkonfiguration, og smid yaml/koden ind i fra https://github.com/MaximusClavius/Energi-Data-Service-Sensor/blob/main/spotprice%20in%20near%20future. Ønsker du flere eller mindre end 3 priser, så skal du trylle med "ns.count < 3".
