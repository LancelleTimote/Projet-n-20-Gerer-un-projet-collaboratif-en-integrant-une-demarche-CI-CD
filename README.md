# Projet n°20 : Gérer un projet collaboratif en intégrant une démarche CI/CD

![GitHub contributors](https://img.shields.io/github/contributors/LancelleTimote/Projet-n-20-Gerer-un-projet-collaboratif-en-integrant-une-demarche-CI-CD?style=for-the-badge&color=green)
![GitHub language count](https://img.shields.io/github/languages/count/LancelleTimote/Projet-n-20-Gerer-un-projet-collaboratif-en-integrant-une-demarche-CI-CD?style=for-the-badge)
![GitHub repo size](https://img.shields.io/github/repo-size/LancelleTimote/Projet-n-20-Gerer-un-projet-collaboratif-en-integrant-une-demarche-CI-CD?style=for-the-badge)
![GitHub last commit](https://img.shields.io/github/last-commit/LancelleTimote/Projet-n-20-Gerer-un-projet-collaboratif-en-integrant-une-demarche-CI-CD?style=for-the-badge)
![GitHub License](https://img.shields.io/github/license/LancelleTimote/Projet-n-20-Gerer-un-projet-collaboratif-en-integrant-une-demarche-CI-CD?style=for-the-badge)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/timote-lancelle-devweb/)

## :mag: Aperçu

![Aperçu du site web](visuel_projet/visuel_projet.png)

## :bookmark_tabs: Sommaire

<ol>
    <li><a href="#sujet">Sujet</a></li>
    <li><a href="#demandes_respecter">Demandes à respecter</a></li>
    <li><a href="#objectifs_projet">Objectifs du projet</a></li>
    <li><a href="#technologies_utilisees">Technologies utilisées</a></li>
    <li><a href="#prerequis">Prérequis</a></li>
    <li><a href="#installation">Installation</a></li>
    <li><a href="#utilisation_siteweb">Utilisation du site web</a></li>
    <li><a href="#auteurs_contributeurs">Auteurs et contributeurs</a></li>
    <li><a href="#licence">Licence</a></li>
</ol>

## :page_facing_up: 1. Sujet <a name = "sujet"></a>

Comme chaque matin, vous buvez votre café devant BobApp, l’application de votre ami Bob, et vous lisez la blague du jour qui vous fait bien rire.

Ça fait 3 ans que Bob a lancé son application ! Chaque jour le nombre de visiteurs augmente, mais cela devient compliqué pour Bob de gérer cela tout seul. Il a passé le projet sous licence open source, mais peu de personnes se sont investies pour l’instant.

En ouvrant vos e-mails, vous voyez un message de Bob :

"Salut, ça va ?

Je voulais voir avec toi car je n’arrive plus à m’en sortir avec BobApp, il y a de plus en plus d’utilisateurs qui remontent beaucoup de bugs, cela me prend beaucoup de temps pour les reproduire et les corriger.

De plus, les déploiements sont devenus un véritable enfer, cela me prend trop de temps ! Il faut que je valide les pull-requests, récupère le code, lance les tests, builde le projet, vérifie que celui-ci fonctionne, et enfin que je le déploie via FTP…

Actuellement, je développe ce projet sur mon temps libre, et je manque donc de temps pour l'ajout de nouvelles fonctionnalités.

J’ai besoin d’aide – tu pourrais me filer un coup de main ?

Bob"

Après cet e-mail, vous allez faire un tour sur internet, car pour vous son application fonctionne bien, et vous tombez sur les avis.

Vous envoyez un message à Bob lui indiquant que vous êtes prêt à l’aider à gérer et à améliorer son application.

"Salut,

Oui je sais que les avis sont de moins en moins bons sur le web, et je suis ravi que tu aies accepté de m’aider !

Je te joins le code pour mon appli. Il faudrait dans un premier temps que tu mettes en place des workflows Continuous Integration/Continuous Delivery complets sur le projet. Cela m’aidera énormément dans la gestion de mon appli, car cela me permettra d’automatiser plein de fonctionnalités qu’actuellement je réalise manuellement. En outre, le fait d’automatiser des fonctionnalités encouragera plus de gens à participer au développement de l’appli et rapportera de meilleurs commentaires, car cela éliminera des blocages.

Tu vas travailler sur GitHub (et plus précisément GitHub Actions pour les workflows), mais pas sur mon repository. Il faut d’abord que tu travailles sur un repository à toi en privé.

Il faudrait dans un premier temps que la CI/CD :

- valide que les tests passent bien sur une pull request pour pouvoir la valider ;
- permette de lancer les tests, vérifier la qualité du code, builder le projet et créer les images Docker ;
- automatise la génération des rapports de couverture ;
- déploie les conteneurs sur Docker Hub.

Pour le projet : du classique back-end sous Spring Boot en Java 11 et avec un front end en Angular. Il y a très peu de tests mais bon, ils tournent, la génération des rapports doit elle aussi être automatisée !

Bien sûr le projet est dockerisé, tu as un container pour le front et un autre pour le back, toutes les informations se trouvent dans le readme, ça va t’aider pour la mise en place de la CI/CD.

Par contre, je n’ai pas de recul sur la qualité du code. J’entends parler depuis longtemps de SonarQube mais je n’ai jamais essayé ce produit, il faut mettre ça en place via tes GitHub Actions.

J’aimerais également fixer les seuils à respecter (KPI), est-ce que tu peux me faire une proposition ? Je pense notamment au taux de couverture (coverage) minimum à atteindre ou encore quelque chose comme les “New blocker issues” (cf les quality gates de SonarQube mais j’ai pas tout compris, à toi de me dire ce qui est utile).

Une fois que tu auras réussi à mettre en place la pipeline CI/CD, pourrais tu m’envoyer un document explicatif dans lequel tu auras fait une analyse des métriques obtenues mais aussi des “Notes et avis” ? Ce sera une bonne base de travail pour identifier mes prochaines actions à mener.

Transmets-moi ton repository GitHub quand tu auras terminé, on se fera une réunion pour que tu me fasses un brief sur ton travail.

Merci encore !

Bob"

## :memo: 2. Demandes à respecter <a name = "demandes_respecter"></a>

- Mettre en place une pipeline CI/CD comprenant l'automatisation des tests, l'analyse de code via SonarQube / SonarCloud, la création d'images sur Docker en utilisant les GitHub Actions.
- Fournir un document explicatif avec les étapes GitHub Actions, les KPIs proposés, l'analyse des métriques, et les retours utilisateurs.

## :checkered_flag: 3. Objectifs du projet <a name = "objectifs_projet"></a>

- Apprendre à mettre en place une pipeline CI/CD ;
- Apprendre à utiliser les GitHub Actions ;
- Apprendre à utiliser SonarQube / SonarCloud ;
- Apprendre à utiliser Docker.

## :computer: 4. Technologies utilisées <a name = "technologies_utilisees"></a>

- SonarQube & SonarCloud
- Docker
- Git & GitHub
- GitHub Actions

## :exclamation: 5. Prérequis <a name = "prerequis"></a>

Aucun prérequis

## :wrench: 6. Installation <a name = "installation"></a>

Aucune installation

## :question: 7. Utilisation du site web <a name = "utilisation_siteweb"></a>

Tous les fichiers pour la pipeline CI/CD sont dans le dossier .github/workflows, tout se passe sur le repository GitHub dans l'onglet Actions, tout le processus est expliqué dans le document explicatif sur le repository.

## :beers: 8. Auteurs et Contributeurs <a name = "auteurs_contributeurs"></a>

Timoté Lancelle : [GitHub](https://github.com/LancelleTimote) / [LinkedIn](https://www.linkedin.com/in/timote-lancelle-devweb/)

## :page_with_curl: 9. Licence <a name = "licence"></a>

Distribué sous la licence MIT. Voir le fichier [LICENSE](LICENSE) pour plus d'informations.
