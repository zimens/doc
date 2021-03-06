L'interface standard et l'interface simplifiée
==============================================

Selon ses habilitations, l'utilisateur utilise l'**interface standard** ou l'**interface simplifiée**.

L'interface standard
--------------------

C'est l'interface principale de l'application. L'ensemble des modules est disponible.

Figure 1. Menu de l'interface standard
![image](docs/image/interfaceStandard.png)

La page d'accueil de l'**interface standard** fournit une vue synthétique pour accéder rapidement aux éléments actifs (tickets, notes, planning, contrats...).

Elle est découpée en 4 vues :

-   **La vue personnelle** présente les tickets ouverts, rejetés, à traiter, à approuver (dont l'utilisateur connecté est le demandeur) ou ceux sur lesquels cet utilisateur a une interaction en tant que valideur ou technicien (en attente de validation, en cours, à clôturer, en attente). Cette vue lui propose également les problèmes en cours, son planning et les notes disponibles.
-   **La vue groupe** propose les mêmes informations à propos des tickets et des problèmes que la vue personnelle mais en prenant comme référence les groupes auxquels il appartient. Suivant son profil, il aura accès ou non aux tickets pour lesquels ses groupes sont demandeurs.

***Remarque :*** *Pour les vues Personnelle et Groupe, seuls s'affichent les tableaux ayant des informations.*

-   **La vue globale** propose des statistiques sur les tickets et les problèmes en fonction de leurs statuts et sur les contrats en fonction de leur date d'expiration. Elle propose également la vue des derniers ajouts d'objets dans GLPI. Suivant la configuration utilisée, les nouveaux tickets peuvent aussi être présentés dans cet onglet.
-   **Flux RSS** propose le contenu des flux RSS définis (voir [Gérer les flux RSS](index.php?fr/06_Module_Outils/04_Flux_RSS.md "Les flux RSS se gèrent depuis le menu Outils > Flux RSS")).

Figure 2. Accueil ![image](docs/image/vuesStandard.png)

***Remarque :*** *Deux messages de sécurité peuvent être affichés lors de votre première connexion à l'issue de la procédure d'installation. 
Le premier vous invite à modifier les mots de passe des comptes créés par défaut dans GLPI. 
Le second à supprimer le répertoire glpi/install.
Figure 2. Sécurité ![image](docs/image/messageAccueil.png)
Tant que vous n'aurez pas réalisé ces opérations les messages subsisteront.*

Figure 3. Menu de l'interface standard personnalisée
![image](docs/image/GLPI-Interface%20personnalisee.png)

Interface présentée à un utilisateur utilisant l'interface standard, mais n'ayant aucun droit de configuration et de consultation de l'inventaire. Le nombre de menus présents dans la barre de navigation
est ainsi limité.

L'interface simplifiée
----------------------

C'est l'interface la plus restrictive. Elle est destinée aux utilisateurs ayant des habilitations très restreintes sur l'application : helpdesk en libre service. Le nombre de menus disponibles est réduit au minimum. Dans la configuration par défaut, un utilisateur peut, depuis cette interface, uniquement créer des tickets, suivre le traitement de ses tickets, réaliser des réservations, voir les notes ou les flux RSS publiques (ou créer des notes ou flux privés) et consulter la foire aux questions. La page d'accueil propose le nombre de ses tickets suivant leurs statuts ainsi que les sujets de la FAQ les plus populaires et les plus récents.

Figure 4. Menu de l'interface simplifiée
![image](docs/image/interfaceSimplifiee.png)

***Remarque :*** *Le choix de l'interface par défaut ainsi que des différents modules à afficher ou non sont paramétrables dans les profils. Voir [Administrer les profils d'utilisateurs](administration_profile.html "Dans GLPI, administrer les profils peut se faire à partir du menu Administration > Profils.").*

---------
**Sujet parent :** [Utiliser GLPI](index.php?fr/02_Premiers_pas_avec_GLPI/03_Utiliser_GLPI/01_Utiliser_GLPI.md)
