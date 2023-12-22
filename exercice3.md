# Checkpoint1

**Donne une ligne de commande bash qui permet de lister la liste des utilisateurs d'un système Linux**    
cut -d: -f1 /etc/passwd
  

**Quelle commande bash permet de changer les droits du fichier myfile en rwxr—r-- ?**  
sudo chmod 744 myfile
  
**Quelle est la différence entre une variable d'environnement et une variable locale dans un script Bash, et comment pouvez-vous les définir et les utiliser ?**  
Une variable environnement est intégré au shell et peut etre appelé partout  
une variable locale est une variable qui ne fonctionnera que dans l'espace ou elle à été créer comme un script

**Expliquez comment fonctionne la structure de contrôle "if" dans Bash. Donnez un exemple concret de son utilisation pour prendre une décision basée sur une condition dans un script Bash.**  
  La commande IF permet d'effectuer différentes commandes lorsque certaines conditions sont remplis ou non  
  par exemple :   if [ $1 < 1 ]; then  
                    echo "$1 est plus petit que 1"  
                  else  
                    echo" $1 est plus grand ou egal à 1"  
                  fi  
  ici $1 représente le premier argument donné lors du lancement du script. Si cette argument est plus petit que 1 alors on réalise le prmeier "echo" sinon on fait le deuxième  



**Donne la(les) ligne(s) de commande(s) bash pour afficher le texte suivant :**  

echo 'Malgré le prix élevé de 100$, il a dit "Bonjour !" au vendeur :  
- "Bonjour est-ce que ce clavier fonctionne bien ?"  
- "Evidemment ! On peut tout écrire avec, que ce soit des pipe | ou bien des backslash \\ !"  
- "Même des tildes ~ ?"  
- "Evidemment !"'  
ou : echo -e 'Malgré le prix élevé de 100$, il a dit "Bonjour !" au vendeur :\n- "Bonjour est-ce que ce clavier fonctionne bien ?"\n- "Evidemment ! On peut tout écrire avec, que ce soit des pipe | ou bien des backslash \\ !"\n- "Même des tildes ~ ?"\n- "Evidemment !"'

**Quelle commande te permet de mettre en avant le processus gedit ?**   

jobs -l | grep gedit

**7. Quels matériels réseaux sont sur la couche 2 et la couche 3 du modèle OSI ? Donne leurs spécificités.**  
En couche 2 on rerouve les commutateurs comme les switch qui vont permetter à plusieurs machine d'un même réseau de pouvoir communiquer entre elles à condition qu'elles soient toutes brannchés sur le commutateur  
En couche 3 on retrouve les routeurs comme les box internet qui vont permettre aux machines du réseau de communiquer avec d'autre réseau via une "passerelle"  


**8. Quels sont les équivalent PowerShell des commandes bash cd, cp, mkdir, ls.**
|  bash     | Powershell  |
|-----------|-------------|
|   cd      | Set-Location|
|   cp      | Copy-Item   |
|  mkdir    | New-item    |
|    ls     | dir         |  

**9. Dans la trame ethernet, qu'est-ce que le payload ?**  
Le playload correspond aux données utiles c'est à dire les infos principales de la communications

**10. Pourquoi les classes IP sont remplacées par le CIDR ?**  
Le CIDR est apparu suit aux pénuries d'adressages des classes IP. Le CIDR est plus flexible et permet une allocation plus efficace des adresses IP
