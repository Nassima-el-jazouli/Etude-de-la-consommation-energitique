# Etude-de-la-consommation-energitique
## 1 Objectifs
L’objectif de ce projet est d’utiliser la classification non supervisée pour résumer les variations de la consommation d’énergie de 100 appartements, observ´ee toutes les 30 minutes durant 91 jours consécutifs. Plus spécifiquement, on cherche ici à obtenir une classification des jours, uniforme pour l’ensemble des appartements. Une telle classification pourra ˆetre utile, par exemple, dans le cadre de la surveillance d’un réseau d’électricité.
## 2 Données
Pour faciliter leur manipulation, les données sont fournies via les trois tableaux suivants, constitués du même nombre de lignes :
• X (100×91 lignes et 48 colonnes) : chaque ligne correspond à la consommation observée sur
une journée avec un pas de temps de 30 minutes :
X = as.matrix(read.table("http://allousame.free.fr/mlds/donnees/X.txt",header=F))
• APPART (100×91 lignes et 1 colonne) : chaque cellule correspond au numéro de l’appartement :
APPART = as.matrix(read.table("http://allousame.free.fr/mlds/donnees/APPART.txt",header=F))
• JOUR (100×91 lignes et 1 colonne) : chaque cellule correspond au numéro de la journée :
JOUR = as.matrix(read.table("http://allousame.free.fr/mlds/donnees/JOUR.txt",header=F))
Par exemple, pour accéder aux données de l’appartement 1 pour la journée 2, on pourra utiliser la commande plot(X[APPART==1 & JOUR==2,],type="l",lty=1)
Pour faciliter l’analyse, chacune des séries a été passée à l’échelle logarithmique, et centrée.
