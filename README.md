# Truckers - Application de Gestion des Messages

Ce projet de 3ème année de BUT Informatique a pour but de créer un service fonctionnant sous Android avec le langage Kotlin.
Ce service a pour but de traquer les messages de chauffeurs de camions liés à leurs itinéraires, rendez-vous, livraisons, etc.

## Ajout du Fichier Défaut

Pour que le service puisse se lancer, il faut donner à l'application un fichier défaut.json (contenant minimum un numéro admin par défaut).

1. Ouvrez un gestionnaire de fichiers sur votre téléphone.

2. Accédez au répertoire de téléchargements.

3. Placer le fichier defaut.json

4. Lancer l'application, après avoir validé les permissions pour le stockage ainsi que les sms, le service devrait se lancer et créer un fichier logcat.txt dans le même répertoire que le fichier defaut. 

Le fichier "defaut.json" contient les configurations par défaut nécessaires pour le bon fonctionnement de l'application. Veillez à ne pas modifier ce fichier de manière inappropriée pour éviter tout problème de configuration.
Vous pouvez relancer l'application, le service va se lancer et rester actif.

---

<div style="display: flex; justify-content: space-between;">
    <img src="https://github.com/Taukix/Truckers/blob/main/ReadMe_Images/Logo.png" width="49%" height="400px;">
    <img src="https://github.com/Taukix/Truckers/blob/main/ReadMe_Images/Fonctionnement.png" width="49%" height="400px;">
</div>

---

## Utilisation de l'Application

1. **Recevoir des Messages :**
   - Le service récupère automatiquement les messages reçus par les chauffeurs.
   - Les messages valides sont stockés, tandis que les messages invalides sont ignorés.

2. **Gérer les Messages :**
   - Les messages stockés seront synchronisés dans une API REST afin d'avoir un historique des messages reçus côté Admin.

## Exemples de Messages Validés

- **Rendez-vous :** RDV 4 rue Pasteur 18h00
- **Livraison :** LIVRAISON prévue le 4 janvier

## Exemple de Message Invalide

- Bonjour, pouvez-vous m’indiquer votre position ? Pouvez-vous me répondre maintenant ?

## Configuration Administrative

Les administrateurs peuvent configurer l'application en utilisant des messages de configuration spécifiques.

- **Ajout de Numéro :** CONFIG Ajout numéro 011111111111
- **Suppression de Numéro :** CONFIG Suppression numéro 011111111111
- **Ajout de Mot-clé :** CONFIG Ajout mot-clé RENDEZ-VOUS
- **Suppression de Mot-clé :** CONFIG Suppression mot-clé RENDEZ-VOUS
- **Ajout d'Administrateur :** CONFIG Ajout administrateur 0453627283
- **Suppression d'Administrateur :** CONFIG Suppression administrateur 023923492

## Stockage des Messages

Les messages sont stockés dans le répertoire `/data/data/com.unilim.iut.truckers/files`. Ils sont répartis dans deux fichiers distincts en fonction de leur validité. Chaque jour, de nouveaux fichiers sont créés pour minimiser les risques de perte d'informations.

1. Ouvrez le device explorer sur Android Studio.

2. Accédez au répertoire `/data/data/com.unilim.iut.truckers/files`.

3. Vous y trouverez les fichiers `messagesValides-date` et `messageInvalides-date`.

4. Pour consulter les messages ouvrez les fichiers avec un éditeur de texte.

## Consulter les Logs

Pour vérifier le bon fonctionnement du service, vous pouvez consulter les logs enregistrés dans le fichier "logcat.txt" sur votre téléphone, accessible dans votre répertoire de téléchargements.

1. Ouvrez un gestionnaire de fichiers sur votre téléphone.

2. Accédez au répertoire de téléchargements.

3. Recherchez le fichier "logcat.txt" et ouvrez-le avec un éditeur de texte.

4. Vous verrez les détails des actions du service en réponse à la réception des messages.

## Compétences

Le développement de cette application avec Android Studio en Kotlin au sein d'une équipe de 6 personnes a sans aucun doute permis le développement de compétences variées et essentielles dans le domaine de l'informatique. Voici comment ce projet a influencé le développement de compétences spécifiques :

### Réaliser un Développement d'Application

_Architecture Android :_ 

- La conception et la mise en œuvre d'une architecture Android robuste ont été nécessaires pour garantir la fiabilité, la maintenabilité et la scalabilité de l'application.

_Programmation en Kotlin :_ 

- Le développement de l'application en utilisant Kotlin a offert une opportunité d'apprendre et de maîtriser ce langage moderne pour le développement d'applications Android.

_Intégration de Services Système :_ 

- L'application impliquant la récupération de messages du téléphone d'un camionneur a nécessité l'intégration avec des services système d'Android.

### Optimiser des Applications Informatiques

_Optimisation de la Consommation de Ressources :_ 

- L'optimisation de la consommation de la batterie, de la mémoire et du processeur a été un point crucial pour garantir que l'application fonctionne de manière efficace et fluide sur les périphériques des camionneurs.

### Travailler dans une Équipe Informatique

_Collaboration sur le Code :_ 

- La collaboration avec une équipe de 6 personnes a permis une division des tâches efficace et la résolution conjointe des problèmes rencontrés pendant le développement.

_Gestion de Version avec Git :_ 

- Travailler avec Git comme système de contrôle de version a renforcé les compétences liées à la collaboration sur le code, à la gestion des conflits et à la synchronisation du travail d'équipe.

### Gestion des Données de l’Information

_Traitement des Messages :_ 

- La gestion des messages reçus a impliqué la manipulation et le traitement de données en temps réel, mettant en œuvre des mécanismes de filtrage basés sur des mots clés.

_Stockage des Données :_ 

- Le stockage efficace des messages filtrés ou non filtrés, dans des fichiers au format JSON, a été une compétence améliorée lors de ce projet.

### Conduite d’un Projet

_Planification du Projet :_ 

- La planification du projet, y compris la définition des fonctionnalités, l'affectation des tâches et l'établissement de jalons, a été une partie essentielle du processus de développement, notamment grâce au logiciel YouTrack.

_Gestion du Temps :_ 

- La gestion efficace du temps a été cruciale pour respecter les délais et maintenir la qualité du projet.

### Usages des Outils Numériques

_Android Studio :_ 

- L'utilisation d'Android Studio comme environnement de développement intégré a été une compétence clé à acquérir pour le développement d'applications Android.

### Expression et Communication Écrites et Orales

_Documentation du Code :_ 

- La documentation du code a été une activité fréquente pour expliquer la logique du code, les choix d'implémentation et les mécanismes de filtrage.

_Communication au Sein de l'Équipe :_ 

La communication orale et écrite au sein de l'équipe, lors de réunions régulières et par le biais de canaux de communication numérique, a été essentielle pour coordonner les efforts.

---

En conclusion, le développement de cette application a permis de développer une gamme étendue de compétences, allant de la conception et du développement technique à la gestion de projet, en passant par la collaboration au sein d'une équipe.








