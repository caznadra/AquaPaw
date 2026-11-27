# Blinkprogram på NodeMCU (ESP8266)


## Översikt

Ett Blinkprogram är ett enkelt program som får en LED-lampa att tändas och släckas. Det är ett bra första exempel för att lära sig hur en mikrokontroller fungerar och hur man styr en digital port.

## Mikroprocessor

NodeMCU använder mikroprocessorn ESP8266. Den kan programmeras med Arduino IDE och har digitala pinnar som kan användas för att ansluta olika komponenter, till exempel LED-lampor och sensorer.

NodeMCU ansluts till datorn med en USB-kabel. Koden skrivs i Arduino IDE och laddas sedan upp till kortet.

![NodeMCU board](

## Två basfunktioner i Arduino

Arduino-program använder två viktiga funktioner:

- `setup()` körs en gång när programmet startar. Här görs inställningar, till exempel vilka pinnar som ska användas.
- `loop()` körs om och om igen. Här skriver man koden som ska upprepas.

## Portinitialisering

För att kunna styra en LED måste pinnen ställas in som en utgång. Detta görs med `pinMode()`.

Exempel:

`pinMode(D5, OUTPUT);`

D5 är pinnen som används. `OUTPUT` betyder att mikroprocessorn ska skicka en signal ut från pinnen.

## Kod med förklaringar

I Blinkprogrammet skickas först en HIGH-signal till pin D5. LED-lampan tänds och väntar i en sekund. Sedan skickas en LOW-signal och lampan släcks. Detta upprepas hela tiden.

- `digitalWrite(HIGH)` – tänder LED-lampan.
- `digitalWrite(LOW)` – släcker LED-lampan.
- `delay(1000)` – väntar i 1000 millisekunder, alltså en sekund.

## Kodexempel

Här visas ett exempel på ett Blinkprogram i Arduino IDE. Programmet tänder LED-lampan i en sekund och släcker den i en sekund.

![Blinkprogram i Arduino IDE]

## Användning i vårt projekt

I vårt projekt ska vi mäta hur mycket vatten en katt dricker. Samma princip med digitala signaler kan användas för att styra en LED. Till exempel kan en LED tändas om vattennivån är låg och visa att katten behöver mer vatten.

## Resultat

Med Blinkprogrammet lär vi oss hur en mikroprocessor kan styra en komponent genom att skicka signaler från en digital pin.
