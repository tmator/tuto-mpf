# Installation

Pour installer MPF il vous faudra un ordinateur exécutant l'un des système d'exploitation suivant :

-   Windows 10/11 (64-bit only)
-   macOS 10.14 ou plus (Intel & Apple Silicon)
-   Linux (64-bit)
-   Raspberry PI

**Actuellement Python 3.12 n'est pas totalement validé mais fonctionnel avec MPF, si vous avez des déboires avec cette version n'hésitez pas à les faire remonter.**

## Windows

En premier lieu, il faut installer Python 3.11 qui est disponible sur leur site : https://www.python.org/ftp/python/3.11.0/python-3.11.0-amd64.exe
Exécutez le programme d'installation, choisissez l'option « Personnaliser l'installation » et assurez-vous de cocher la case « py launcher » et « pip ». (Les autres n'ont aucune importance.) Ensuite, sur l'écran suivant, cochez la case « Ajouter Python aux variables d'environnement ». Cliquez ensuite sur « Installer ».

Maintenant, il faut créer un environnement virtuel Python, cela permet de pouvoir utiliser différents projets Python sans avoir d'impact sur les versions des dépendances de ces projets.

On crée un dossier (par exemple "mpfenv" dans Documents), puis on ouvre un terminal et on tape la commande suivante :
```
python3 -m venv C:\Users\tmator\mpfenv
```

Nous allons maintenant activer l'environnement  avec la commande suivante :

```
C:\Users\tmator\mpfenv\Scripts\activate.bat
```
Nous pouvons maintenant installer MPF (ici nous utilisons l'option --pre pour installer la version 0.8)

```
pip install mpf --pre
```
Voilà, MPF est installé.

## MAC OS

Téléchargez python sur le site officiel (3.12) https://www.python.org/downloads/macos/ et installez le.

Maintenant, il faut créer un environnement virtuel Python, cela permet de pouvoir utiliser différents projets Python sans avoir d'impact sur les versions des dépendances de ces projets.

On ouvre un terminal et on tape la commande suivante pour installer l'environnement dans le répertoire utilisateur:
```
python3 -m venv ~/mpfenv
```

Nous allons maintenant activer l'environnement  avec la commande suivante :

```
  source ~/mpfenv/bin/activate
```
Nous pouvons maintenant installer MPF (ici nous utilisons l'option --pre pour installer la version 0.8)

```
pip install mpf --pre
```
Voilà, MPF est installé.

## Linux

Installez Python 3.12 suivant les instructions de votre distribution

Maintenant, il faut créer un environnement virtuel Python, cela permet de pouvoir utiliser différents projets Python sans avoir d'impact sur les versions des dépendances de ces projets.

On ouvre un terminal et on tape la commande suivante pour installer l'environnement dans le répertoire utilisateur:
```
python3 -m venv ~/mpfenv
```

Nous allons maintenant activer l'environnement  avec la commande suivante :

```
  . ~/mpfenv/bin/activate
```
Nous pouvons maintenant installer MPF (ici nous utilisons l'option --pre pour installer la version 0.8)

```
pip install mpf --pre
```
Voilà, MPF est installé.

[configuration](Configuration.md)
