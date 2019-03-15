Ustawianie parametrów sieci ip
------------------------------
* stan interfejsu
    * interfejs up
    * interfejs down
* adresacja
    * dodaj adres
    * zmień adres
    * usuń adres
* routing
    * dodaj trasę default
    * dodaj trasę przez bramę
    * dodaj trasę przez interfejs
    * usuń trasę
    * zmień trasę
    * pobierz trasę dla adresu
* adresacja fizyczna
    * pokaż adresy interfejsów dostępnych w sieci
    * pokaż adresy dla konkretnego interfejsu
     


ip 
-------------------------
| subcommand    |  polecenie   | opis  |
| ------------- |:-------------| :---------------| 
|   ``addr``    |                               | informacje o adresacji i własnościach interfejsów |
|     ``addr``  |   ``ip addr``                 | informacja o wszystkich interfejsach              |
|     ``addr``  |   ``ip addr show dev enp0s3`` | informacja o konkretnym interfejsie               |
|   ``link``    |  ``ip link set dev eth0 down``| służy do konfigurowania, włączania i zarządzania urządzeniami sieciowymi oraz urządzeniami wirtualnymi warstwy sieci |
|   ``route``   | ``ip route add default via 192.168.0.1`` | służy do zarządzania tablicami routingu wewnątrz jądra. Pozwala na dodawanie, usuwanie i modyfikowanie tras. Składnia polecenia wyświetlana za pomocą polecenia `ip route help`: |
|   ``maddr``   | ``ip maddr [ add , del ] MULTIADDR dev STRING`` | Multicast addresses management |
|   ``neigh``   |  ``ip neigh { add , del , change , replace }`` | Command manipulates neighbour objects that establish bindings between protocol addresses and link layer addresses for hosts sharing the same link.  Neighbour entries are organized into tables. The IPv4 neighbour table is also known by another name - the ARP table |
|   ``help``    | ``ip help, ip addr help, ip link help, ip neigh help`` | Display a list of commands and arguments for each subcommand |



Notatki
------------

* curl -X POST -d '{"text": ":D"}' http://172.16.100.10:8888/chat
* ip addr add 172.16.100.11/24 dev enp0s3



Zadanie
------------

![zadanie 3](cwiczenia3.svg)
![](https://github.com/MrSyta/sk-2019/blob/master/%C4%86wiczenia-3/obrazek.png)

1.
   * Przygotuj konfigurację sieci zgodnie z powyższym diagramem, 
   * Przetestuj połączenie poleceniem ping
2.
   * Zainstaluj na komputerze ``PC1`` serwer programu ``HTTP CHAT`` dostępnego pod adresem ``https://github.com/jkanclerz/http-chat``
   * Przetestuj komunikację wysyłając wiadomość z komputera ``PC2``, upewnij się czy jest widoczna w konsoli serwera
3.
   * Dodaj do istniejącej sieci komputer ``PC3`` pod kontroloą systemu windows
   * Skonfiguruj ``PC3`` zgodnie z poniższym diagramem
   * Zweryfkuj połączenie kożystając z przeglądarki, odwiedzając graficzny interfejs ``HTTP CHAT`` pod adresem ``http://172.16.100.10:8888``
   * Przygotuj dokumentację pisemno obrazkową z wykonania zadania w formacie ``markdown`` zamieść ją w serwisie ``github.com`` obok obocnego tematu ``cwiczenia-3``

![zadanie 3.1](cwiczenia3.1.svg) 
