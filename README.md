# Energi-Data-Service-Sensor

Der findes en løsning lavet af Marlene Trab i Python til installation i HACS, https://github.com/MTrab/energidataservice

Dog kan man lave samme i HA med en enkel og simpel sensor, som selv indsætte start- og slutdato. Desuden kan man selv bestemme hvor tit der skal scanne efter nye data, samt at man kan udvide historikken ved at ændre days i start-parameter i cURL'en. Ønsker man data fra andre områder, så skal PriceArea ændres fra DK1 til eksempelvis DK2.

Beskrevet diagram ligner dette:

![image](https://user-images.githubusercontent.com/103023823/183290946-112ce31c-cee0-4904-8b8a-543f35cd5eb8.png)
