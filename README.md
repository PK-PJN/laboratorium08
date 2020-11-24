# Przetwarzanie języka naturalnego
# Laboratorium 8: modele wektorowe (*word embeddings*)

1. Dzięki łatwo dostępnym wielkim korpusom tekstów
(np. Wikipedii) w ostatnich latach powstało
sporo metod przedstawiania znaczenia wyrazów lub wyrażeń
jako wielowymiarowych wektorów (tzn. dość długich tablic)
liczb rzeczywistych. Łatwo jest obliczyć
cosinus kąta między dwoma takimi wektorami,
czyli ich
[podobieństwo cosinusowe](https://en.wikipedia.org/wiki/Cosine_similarity),
znane z laboratorium 6.
Wektory zaś są wyznaczane na podstawie kontekstów,
w których występują wyrazy lub wyrażenia.
Chyba najbardziej znaną metodą tworzenia takich modeli wektorowych jest
[word2vec](https://en.wikipedia.org/wiki/Word2vec).
Godna uwagi jest też metoda
[fastText](https://fasttext.cc/),
polegająca na sumowaniu wektorów odpowiadających *N*-gramom,
z których składają się wyrazy.

2. Dzisiejsze laboratorium nie wymaga programowania.
Zostanie wykonane zdalnie na stronie
[dsmodels.nlp.ipipan.waw.pl](http://dsmodels.nlp.ipipan.waw.pl/).

3. [Podobieństwo wyrazów](http://dsmodels.nlp.ipipan.waw.pl/sim2.html).
Używając modelu opartego na formach,
znaleźć po 10 wyrazów podobnych do
    * dowolnych dwóch rzeczowników (w mianowniku liczby pojedynczej);
    * dowolnych dwóch przymiotników (w mianowniku liczby pojedynczej
    rodzaju męskiego stopnia równego);
    * dowolnych dwóch czasowników (w bezokoliczniku).

4. Podobieństwo wyrazów — ciąg dalszy. Znaleźć po 10 wyrazów
podobnych do tych samych wyrazów,
które zostały użyte w poprzednim punkcie,
ale tym razem w innych formach odmiany.

5. [Arytmetyka wyrazów](http://dsmodels.nlp.ipipan.waw.pl/arithmetic.html).
Równość (*król* − *mężczyzna*) + *kobieta* ≈ *królowa*
jest jednym ze sławniejszych przykładów
zastosowania modeli wektorowych
(chociaż w rzeczywistości ich zdolność znajdowania
analogii między wyrazami okazała się
[nieco przereklamowana](https://twitter.com/rikvannoord/status/1132933236756238341)).
Używając modelu opartego na formach,
znaleźć po 10 wyrazów najbliższych
do pięciu innych wyrażeń arytmetycznych postaci *A* − *B* + *C*
(bez nawiasów, bo strona kapryśnie je rozpoznaje,
ale i tak wygodniej z niej korzystać
niż z pozbawionej wskazówek strony *Analogie*).
Oprócz analogii typu *osoba*:*płeć*
można próbować np. typów *państwo*:*stolica*,
*nazwisko osoby*:*język*, *zwierzę*:*odgłos*, *przedmiot*:*barwa*,
*przymiotnik pozytywny*:*przymiotnik negatywny*
(warto porównać wyrażenia zaczynające się od *dobry* − *zły*,
czyli najczęstszej takiej pary,
z wyrażeniami zaczynającymi się od rzadszych przymiotników),
*wyraz*:*jego inna forma* lub dowolnych innych,
które przyjdą Państwu do głowy.

6. Sprawozdanie powinno zawierać dane i wyniki
z punktów 3–5 oraz wnioski. Wystarczy po jednym
zdaniu wniosku w każdym punkcie.

Dodatek. Osobom zainteresowanym budowaniem
własnych modeli wektorowych polecam Pythonową
bibliotekę `gensim`, która potrafi tworzyć modele
[word2vec](https://radimrehurek.com/gensim/models/word2vec.html)
i
[fastText](https://radimrehurek.com/gensim/models/fasttext.html).
Natomiast narzędzie
[`wikipedia2vec`](https://github.com/wikipedia2vec/wikipedia2vec)
tworzy modele, których wektory odpowiadają
nie tylko wyrazom języka, lecz również hasłom Wikipedii.
Ciekawym doświadczeniem może być porównanie
rekomendacji opartych na takich modelach
z rekomendacjami opartymi na treści haseł.
