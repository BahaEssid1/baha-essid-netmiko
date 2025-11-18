Mon Projet Netmiko
* 1 Initialiser un dépôt Git local
  1. Créez un nouveau répertoire prenom-nom-netmiko pour votre projet.
  2. Initialisez un dépôt Git dans ce répertoire.
<img width="745" height="107" alt="1" src="https://github.com/user-attachments/assets/cd65475c-0b39-490d-a409-e50f47984709" />
-II. Ajouter et commiter des fichiers
  1. Créez un fichier README.md et ajoutez-y le titre : Mon Projet Netmiko   
   On a crée une fichier README.md aec la command nano README.md et ajouter le titre : Mon Projet Netmiko
 <img width="955" height="156" alt="2" src="https://github.com/user-attachments/assets/afdb1456-67ac-47c3-8f4b-a32de9a5723f" />

  2. Ajoutez ce fichier à l'index et commitez-le en utilisant le message "Ajout du fichier
README".
  <img width="768" height="205" alt="3" src="https://github.com/user-attachments/assets/771b79bf-8f4d-4af9-b3cb-13c4c89840c3" />

  3. Créez un fichier main.py et ajoutez-y un simple script Python : print("Hello, Git!")
   nano main.py
 
  4. Ajoutez et commitez ce fichier en utilisant le message "Ajout du script Python principal".
  git add main.py
  git commit -m "Ajout du script Python principal"
 
  6. Affichez tous les commits effectués.
  
   git log
-III. Créer et fusionner des branches
  1. Créez une nouvelle branche feature/netmiko pour ajouter une fonctionnalité.
    git branch feature/netmiko
    git checkout feature/netmiko

  3. Modifiez main.py pour inclure une fonction acces_netmiko qui utilise la bibliothèque
     netmiko pour effectuer les opérations suivantes sur un routeur Cisco C8000V :

      nano main.py
      aprés en ajout les code des fonctionnalités

  5. Ajoutez et commitez ces modifications avec le message "Ajout de la fonction
acces_netmiko".
  git add .
  git commit -m "Ajout de la fonction acces_netmiko"

  6. Revenez à la branche principale (main).
  git checkout master

  7. Fusionnez les modifications de la branche feature/netmiko dans main.
 git merge feature/netmiko

-IV. Travailler avec un dépôt distant sur GitHub
  1. Créez un nouveau dépôt sur GitHub (nommez-le prenom-nom-netmiko ).
  <img width="1353" height="387" alt="4" src="https://github.com/user-attachments/assets/dd346ef5-4c9b-427b-a1c2-ca776d40846d" />

  2. Ajoutez ce dépôt GitHub comme dépôt distant.
    git remote add origin https://github.com/BahaEssid1/baha-essid-netmiko
  
  3. Poussez vos commits locaux vers GitHub.
      git push --set-upstream origin master
  4. Allez sur GitHub et vérifiez que les fichiers sont bien présents.
    <img width="1331" height="681" alt="5" src="https://github.com/user-attachments/assets/e284158c-2f29-4bd4-8199-bee0b161c555" />

  5. Créez une nouvelle branche sur GitHub nommée feature/salut
    <img width="1800" height="800" alt="6" src="https://github.com/user-attachments/assets/fb8873be-033d-49aa-acc0-750316514494" />

  6. Sur votre machine locale, récupérez cette nouvelle branche.
     git fetch origin
     git checkout -b feature/salut origin/feature/salut
  
  7. Modifiez main.py pour ajouter une fonction qui dit salut.
     nano main.py
     and after that we make the changes
  
  8. Ajoutez et commitez ces modifications avec le message "Ajout de la fonction dire_salut".
     git add .
     git commit -m "Ajout de la fonction dire_salut"
 
  9. Poussez cette branche vers GitHub.
     git push origin feature/salut
  
  10. Sur GitHub, créez une Pull Request pour fusionner feature/salut dans main.
  11. Acceptez la Pull Request et fusionnez la branche.
  <img width="1137" height="77" alt="7" src="https://github.com/user-attachments/assets/edfaf30a-b739-4b8c-8c3a-819ca3d16493" />

  12. Revenez à la branche main locale et récupérez les dernières modifications.
     git checkout master
     git pull https://github.com/BahaEssid1/baha-essid-netmiko.git
