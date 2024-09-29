# Wsparcio - Agent AI do surfowania po sieci!

![](img/2.png)

Project Design oraz MVP agenta AI (według definicji https://www.aidevs.pl/) przystosowanego do poruszania się po sieci WWW. Agent potrafi wykonywać  taski takiej jak:
- znajdowanie kluczowych informacji na stronie,
- wykonywanie danych czynności na stronie (np. rejestracja na event, zmiana hasła w serwisie, złożenie zapytania ofertowego), 

a interfejsem graficznym dla końcowego użytkownika jest chatbot pojawiający się na każdej odwiedzanej stronie. Agent przystosowany jest do komunikacji z użytkownikami o ograniczonej dostępności. 

Rozwiązanie zaimplementowanie zostanie jako wtyczka do przeglądarki.


## Opis słowny

Używamy web crawlera, do tego web scrapingu. Zescrapowane dane zapisujemy w bazie (cacheujemy, żeby nie powtarzać niepotrzebnie żmudnego procesu web crawlera). Jak już mamy zapisane dane to używamy ich jako kontekst do rozmowy z chatem gpt. chat gpt już z nich potrafi wyciągnąć to o co user pyta.

Jeśli chodzi o wykonywanie trudniejszych tasków jak zmiana hasła na stronie to wymaga interakcji między backendem a chatem gpt oraz interakcji z serwerem strony (poza UI usera). 