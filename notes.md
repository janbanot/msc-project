Otwarte pytania:
test.ipynb
Moduł A
- Filtrowanie tylko toksycznych przykładów - czy tutaj nie powinniśmy brać pod uwagę tez innych etykiet dla pełnego obrazu testu?

Moduł B
- Tak samo jak wyzej, czy to dobrze, ze wyciągamy? - Tylko etykieta 'toxic' (indeks 0)
- Czy tutaj zawsze powinniśmy zapisywać warstwę 5, a nie robić tego per case? - Zapisujemy aktywacje warstwy 5 do wykorzystania w Module D (steering)

Moduł C
- Metoda parafraz do przetestowania czy nie trzeba jej przepisać czy to faktycznie działa, bo mam wątpliwości
- Co to jest Jaccard Index?

Moduł D
- Sprawdzić jak to wygląda w rzeczywistości jakie przykłady generuje? Przed i po detoksyfikacji, zeby zweryfikować, ze to ma sens.

Ogólne
- Czy te metryki są wystarczające? Czy moze potrzebne jest coś jeszcze?
- Czy obecna forma przedstawienia wyników jest ok czy moze lepiej coś zmienić?

training.ipynb
- Jak duzy jest ten zbiór danych? Co zmienia trening na całości, a na 10k jak teraz
- Tutaj mamy zdefiniowane więcej etykiet, czy nie powinniśmy ich tez uzywać wcześniej?
label_cols = ["toxic", "severe_toxic", "obscene", "threat", "insult", "identity_hate"]
