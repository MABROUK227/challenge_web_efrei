# Guide d'installation et d'utilisation pour le projet Internet Banking

## Installation de la base de données

1. **Installez la base de données en local** :
   - Importez le fichier `internetbanking.sql` dans votre serveur de base de données (par exemple, via **phpMyAdmin** ou en ligne de commande).

2. **Configurez les fichiers de configuration suivants** :

   - 🛠️ **Fichier `config.php`**
     - **Chemin** : `challenge_web_efrei/admin/conf/config.php`
   
   - 🛠️ **Fichier `pdoconfig.php`**
     - **Chemin** : `challenge_web_efrei/admin/conf/pdoconfig.php`
     - **Exemple de contenu** :
       ```php
       <?php
       $databaseuser = "root";
       $databasepassword = "root";
       $host = "localhost";
       $databasename = "internetbanking";
       $mysqli = new mysqli($host, $databaseuser, $databasepassword, $databasename);
       ```

---

## Connexion à l'interface administrateur

🔒 **Après la configuration de la base de données** :

1. Accédez au **portail administrateur**.
2. Connectez-vous avec les identifiants suivants :
   - **Email** : `admin@mail.com`
   - **Password** : `codeastro.com`

### Interface administrateur

🖥️ Une fois connecté, l'interface administrateur s'affiche. Voici un aperçu des fonctionnalités disponibles :

- 🔎 Visualiser l'ensemble des **dépôts** et des **transferts**.
- ➕ **Créer un compte client**.
- 💰 Assurer les **dépôts** sur le compte principal du client.
- 🔄 **Effectuer des transferts** entre clients.
- 🔑 Changer le **mot de passe**.
- 🖨️ Imprimer l'ensemble des tâches, consulter les **statuts** et le type de virement effectué par chaque client.
- 🚫 **Fermer des comptes** et des profils clients.

> **Remarque** : La création d'un compte client est gérée uniquement par l'administrateur.

---

## Connexion à l'interface client

🔓 **Après la création d'un compte client** par l'administrateur :

1. Rendez-vous sur l'onglet `index.php` et connectez-vous.
2. Exemple d'identifiants client :
   - **Identifiant** : `ma@gmail.com`
   - **Mot de passe** : `azer`

### Interface client

👤 Une fois connecté, le client peut :

- ➕ **Créer plusieurs comptes**.
- 🔄 **Effectuer des transferts d'argent** entre ses différents comptes.
- 📊 **Consulter le statut de ses comptes** et gérer ses paramètres.

### Tableau de bord

📋 En accédant à l'onglet `dashboard`, le client peut **visualiser** et **gérer** ses activités bancaires.

