# BIENVENUE DANS NOTRE PROJET

### 📰Projet-sdl3-pong-reinventer✨
Ce projet consiste en jeu de tennis virtuel qui à pour principe de renvoyer la balle pour marquer des points avec des elements interactifs comme les bonus speciaux, les effets visuels, ImGui.

### 📗👾FONCTIONALITE PRINCIPALE 
#### Bonus speciaux
Pour rendre le jeu plus interactif et strategique avec: augmenté la taille de la raquette, ralentir ou accelerer la balle, multiplier la balle, inverser les commandes de l adversaire.
#### Les effets visuels
Pour rendre le jeu plus attrayant comme: les effets lumineux quand la balle touche une raquette, l animation lors du but, couleurs selon l etat du jeu.
#### ImGui
Pour modifier les parametres du jeu pendant qu il tourne sans redemarrer. Il nous aide à: ajuster la vitesse de la balle, changer la taille des raquettes, modifier les couleurs, activer et desactiver des bonus speciaux, tester differentes configurations.

### 🌟📚STRUCTURE DU PROJET 
 MonProjet/
 
├── main.cpp          # Point d'entrée

├── Game.h/cpp      # Logique principale

├── Renderer.h/cpp  # Tout le rendu SDL 

├── UI.h/cpp        # Interface ImGui

└── Utils.h/cpp     # Fonctions helpers 

### COMMANDE DE COMPILATION😏
```cpp
python -u Mon_projet/build.py
```

### COMMANDE DU JEU👾👾

- joueur 1:
   - w : monter
   - s : descendre
- joueur 2:
  - ^ : monter
  -   : descendre
- echap : quitter le jeu

## 📰📰FICHIER DU PROJET

### Mon_projet/Build.py
```cpp
# build.py
import os 
import subprocess 
import sys 

def build_project(): 
    sources = [] 
    for root, dirs, files in os.walk("."): 
        for file in files: 
            if file.endswith(".cpp"): 
                sources.append(os.path.join(root, file)) 
            
    include_dirs = [ 
        "-I.", 
        "-Ithirdparty/SDL3/include", 
        "-Ithirdparty/imgui" 
    ]   

    libraries = [] 
    if sys.platform == "win32": 
        libraries = ["-lSDL3", "-limm32"] 
    elif sys.platform == "darwin": 
        libraries = ["-lSDL3", "-framework Cocoa"] 
    else: 
        libraries = ["-lSDL3", "-ldl", "-lpthread"] 

    cmd = [ 
        "clang++", 
        "-std=c++17", 
        "-Wall", 
        "-g", 
        *include_dirs, 
        *sources, 
        *libraries, 
        "-o",
        "mygame" 
        ] 
    subprocess.run(cmd) 

if __name__ == "__main__": 
    build_project()
```

### Mon_projet/Game.h
```cpp

```

### Mon_projet/Game.cpp
```cpp

```

### Mon_projet/Players.h
```cpp

```

### Mon_projet/Players.cpp
```cpp

```

### Mon_projet/Renderer.h
```cpp

```

### Mon_projet/Renderer.cpp
```cpp

```

### Mon_projet/Ui.h
```cpp

```

### Mon_projet/Ui.cpp
```cpp

```

### Mon_projet/main.cpp
```cpp

```
## 🎗️🎗️CONCEPT APPRIS DANS CE PROJET 

* La programmation modulaire
* Les mathematiques(les vecteures, les positions)
* La SDL3
* La logique algorithmique
* Boucle de jeu

## ✨✨AUTEUR✨

Projet realise par MARILEE EMMANUELLE dans le cadre d'un projet academique

## 
