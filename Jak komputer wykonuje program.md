Wszystko rozbija się o dwa główne komponenty, bez których dzisiejsze komputery nie mają raczej racji bytu. Mowa o pamięci oraz procesorze. Ogólne zasady ich współpracy są bardzo proste. Pamięć odpowiada za przechowywanie instrukcji dla procesora, które ten pobiera, przetwarza, a później przesyła spowrotem do pamięci, ale tym razem do szuflady dedykowanej dla danych, a nie dla instrukcji.

Istotne w tym miejscu jest zwrócenie uwagi na fakt, iż zarówno pamięć jak i procesor operują na tzw. języku maszynowym. Który jest możliwie najniższą formą reprezentacji danych i informacji w komputerze. 
Język maszynowy można rozumieć po prostu jako zbiór zer i jedynek, natomiast pracę procesora możemy postrzegać jako przetwarzanie zbioru zer i jedynek, na inny zbiór zer i jedynek. I to by było na tyle, ofc procesory różnią się architekturą i wydajnością, ale ogólnie rzecz biorąc ich zasady działania są relatywnie proste. Warto więc w tym miejscu docenić to co byliśmy i jesteśmy w stanie z ich wykorzystaniem osiągać. Tak czy siak zastanówmy się teraz jak wykonywane są napisane w kąpilowanych i interpretowanych językach programowania. 

W przypadku języków kompilowanych, takich jak język C,  kod źródłowy programu, przed jego uruchomieniem na procesorze komputera musi zostać skompilowany, czyli najzwyczajniej w świecie przetłumaczony z wysokopoziomowego języka programowania rozumianego przez człowieka na niskopoziomowy język maszynowy ozumiany przez procesor komputera. 

Do kompilacji korzystamy z dedykowanych programów nazywanych kompilatorami. Ważne jest w tym miejscu odpowiedzenie sobie na pytanie o to, dlaczego proces kompilacji nie może być wykonywany w momencie zapisywania pliku z kodem źródłowym, ano dlatego, że na świecie istnieje wiele różniących się od siebie typów procesorów, które rozumieją, powiedzmy. że różne dialekty języka maszynowego. 

Dzięki temu, że oddzielamy od siebie proces pisania kodu, od procesu kompilacji. Kod programu piszemy raz, po czym możemy go kompilować dowolną liczbę razy, z użyciem różnych kompilatorów na komputery z procesorami o różnych architekturach.

Wrócmy jednak do naszego przykładu: kod źródłowy napisany w języku c, zapisany do pliku o odpowiednim rozszerzeniu, trafia do dedykowanego kompilatora, który tłumaczy kod na instrukcje wyrażone w języku maszynowym, po czym zapisuje je do pliku wykonywalnego. Wyobraźmy sobie teraz, że plik ten znajduje się na pu;picie naszego komputera i klikamy na jego ikonę w celu uruchomienia jego komputera. Co się wtedy stanie? No dokładnie to, co już omówiliśmy. Czyli instrukcje trafiają do pamięci, procesor pobiera je po kolei, przetwarza, po czym wysyła wyniki przetworzenia do pamięci. I to cała filozofia. 

No dobrze, a jak to wrszystko wygląda w przypadku języków interpretowanych takich jak Python? 
Podobnie jak w przypadku języków kompilowanych tak i tutaj zaczynamy od kodu źródłowago zapisanego w pliku o określonym rozszerzeniu. W przypadku języka Python, pliki źródłowe zapisujemy z rozszerzeniem .py
Następnie, w celu uruchomienia napisanego programu, musimy skorzystać z interpretera języka Python. Interpreter języka Python jest po prostu niczym innym, jak kolejnym programem, który możemy uruchamiać z wiersza poleceń (jeśli jest dodany do świeżki środowiskowej).
Otwieramy więc wierz poleceń i wpisujemy słowo python, wraz z plikiem, pamkętając o jego rozszerzeniu.
Naciśnięcie enter powoduje uruchomienie interpretera i przesłanie do niego pliku z kodem źródłowym w języku py
Uruchomienie interpretera powoduje, że w formie zestawu instrukcji ląduje w pamięci komputera, jak każdy inny program napisany w języku kompilowanym.
Co ważne interpreter składa się z dwóch głównych składowych, są nimi tzw. maszyna wirtuallna języka python, oraz kompilator.
I w tym momencie zaczyna się prawdziwa zabawa. Kod źródłowy w postaci pliku, przesłany jako argument, do uruchamianego interpretera, trafia do kompilatora, ale w odróżnieniu od języków kompilowanych, nie jest od razu zamieniany na zestaw instrukcji które mogą od razu zostać przesłane do procesora. Jest bowiem tłumaczony na coś, co nazywamy kodem bajtowym, co nie jest do końca językiem maszonowym, ale też nie jest czymś co rozumie normalny człowiek. 
Kod bajtowy jest następnie pobierany przez maszynę wirtualną i tłumaczone na instrukcje, w języku maszynowym, które jak już wiemy, może zrozumieć nasz procesor.
Ostatecznie więc instrukcje reprezentujące program napisany w języku py pobierane są przez procesor z maszyny wirtualnej i wykonywane jak wszystkie inne instrukcje, każdego innego programu.
![[Pasted image 20230507184607.png]]

Dlaczego język jest kompilowany / interpretowany? Ostatecznie wszystko sprowadza się do kilku małych, subtelnych różnic, które wynikają w głównej mierze z faktu, że w przypadku języków kompilowanych możemy uruchomić program dopiero wtedy gdy jest już wyrażony w języku maszynowym, natomiast w przypadku języków interpretowanych możemy uruchomić program gdy ten jest wyrażony w formie kodu źródłowego.

Ta, wydawałoby się mała różnica powoduje, że dla przykładu nie możemy modyfikować kodu napisanego w języku kompilowanym, w czasie jego działania, gdzie w przypadku programu napisanego w języku interpretowanym nie ma z tym problemu.  I róŻnic między językami jest ofc więcej, ale myślę, że na początek wystarczy nam to, czego się właśnie dowiedzieliśmy. 
![[Pasted image 20230507185108.png]]

Czyli to czym jest interpreter języka py oraz co robi z napisanem kodem żródłowym. 

Programować w języku py możemy na 3 główne sposoby.
- w przeznaczonym do tego edytorze i zapisywaniu go do pliku, tak napisany program możemy następnie uruchomić za pomocą cmd , korzystając w tym celu z interpretera języka py. Psać kod źródłowy możemy natomiast w dowolnym edytorze, choćby w zwykłym notatniku.