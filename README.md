Trieda DataHandler vyžaduje názov súboru ako parameter konštruktoru.  
Po vytvorení inštancie si pred začatím každej hry zavoláme funkciu startGame()  
V cykle hry je potrebné volať funkciu add(action,reward)  
Po skončení hry zavolať funkciu endGame(epsilon,learningRate)  
Po skončení tréningu/animácie zavolať funkciu saveToFile()  
V konštruktore triedy sa nachádza atribút writeCount ktorý určuje po koľkých hrách sa bude ukladať do súboru.  
Príklad použitia triedy je v súbore priklad.txt  

Trieda Visualizer vyžaduje ako parameter konštruktoru názov .csv súboru, ktorý bol vytvorený pomocou triedy DataHandler.
Následne stačí na vytvorenom objekte triedy Visualizer zavolať metódu visualize_data().
Metóda slúži na zobrazenie grafu skóre, epsilonu a priemeru / kĺzavého priemeru skóre v danej hre.
Metóda má volitelný parameter average, ktorý slúži na zobrazenie priemeru / kĺzavého priemeru v grafe, default False a druhý volitelný parameter
moving_average_threshold, ktorý hovorí o tom koľko posledných hier sa má priemerovať, default 100.

Druhý typ grafu je možné vykresliť metodou visualize_score_time().
Metóda slúži na zobrazenie grafu skóre, času hry a priemeru / kĺzavého priemeru skóre v danej hre.
Parametre metódy sú rovnake ako pri metóde visualize_data().

Tretí druh grafu je možné vykresliť metodou visualize_actions_data().
Metóda slúži na zobrazenie grafu priemerného počtu vykonania jednotlivých akcii počas posledných X hier.
Parameter moving_average_threshold udáva počet posledných hier, ktoré sa berú do úvahy pri počítaní priemerneho počtu akcii.
