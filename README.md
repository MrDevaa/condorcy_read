# 🌟 Application de Gestion de Scrutins

## 🌍 Contexte

Avec quelques amis, vous avez été convaincu par le mouvement de la Civic Tech, dont l'ambition est de proposer des outils numériques pour offrir des méthodes alternatives au vote majoritaire.

Bien que ce dernier soit la méthode la plus répandue (et la plus simple) pour prendre des décisions, en particulier pour les processus politiques locaux et nationaux, il existe depuis très longtemps des approches différentes, plus représentatives, mais aussi plus difficiles à mettre en œuvre manuellement.

🕰️ Parmi celles-ci, on peut compter au moins deux travaux majeurs :

- 📜 Ramon Lull, philosophe catalan, auteur de *De arte electionis* en 1299.
- 🧮 Nicolas de Condorcet, mathématicien français, qui proposa un système électoral plus juste connu sous le nom de « méthode de Condorcet ».

Avec l'essor du vote numérique, ce projet vise à développer une application Python utilisant Flask, permettant d'organiser des scrutins en ligne basés sur ces algorithmes avancés.

## 🎯 Objectifs

1️⃣ Concevoir le modèle des données de l'application.
2️⃣ Développer un prototype permettant l'organisation, le déroulement et l'affichage des résultats d'un scrutin, incluant la sélection de l'algorithme de décision.
3️⃣ Réaliser une interface d'administration pour modérer les scrutins et afficher des statistiques.

## 📋 Cahier des charges

### 📂 Modèle de données

#### 🗳️ Scrutin
- **Question** : Définie par une question et un texte de présentation.
- **Réponses** : Plusieurs options configurées par l'organisateur.
- **Période** : Dates de début et de fin pour la participation.
- **Résultat** : Une réponse préférée identifiée après clôture.

#### 👤Utilisateurs
- **Identification** : Par pseudonyme.
- **Données personnelles** : Conservées pour chaque utilisateur, sauf en cas de suppression.
- **Sécurité** : Non prioritaire, un pseudonyme suffit pour voter.

### 🛠️ Cas d'utilisation

#### Principaux cas d'utilisation

1️⃣ **Accéder à la page d'accueil** : Présente la plateforme et liste les 10 derniers scrutins créés et actifs.
2️⃣ **S'inscrire** : Permet à un visiteur de devenir utilisateur en remplissant un formulaire d'inscription.
3️⃣ **Modifier le profil** : Mise à jour des données personnelles, sauf le pseudonyme.
4️⃣ **Supprimer le profil** : Désactivation d'un profil tout en conservant son pseudonyme pour l'historique.
5️⃣ **Créer un scrutin** : Les utilisateurs peuvent organiser des scrutins avec un minimum de deux options.
6️⃣ **Modifier un scrutin** : Possible tant qu'il n'a pas été rendu public.
7️⃣ **Participer à un scrutin** : Classement des options par ordre de préférence.
8️⃣ **Modifier un vote** : Révision possible tant que le scrutin est ouvert.
9️⃣ **Afficher les résultats** : Les résultats sont disponibles après clôture.
🔟 **Dépouiller un scrutin** : Calcul des résultats pour un scrutin organisé par un utilisateur.
🔢 **Modérer un scrutin** : Les administrateurs peuvent désactiver des scrutins non conformes.
📊. **Afficher des statistiques** : Permet d'analyser la participation et d'obtenir des données détaillées.

### 🔍 Analyse des votes

#### Méthodes d'analyse

1️⃣ **Vote proportionnel**
   - Chaque votant sélectionne une seule option.
   - L'option avec le plus de votes est déclarée gagnante.

2️⃣ **Vote majoritaire**
   - L'option gagnante doit réunir au moins 50% + 1 des voix.
   - Plusieurs implémentations sont possibles.

3️⃣ **Méthode de Condorcet**
   - Classement des options par ordre de préférence.
   - Gestion des équivalences et des abstentions.
   - Algorithme complexe basé sur des cycles et un graphe orienté.

## 📦 Livrables

1️⃣ **Code source** : Archive ZIP contenant tous les fichiers nécessaires à l'application.
2️⃣ **Documentation** : DocStrings Python pour générer une documentation technique.
3️⃣ **Tests (optionnel)** : Couverture des fonctionnalités principales.

## 📚 Ressources

### 🗳️ Systèmes électoraux
- [Systèmes électoraux (Wikipedia)](https://fr.wikipedia.org/wiki/Syst%C3%A8me_%C3%A9lectoral)
- [Méthode de Condorcet (Wikipedia)](https://fr.wikipedia.org/wiki/M%C3%A9thode_de_Condorcet)
- [Observatoire de la Civic Tech](https://civictechobservatory.org/)

### 🐍 Python
- [Flask - Documentation officielle](https://flask.palletsprojects.com/)
- [PyMongo](https://pymongo.readthedocs.io/)
- [PyTest](https://docs.pytest.org/)
- [Faker](https://faker.readthedocs.io/)

### 🗄️ MongoDB
- [MongoDB - Documentation officielle](https://www.mongodb.com/docs/)
