In acest proiectat am implementat un model ce calculeaza ce sanse are o persoana sa obtina un imprumut pe baza anumitori criterii, regasite in fiserul .csv.

In primul rand, am verificat daca exista valori lipsa in dataset. In cazul in care sunt prea multe valori lipsa(mai mult de 50% dintre exemple), nu voi lua in considerare coloana respectiva.
Daca sunt mai putine, le voi inlocui cu media coloanei, in cazul datelor numerice sau cu cel mai intalnit element, in cazul datelor catergorice.
Verific daca procentul de acceptare/respingere este cu mult mai mare decat procentul de respingere/acceptare. Daca este o diferenta majore, modelul va avea probleme.
Normalizez coloana de LoanAmount si transform datele categorice in date numerice. 

Incerc regresie logistica si KNN pentru aceasta problema. Observ ca modelul de regresie logistica are rezultatele mai bune
si ii optimizez hiper-parametrii. Avand mai multe coloane aleg sa utilizez tehnica de optimizare RandomizedSearchCV pentru a avea o eficienta mai mare
Ii optimizez 'C' - parametru de regularizare, tehnica de regularizare si algoritmul de optimizare. Rulez din nou modelul cu cea mai buni hiper-parametrii
si obtiun o precizie de 0.88 pentru cazul in care nu este acordat imprumutul si 0.83 pentru situatia in care ii este acordat. Iar, precizia medie avand in vedere numarul de exemple pentru fiecare caz este 0.84.
