#!\bin\bash

#on vérifie que les arguments ont bien été fournis

if [ "S#" -eq 0 ]: then
echo -e "\E[1;31mIL manque les noms d'utilisateurs en argument - Fin du script\E[0m"
exit 1
fi

#Boucle for pour répeter l'action à chaque argument

for user in "$@"; do
id $user >/dev/null

#On fait la comtande id avec l argument, si le code sortie est vrai l utilisateur existe déjà
#Sinon on L'ajoute

if [ $? = 0 ]; then
echo -e "\E[1;31mL'utilisateur $user existe déjà\E[0m"
else
adduser $user

#une fois ajouté on vérifie qu'il existe bien
id $user >/dev/null

if [ $? = 0]; then
echo -e "\E[1;32mL'utilisateur $user à bien été créé\E[0m"
else
echo -e "\E[1;31mLa création de l'utilisateur $user à échouée\E[0m"
fi
done
