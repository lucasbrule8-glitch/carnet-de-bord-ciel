***Étape 1 — Se repérer***

**affichez le chemin du dossier courant :**
```
pwd
```
**affichez son contenu, puis avec les fichiers cachés, puis en version longue sans les fichiers cachés, puis en version longue avec les fichiers cachés:**
```
ls /c/Users/Utilisateur/Desktop/test
ls /c/Users/Utilisateur/Desktop/test -a
ls /c/Users/Utilisateur/Desktop/test -l
ls /c/Users/Utilisateur/Desktop/test -la
```
**affichez le chemin du dossier courant ; affichez son contenu, puis avec les fichiers cachés, puis en version longue sans les fichiers cachés, puis en version longue avec les fichiers cachés ; affichez l'aide de la commande ls pour retrouver ces options:**
```
ls --help
```
**déplacez-vous dans votre dossier Documents et affichez son contenu:**
```
cd ../../documents/
ls
```
---
***Étape 2 — Organiser un projet***

**créez le dossier station-meteo , puis, depuis ce dossier et en une seule commande, le brouillon et son sous-dossier data:**
```
mkdir -p station-meteo/brouillon/data
```
**créez en une seule commande les dossiers ;src, tests et docs à la racine de station-meteo :**
```
mkdir src tests docs
```
**créez dans brouillon un fichier main.py contenant la ligne print("Station météo prête"):**
```
cd ./brouillon
touch main.py
echo 'print("Station météo prête")' > main.py
```
**déplacez main.py dans src ,puis le dossier data et son contenu à la racine de station-meteo:**
```
cd ..
mv brouillon/main.py src/
cd ..
mv station-meteo/brouillon/data station-meteo/
```
**supprimez le dossier brouillon:**
```
cd ./station-meteo
rm -r brouillon
```
**exécutez src/main.py avec Python.:**
```
python ./src/main.py
```
---
***Étape 3 — Manipuler le contenu des fichiers***

**créez fichier1.txt contenant Bonjour ! et fichier2.txt contenant Je m'appelle <votre prénom>.:**
```
cd ./docs
touch fichier1.txt
touch fichier2.txt
echo "Bonjour!" > fichier1.txt
echo "Je m'appelle <votre prénom>." > fichier2.txt
```
**créez resultat.txt en concaténant les deux fichiers, puis affichez-le :**
```
cat fichier1.txt fichier2.txt > resultat.txt
cat resultat.txt
```
**ajoutez la ligne Fin du test. à la fin de resultat.txt sans effacer son contenu**
```
echo "Fin du test." >> resultat.txt
```
**copiez resultat.txt en resultat_sauvegarde.txt:**
```
cp resultat.txt resultat_sauvegarde.txt
```
---
***Étape 4 — Retrouver et quitter***

**Affichez la liste des dernières commandes tapées:**
```
history 
```
**Retrouvez une commande précédente avec le clavier, sans la retaper**
```
↑
```
**Depuis Documents, retrouvez tous les fichiers .py contenus dans station-meteo**
```
cd ..
find station-meteo -name "*.py"
```
**Quittez le terminal:**
```
exit
```