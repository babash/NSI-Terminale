# 📚 Cours de terminale NSI et TP Pokédex

**Le premier chapitre des structures de données, illustré par le jeu Ricochet Robots, et un TP de programmation objet avec des pokémons.** Pour la terminale NSI.

> Les élèves distinguent l'interface d'une structure de données, c'est-à-dire ses primitives, de son implémentation en Python, pour les listes, les files et les piles. Sur un plateau schématique inspiré du jeu Ricochet Robots, ils et elles exécutent à la main de courts programmes qui déplacent les robots, puis écrivent les leurs pour faire jouer les autres groupes. Dans le TP Pokédex, chaque élève crée des pokémons à partir d'une classe `Pokemon`, lui ajoute un attribut et des méthodes, puis fait s'affronter ses pokémons.

## 👉 [Lire et imprimer : babash.github.io/Babash-NSI-SNT/nsi-terminale/fichiers/chapitre1-interface-et-implementation.pdf](https://babash.github.io/Babash-NSI-SNT/nsi-terminale/fichiers/chapitre1-interface-et-implementation.pdf)

**Gratuit · sans compte · à imprimer en A4 · rien n'est enregistré**

Le cours de terminale NSI et le TP Pokédex font partie des [Ressources NSI et SNT](https://babash.github.io/Babash-NSI-SNT/), rubrique [NSI Terminale](https://babash.github.io/Babash-NSI-SNT/nsi-terminale/).

---

## Ce que contiennent les fiches

### Chapitre 1 : interface et implémentation

[Le PDF, 9 pages A4](https://babash.github.io/Babash-NSI-SNT/nsi-terminale/fichiers/chapitre1-interface-et-implementation.pdf) · [les sources LaTeX](Th%C3%A8me%201%20%E2%80%93%20Structures%20de%20donn%C3%A9es/Chapitre%201%20-%20Interface%20et%20impl%C3%A9mentation/)

Le premier chapitre du thème « Structures de données » :
- **les définitions** : structure de données, structure linéaire, interface (les primitives) et implémentation ;
- **les listes** : leurs primitives (insérer, retirer, tester si la liste est vide, compter ses éléments), puis leur implémentation en Python : `len`, les indices positifs et négatifs, `append`, `del` ;
- **8 exercices sur un plateau inspiré de Ricochet Robots** (16 × 16 cases, 4 robots, 17 repères) : un court programme déplace un robot à l'aide d'une liste de directions, et les élèves cherchent sur quel repère il s'arrête ; puis, par groupes de 3, ils et elles écrivent leurs propres instructions pour les autres groupes ;
- **les files (FIFO) et les piles (LIFO)** : enfiler, défiler, tester si la file est vide, compter ses éléments ; leur implémentation avec des listes Python, puis 3 exercices sur le même plateau, avec une file puis avec une pile.

### TP de programmation objet : le Pokédex

[Lire le notebook](https://nbviewer.org/github/babash/NSI-Terminale/blob/main/tp-poo-pokemons/tp-poo-pokemons.ipynb) · [le télécharger (.ipynb)](https://raw.githubusercontent.com/babash/NSI-Terminale/main/tp-poo-pokemons/tp-poo-pokemons.ipynb) · [les données des pokémons (JSON)](https://raw.githubusercontent.com/babash/NSI-Terminale/main/tp-poo-pokemons/pokemon_data_light.json)

Un notebook Jupyter en 4 exercices, autour d'une classe `Pokemon` fournie (nom, numéro, taille, poids, types, statistiques, image et cri) :
1. **Classe, attributs et constructeur** : lire la classe.
2. **Instancier des objets** : créer Herbizarre (Ivysaur), modifier son attaque, ajouter un attribut `level` à la classe.
3. **Créer des méthodes et les appeler** : monter d'un niveau, présenter le pokémon, comparer sa vitesse, trouver les pokémons du même type.
4. **Pour aller plus loin** : créer des pokémons à partir des données de 1 301 pokémons, puis écrire une fonction d'attaque pour les faire s'affronter.

## Pour aller plus loin

### Faire le TP
- Le notebook s'ouvre dans un environnement Jupyter (le fichier vient de Google Colab). Il utilise `requests`, `matplotlib` et Pillow.
- Il est livré sans ses sorties : exécute les cellules dans l'ordre, en commençant par la classe `Pokemon`.
- L'exercice 4 lit `pokemon_data_light.json` : ce fichier doit être dans le même dossier que le notebook.
- La méthode `show()` télécharge l'image et le cri du pokémon : il faut un accès à Internet.

### Modifier le cours
- `main.tex`, à la racine, assemble la page de garde et le chapitre 1. Le dépôt vient d'Overleaf. Le PDF est au format A4 : il se compile depuis la racine du dépôt avec `pdflatex main.tex`, lancé deux fois (pour le nombre de pages), et le français de babel (paquet `texlive-lang-french` sous Debian ou Ubuntu).
- Les schémas du cours sont dans le dossier `BLOB/` du chapitre : en SVG (la source, à modifier) et en PDF (le format lu par pdfLaTeX). Pour refaire le PDF d'un schéma : `rsvg-convert -f pdf -o schema.pdf schema.svg`.
- `tp-poo-pokemons/pokemon_api_tool.py` regroupe des fonctions qui interrogent [PokéAPI](https://pokeapi.co) pour récupérer les noms et les données des pokémons. Lancé comme script (`python3 pokemon_api_tool.py`), il télécharge les données de tous les pokémons, une requête par pokémon, puis écrit `pokemon_data.json` et `pokemon_names.json` dans le dossier courant.

## Contact

Conçu par Babash - NSI Tani Malandi pour les classes de NSI de terminale de l'académie de Mayotte.
Une question, une idée, un bug ? Les [issues GitHub](https://github.com/babash/NSI-Terminale/issues) du dépôt. Toutes les ressources sont sur le site [Ressources NSI et SNT](https://babash.github.io/Babash-NSI-SNT/).

## Licence

- **Le code** (`tp-poo-pokemons/pokemon_api_tool.py`) est sous licence [MIT](LICENSE).
- **Les documents** (le cours, ses sources LaTeX et son PDF, le notebook du TP) sont sous licence [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.fr), sauf ce qui suit.
- **Les schémas du cours** (dossier `BLOB/` : le plateau de jeu, le tableau, l'arbre binaire et les tours de Hanoï, en SVG et en PDF) sont de Babash - NSI Tani Malandi, sous licence [CC BY-SA 4.0](https://creativecommons.org/licenses/by-sa/4.0/deed.fr).
- **L'icône** du dossier `Common_blob/` (`mindblow.png`) vient d'une autre source : elle n'est pas couverte par ces licences.
- **Les données, les images et les cris des pokémons** (les fichiers JSON, et ce que le notebook télécharge et affiche) viennent de [PokéAPI](https://pokeapi.co) : ils ne sont pas couverts par ces licences. « Pokémon » et les noms des pokémons sont des marques de Nintendo.

Tu peux les réutiliser et les modifier, y compris pour tes classes, en mentionnant Babash - NSI Tani Malandi et la licence ; un document modifié se partage sous la même licence. Si tu utilises l'IA pour les modifier, merci de le préciser.
