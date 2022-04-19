# [offer.infrash.com](https://infrash.github.io/offer/)



## for whom ?

+ software houses
+ SaaS
+ PoC, MVN
+ freelancers
    + devops
    + admin
    + architect


## use cases

+ privatye infra

## when is important

+ migration - mapigration.com
    + monitoring infrastruicture
    + testing infrastruicture and apps
+ integration with hundreds and more services


## Z notatnika DevOps'a

chodzi o generowanie pliku wyjsciowego csv z wynikami na podstawie wejsciowego bez wyników

    load.sh 1/in.csv 1/out.csv 1/status.csv

wejsciowy

    domain,https_status
    example1.com
    example2.com
    example3.com
    
wyjsciowy, wygenerowany przez skrypt bash

    domain,https_status
    example1.com,200
    example2.com,500
    example3.com,200

chodzi o masowe generowanie wyników z shella
aby sprawdzać i zapisywać stan infrastruktury
np robienie pingów dla setek domen
z informacją o przebiegu statusu zadań
jak to będzie działać to wezmę się za skrypty do skanowania infry
oraz API do pobierania obiektów które będą monitorowane, domen, numerów IP,

## masz coś podobnego w swojej skrzynce narzędziowej?

To rozwiązanie dla osób zajmujących się testowaniem infrastruktury z setkami domen i tysiącami subdomen

## Mapa Infrastruktury - MultiSiteMap.com

Skrypt generuje raport, z potrzebnymi informacjami co nie działa ale żeby wiedzieć czy coś działa niepoprawnie trzeba zdefiniować oczekiwany stan.

np domena ktora ma isc na sprzedaż powinna wisieć na parkingu
a domena, która ma wordpressa powinna pokazywać poprawną stronę a nie np. widok strony serwisowej
inna sprawa to indywidualne skrypty i ministronki, gdzie trzeba też sprawdzać DNS
bo są domeny z wieloma zależnosciami, jedna domena może być poprzez DNS przypisana do różnych usług i to muszę monitorować

## migracje

najgorsze są migracje
wtedy muszę testować czy wszystko działa tak jak wcześniej
czy jakieś domeny nie padły, np na skutek zmiany namesevera

## mapowanie

w pliku mapy, trzeba zdefiniować oczekiwane NS i DNS a także zdefiniować oczekiwane treści na każdej domenie, url
aby było wiadomo, że mimo, że stronka wisi to działa poprawnie
aktualnie jak są jakieś zmiany, to mimo, że wiem, że coś padło, to muszę "pamiętać" każdą z setek domen, co powinna wyświetlać i na jakich nameserwerach być podłączona 
trudno testować infrastrukturę u jednego usługodawcy gdy ma się wiele usługodawców

