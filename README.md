# Energi-Data-Service-Sensor

Der findes en løsning lavet af Malene Trab i Python til installation i HACS, https://github.com/MTrab/energidataservice

Dog kan man lave samme i HA med en enkel og simpel sensor, som selv indsætte start- og slutdato. Desuden kan man selv bestemme hvor tit der skal scanne efter nye data, samt at man kan udvide historikken ved at ændre days i start-parameter i cURL'en. Ønsker man data fra andre områder, så skal PriceArea ændres fra DK1 til eksempelvis DK2. Ønsker man flere så giv lyd, så skal jeg vise hvordan man kØRL'er sådan en.

"Tilføj kort" til din brugergrænseflade/dashboard, og vælg apexcharts-card. Så kopier du koden ind vinduet til venstre, så skulle diagrammet komme til syne i højre vindue.
Diagramet bruger grøn, gul og rød farve for at markere forskelle pris, hvor grøn er lavest og rød højest. Beskrevet diagram ligner dette:

![image](https://user-images.githubusercontent.com/103023823/183419890-0737c639-06cf-4959-8c0c-ecc75de36407.png)

PS
Viser diagrammet "Loading" i stedet for data fra sensor, så er formentlig noget gal med formattering af koden eller ikke komplet kopiering. Vælg ikon "Copy raw content" på Github, og brug Ctrl+a for at markere al tekst og indsæt/erstat med Ctrl+v...

Ønsker du en mere tekstuel fremstilling, som:

![image](https://user-images.githubusercontent.com/103023823/189045731-00e8d17b-dbb0-4f1b-ad4d-960e3adfaa0e.png)

Tilføj et Markdown-kortkonfiguration, og smid koden ind i fra https://github.com/MaximusClavius/Energi-Data-Service-Sensor/blob/main/spotprice%20in%20near%20future. Ønsker du flere eller mindre end 3 priser, så skal du trylle med ns.count.
