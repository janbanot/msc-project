# Pytania
## test.ipynb
Moduł A

Moduł B

Moduł C

Moduł D
- Sprawdzić jak to wygląda w rzeczywistości jakie przykłady generuje? Przed i po detoksyfikacji, zeby zweryfikować, ze to ma sens.

Ogólne
- Czy te metryki są wystarczające? Czy moze potrzebne jest coś jeszcze?
- Czy obecna forma przedstawienia wyników jest ok czy moze lepiej coś zmienić?

## training.ipynb
- Jak duzy jest ten zbiór danych? Co zmienia trening na całości, a na 10k jak teraz
- Tutaj mamy zdefiniowane więcej etykiet, czy nie powinniśmy ich tez uzywać wcześniej?
label_cols = ["toxic", "severe_toxic", "obscene", "threat", "insult", "identity_hate"]

# Notatki
1. Po wytrenowaniu model w training.ipynb skopiować ściezkę modelu wynikowego do plików
- training.ipynb -> OUTPUT_MODEL_DIR = "/drive/MyDrive/msc-project/models/distilbert-jigsaw-binary_{TIMESTAMP}"
- test_pharaphrases.ipynb -> MODEL_CHECKPOINT = "/drive/MyDrive/msc-project/models/distilbert-jigsaw-binary_{TIMESTAMP}"
- test.ipynb -> MODEL_CHECKPOINT = "/drive/MyDrive/msc-project/models/distilbert-jigsaw-binary_{TIMESTAMP}"

# To Do
- sprawdzić czy nie lepiej będzie zmienić główny model z DistillBerta na DeBERTA-v3

- Uzywamy tylko metod gradientowych (Captum), czy potrzebujemy tez dodać SHAP albo LIME?
- Sprawdzić jak mozna lepiej uzyć Captum do wizualizacji przykładów (np. zaznaczanie kolorem w tekście)
- Metryki quantus - czy nie lepiej uzyc wbudowanych do quantusa metryk (np. Sparsity, Continuity), a nie tylko ręcznie zaimplementowane Comprehensivness
- Moduł C - sprawdzić kod na parafrazach, które będą zmieniały tylko nieistotne słowa (synonimy?)
- Moduł C - warto zapisywać do pliku .json lub .csv konkretne pary: Tekst oryginalny -> Wyjaśnienie A | Parafraza -> Wyjaśnienie B. Będą to idealne przykłady ("Case Studies") do zamieszczenia w treści pracy.
- Uwzględnić w pracy wybór warstwy 5, wykresy!!