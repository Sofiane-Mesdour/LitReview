# LitReview

Développez une application Web en utilisant Django.

Dans le cadre de la formation Open Classrooms(/https://openclassrooms.com) "DA Python", 9e projet
## Création d'un environnement virtuel, téléchargement et exécution du programme:

Vous avez besoin de : 
                    - Python 3 (testé sur 3.9.5).
                    - Git.
                    - venv installés sur votre machine.

* Sous Linux ou macOS :
```bash
git clone https://github.com/Sofiane-Mesdour/LitReview
cd LitReview
python3 -m venv env
source env/bin/activate
pip install -r requirements.txt
cd LitReview
python manage.py runserver
```

* Sous Windows:
```bash
git clone https://github.com/YoannDeb/LitReview.git
cd LitReview
python -m venv env
env\Scripts\activate
pip install -r requirements.txt
cd LitReview
python manage.py runserver
```

Vous pouvez alors accéder localement à LitReview à l'adresse suivante : http://127.0.0.1:8000


### Consultation d'exemples :

Un exemple db.sqlite3 est inclus dans le référentiel.
Il contient des utilisateurs fictifs, des tickets et des critiques.
Le mot de passe de tous les utilisateurs est leur nom d'utilisateur.
Vous pouvez utiliser l'utilisateur sofiane, mot de passe sofiane, qui est administrateur du site (peut accéder à http://127.0.0.1:8000/admin).
Vous pouvez alors consulter tous les utilisateurs dans sa page de suivi, ou dans l'interface d'administration, ou créer de nouveaux utilisateurs.

List of example users:

* alpha				
* beta				
* delta				
* epsilon				
* eta				
* gamma				
* zeta

### Réinitialisation de la base de données :

Supprimez simplement le fichier db.sqlite3, puis entrez la commande suivante dans un terminal du dossier de l'application avec l'environnement activé :

```
python manage.py migrate
```


Si vous souhaitez recréer un utilisateur admin, saisissez un terminal dans le dossier de l'application avec l'environnement activé :

```
python manage.py createsuperuser 
```

Ensuite, remplissez le nom d'utilisateur, l'e-mail et le mot de passe deux fois lorsqu'on vous le demande.

## Comment utiliser l'application ?

### Authentification :

Si vous n'êtes pas connecté, vous serez redirigé vers la page de connexion.
Là, vous pouvez vous connecter avec votre nom d'utilisateur et votre mot de passe ou créer un compte en utilisant l'onglet "inscription".

### Flux:

La page "Flux" est votre flux principal où vous verrez tous vos messages et tous les messages de vos utilisateurs suivis, y compris les tickets et les avis, triés par heure de publication (le plus récent en premier).
Vous pouvez créer un nouveau ticket 
        (c'est-à-dire demander une critique de livre) en cliquant sur le bouton "Demander une critique".
Vous pouvez créer un nouvel avis 
        (c'est-à-dire créer un ticket et l'avis associé) en cliquant sur le bouton "Créer une critique".
Vous pouvez créer une critique en réponse à un ticket en cliquant sur le bouton "Soumettre une critique" dans un ticket non encore répondu auquel vous souhaitez répondre.

### Mes posts:

Ici vous pouvez voir tous vos messages précédents sur le site.

Vous pouvez modifier une publication (ticket ou avis) en cliquant sur le bouton "Modifier".
Vous pouvez supprimer une publication (ticket ou avis) en cliquant sur le bouton "Supprimer".

Attention, si vous supprimez un ticket et qu'une réponse existait, le ticket et l'avis seront supprimés.

### Abonnements:

Ici, vous pouvez consulter et gérer vos suivis et abonnés.

#### Section de recherche :

Vous pouvez rechercher des utilisateurs à suivre :
* Tapez le nom exact de votre follow, il sera ajouté à vos followers.
* Tapez une partie du nom pour voir toutes les correspondances dans la base de données des utilisateurs et cliquez sur le bouton "s'abonner" devant l'utilisateur que vous souhaitez ajouter à vos abonnés.
* Cliquez sur "Montrer tous les utilisateurs auxquels je ne suis pas déjà abonné" pour afficher tous les utilisateurs existants que vous ne suivez pas encore. Cliquez ensuite sur le bouton "s'abonner" devant l'utilisateur que vous souhaitez ajouter à vos followers.


### Abonnements:

Vous y verrez tous les utilisateurs que vous suivez réellement.
Vous pouvez cliquer sur le bouton "Se désabonner" devant l'utilisateur que vous souhaitez désabonner.

### Abonnés:

Ici, vous pouvez voir tous les utilisateurs qui vous suivent.
Vous pouvez les suivre si vous ne le faites pas déjà en cliquant sur le bouton "Ajouter à mes abonnements" devant l'utilisateur que vous souhaitez suivre.

## Se déconnecter du compte

Vous pouvez fermer votre session en cliquant sur cette entrée de menu.
Vous serez redirigé vers la page de connexion.
