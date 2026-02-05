# Do zrobienia
- Moduł A - dodać tabelę z metrykami
    - Comprehensiveness: Spadek pewności po usunięciu top-k tokenów (mamy tą wartość)
    - Sufficiency: Pewność modelu, gdy zostawimy tylko top-k tokenów, a resztę zamaskujemy.
- Moduł C - lepsze parafrazy
    - sprawdzić kod na parafrazach, które będą zmieniały tylko nieistotne słowa (synonimy?)
    - dodac prostą pętlę, która zamienia 1-2 słowa na synonimy (NLTK, WordNet) i sprawdź korelację map atrybucji przed i po zmianie.
- Moduł C - warto zapisywać do pliku .json lub .csv konkretne pary: Tekst oryginalny -> Wyjaśnienie A | Parafraza -> Wyjaśnienie B. Będą to idealne przykłady ("Case Studies") do zamieszczenia w treści pracy.
- Dodać testy istotności statystycznej (t-test?), które potwierdzą, ze róznica pomiędzy IG a IxG nie jest przypadkowa
- Zweryfikować i wyjaśnić
    - Synteza w Module D (Twój "Killer Feature") To jest najsilniejszy punkt Twojej pracy. Pokazujesz, że XAI nie jest tylko "ładnym obrazkiem", ale narzędziem inżynierskim. W opisie pracy nazwij to "XAI-driven Model Editing" lub "Representation Engineering". To brzmi znacznie lepiej niż zwykłe "sterowanie".
- Sprawdzić jak mozna lepiej uzyć Captum do wizualizacji przykładów (np. zaznaczanie kolorem w tekście)
- Metryki quantus - czy nie lepiej uzyc wbudowanych do quantusa metryk (np. Sparsity, Continuity), a nie tylko ręcznie zaimplementowane Comprehensivness
- Uwzględnić w pracy wybór warstwy 5 -> wykresy!!


## Na później
- sprawdzić czy nie lepiej będzie zmienić główny model z DistillBerta na DeBERTA-v3

# Pytania
- Róznice w warstwach (3 czy 5), wyjaśnić dlaczego i wytłumaczyć? Czy wykres, ktory mamy wcześniej jest wiarygodny?
    - Warstwa 3 wydaje się duzo lepsza na podstawie wyników z test_steering notebook!
- Uzywamy tylko metod gradientowych (Captum), czy potrzebujemy tez dodać SHAP albo LIME?

# Notatki
1. Po wytrenowaniu model w training.ipynb skopiować ściezkę modelu wynikowego do plików
- training.ipynb -> OUTPUT_MODEL_DIR = "/drive/MyDrive/msc-project/models/distilbert-jigsaw-binary_{TIMESTAMP}"
- test_pharaphrases.ipynb -> MODEL_CHECKPOINT = "/drive/MyDrive/msc-project/models/distilbert-jigsaw-binary_{TIMESTAMP}"
- test.ipynb -> MODEL_CHECKPOINT = "/drive/MyDrive/msc-project/models/distilbert-jigsaw-binary_{TIMESTAMP}"
