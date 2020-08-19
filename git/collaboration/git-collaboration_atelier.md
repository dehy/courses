# Collaboration avec git et GitHub

# À Propos

- **Auteur** [Arnaud de Mouhy](https://github.com/dehy)
- **License** Creative Commons BY-NC-SA [![Licence Creative Commons](https://i.creativecommons.org/l/by-nc-sa/4.0/80x15.png)](http://creativecommons.org/licenses/by-nc-sa/4.0/)

## Objectif pédagogique

Arriver à travailler en équipe sur un projet commun, en respectant les bonnes pratiques git et en utilisant les outils fournit par GitHub.

## Pré-requis

Avoir déjà travailler sur un dépôt git local et synchronisé avec GitHub.

## Avant Propos

Afin de se concentrer sur les commandes git et le processus de collaboration, nous n’allons pas utiliser des sujets techniques (comme HTML/CSS ou Python) comme base. Nous allons faire un atelier d’écriture ! Vous pouvez par exemple imaginer une suite à votre livre, film ou série préférée. Je vous ai mis des exemples de sujets dans les ressources ci-après. Pour le déroulé de l'atelier, je prendrai comme exemple la réécriture des saisons 7 & 8 de Game of Thrones.

## Ressources

- [15 idées pour atelier d’écriture chez soi](https://www.ficellesdauteur.fr/idees-pour-atelier-decriture/)
- [Managing access to your personal repositories](https://docs.github.com/en/github/setting-up-and-managing-your-github-user-account/managing-access-to-your-personal-repositories)
- [About pull requests](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/about-pull-requests)
- [Requesting a pull request review](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/requesting-a-pull-request-review)
- [Merging a pull request](https://docs.github.com/en/github/collaborating-with-issues-and-pull-requests/merging-a-pull-request)

## Atelier

### Introduction

Faire des groupes de 2, de préférence par groupes mixtes avec une personne un peu plus expérimentée sur git que la seconde. Essayez au maximum de travailler au travers des outils numériques, comme si vous travailliez à distance.

Dans votre groupe, désignez une personne qui sera le « Product Owner » (PO). Cette personne est le/la responsable du projet et décide de sa direction, tout de même en concertation avec l’autre membre.  
_Dans tout projet, il y a généralement un « responsable » en charge d’arbitrer les décisions. Nous l'appelons ici PO, terme employé dans les méthodes Agile. Il prend les avis de l’équipe, les synthétise et prend les décisions. Il a généralement la « vision » du projet et les objectifs en tête._

Nous choisissons de travailler en équipe avec le workflow git de type « Feature Branch avec Pull Request » (voir Ressources "About pull requests").  
_Une feature (fonctionnalité) est ici employé dans un sens non strict. Une feature sera donc un ensemble logique de code ou de configuration qui ajoute du code, corrige une erreur ou améliore du code existant. L’idée est d’utiliser votre jugement et garder les changements à un problème logique unique._

Dans les instructions de cet atelier, le nom de la personne concernée précèdera l'instruction. Les actions réalisables en parallèles seront dans le même point, avec des sous-points. Sinon, nous considérerons que les actions suivantes devront attendre la fin de l’action précédente (1, 2, 3, ...)

### Préparation

1. [PO] - Créer le dépôt sur GitHub.com - 10min  
   _Le modèle de développement collaboratif sous git est très très généralement un modèle en « hub » (ou « en étoile »). Même si git peut fonctionner de manière entièrement décentralisée, un modèle avec un point central (le hub) reste plus simple en terme d’organisation des équipes. Ce hub est donc le référent, et est donc à créer en premier. Ici, notre hub sera sur GitHub, mais nous aurions très bien pu le faire chez bitbucket, gitlab, framagit, etc…_

2. [PO] Ajouter le deuxième développeur comme contributeur en lecture/écriture a votre projet. Ajoutez moi également sur votre dépôt (username `dehy` sur github). - 15min  
   _Voir Ressources "Managing access to your personal repositories". Sur les hub, vous avez différentes offres. Comptes personnels ou comptes entreprises. En compte personnel (bien souvent gratuit), vous êtes propriétaire du projet mais pouvez inviter des collaborateurs extérieurs. En compte entreprise (souvent payant), l’entreprise (ou organisation) est propriétaire et vous pouvez créer des équipes et assigner ces équipes aux dépôts._

3. [PO & dev] Cloner le dépôt sur chacune de vos machines. - 10min  
   _Vous avez maintenant chacun une copie locale du dépôt central. Il est vide. Vous êtes prêts à le remplir de contenu._

4. [PO & dev] Il est temps pour une réunion de travail ! - 45min  
   _L'objectif est d'arriver à un concensus sur le sujet et l'objectif général du projet d'écriture. Quels personnages ? Quelle fin globale ? Combien de saisons ? Quelle fin pour chaque saison ? Pour s'aider à lister les tâches à faire, nous allons utiliser les "Issues" GitHub. Chacun de vous se rend sur l'onglet "Issues" de votre projet sur github.com. Créer des nouvelles issues avec les titres suivants (développer la description comme bon vous semble) :_  
   * Définir le sujet dans le README
   * Écrire 4 idées de scéanario à débattre
   * Développer les personnages
   * Résumé S7E1
   * Résumé S7E2
   * ...
   * Résumé S8E10

    _Ces issues vont nous servir de fil rouge pour s'organiser. N'hésitez pas à ajouter autant d'issues que vous le souhaitez. Il s'agit ici de planifier le travail à réaliser, garder un cap. Cela reste une des étapes les plus importantes._

### Travail en branches

1. [PO] Créer une branche git nommée "feature/ajout_sujet" puis y faire un checkout. Créer ou modifier le fichier README.md pour y ajouter le sujet (ex. "Réécriture des saisons 7 et 8 décevantes de GoT"). Committer puis pusher cette nouvelle branche.
2. 
   * [PO] Créer une branche git nommée `feature/idees_scenarios_po` (`po` à remplacer par votre nom bien sûr) puis y faire un checkout. Créer un fichier `scenarios.md` et y noter plusieurs idées de scénarios. Committer puis pusher cette nouvelle branche.
   * [dev] Créer une branche git nommée `feature/idees_scenarios_dev` (`dev` à remplacer par votre nom bien sûr) puis y faire un checkout. Créer un fichier `scenarios.md` et y noter plusieurs idées de scénarios. Committer puis pusher cette nouvelle branche.

### Pull Requests

1. 
   * [PO] Rendez-vous sur github.com sur la page de votre projet, puis dans l'onglet "Pull Requests".  
     Cliquer sur "New Pull Request". Dans l'entrée déroulante `base:`, vérifier que la branche `master` est bien sélectionnée.  
     Sélectionner la branche `feature/ajout_sujet` dans l'entrée déroulante `compare:`.  
     Cliquer ensuite sur `Create Pull Request`.  
     Donner un titre à la PR (ex. Ajout du sujet), mettre en commentaire le numéro de l'issue que va régler cette PR (ex. #1) puis cliquez sur `Create Pull Request`.  
     Répéter l'opération pour la branche `feature/idees_scenarios_po`.
   * [dev] Rendez-vous sur github.com sur la page de votre projet, puis dans l'onglet "Pull Requests".  
     Cliquer sur "New Pull Request". Dans l'entrée déroulante `base:`, vérifier que la branche `master` est bien sélectionnée.  
     Sélectionner la branche `feature/idees_scenarios_dev` dans l'entrée déroulante `compare:`.  
     Cliquer ensuite sur `Create Pull Request`.  
     Donner un titre à la PR (ex. Idées de scénarios), mettre en commentaire le numéro de l'issue que va régler cette PR (ex. #1) puis cliquez sur `Create Pull Request`.

   _Vous venez de créer en tout 3 pull requests. Une Pull Request est une demande de fusion d'une branche vers une autre, réalisée sur le dépôt distant (ici github). Dans le workflow "Feature Branch avec PR", la PR sert à un développeur à signaler aux autres membres de l'équipe que son travail sur une branche est terminé et est prêt à être intégré à la branche principale du projet (la branche master). Maintenant que les demandes sont faites, il faut qu'elles soient validées, puis effectivement fusionnées._

### Code Review

_Pour chaque PR, au travers des différents onglets (Conversation, Commits, Files changed), vous pouvez discuter de la PR, voir quelles commits ont été faits (il peut y en avoir plusieurs) et enfin quels fichiers ont été modifiés et quelles sont les modifications. Vous pouvez surtout commenter le travail de l'autre personne au travers de la "Code Review". C'est une bonne pratique._

1. [PO & dev] Retourner sur chaque PR que vous avez créé, puis dans le menu de droite, choisir votre collaborateur comme "Reviewer".
2. [PO & dev] Pour chaque PR de votre collaborateur, aller dans l'onglet `Files Changed`. Lisez les changements effectués par votre collaborateur, puis cliquer sur `Review changes`. Choisissez l'option `Comment`, `Approve` ou `Request changes` selon le besoin, puis cliquez sur `Submit review`.

_Les 3 PR ont maintenant été validées par un autre membre de l'équipe. Il reste à les intégrer au dépôt principal. C'est généralement le rôle du PO ou du "Lead developer" (développeur principal)._

### Merger les Pull Requests

[PO] Pour chaque PR, cliquer en bas de la conversation sur "Merge pull request".  
_Les commits inclus de chaque pull request sont mergés à la branche principale, mais directement sur le dépôt central. La branche master sur le dépôt central va contenir maintenant plusieurs nouveaux commits que vous n'avez pas sur vos copies locales._

### Récupérer les changements en local

[PO & dev] sur votre machine locale, retournez maintenant sur votre branche master (avec un checkout), puis faites un pull pour récupérer les changements. Vous pouvez maintenant, à partir de cette branche master à jour, créer de nouvelles feature branches !

### Nettoyage

_Maintenant que les features branches ont été mergées sur la branche principale, ces feature branches ne sont plus nécessaires._  
1. [PO & dev] Supprimer vos features branches locales.
2. [PO] Supprimer les features branches mergées sur le dépôt central.
3. [PO & dev] Une fois les branches supprimées, allez dans les issues que vous venez de terminer et cliquez sur "Close issue" !

### Un jour sans fin

Retourner à la liste des issues, sélectionner une nouvelle issue sur laquelle vous souhaitez travailler, puis recommencez à partir de la section "Travailler en branches".