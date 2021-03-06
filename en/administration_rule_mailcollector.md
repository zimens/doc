Affecter un ticket ouvert par courriel à une entité
===================================================

GLPI implémente un mécanisme de routage des tickets ouverts par
courriel, afin de les créer dans la bonne entité. Celui-ci se base sur
le moteur de règles.

Ce type de règle est accessible depuis le menu Administration \> Règles
\> Règles d'affectation des tickets ouvert par courriel .

Note: si les notifications ne sont pas activées dans la configuration,
le menu n'apparaît pas dans **Règles**.

Les critères disponibles sont des entêtes du courriel (priorité, from,
to, in\_reply\_to), ainsi que les données du ticket (sujet et corps).

Enfin il existe un troisième type de critères qui joue sur des données
propres à l'utilisateur ou à la configuration des entités :

-   **domaine de messagerie connu** : permet de vérifier que le domaine
    de messagerie du courriel envoyé correspond bien à un renseigné dans
    une entité. Ce critère permet d'éliminer par exemple tous les spams
    (messages ne provenant pas de domaines autorisés);
-   **utilisateur : groupe** : vérifie que l'utilisateur GLPI associé à
    l'adresse de messagerie de l'émetteur appartient bien à un groupe
    donné;
-   **utilisateur : nom** : nom de l'utilisateur GLPI associé à
    l'adresse de messagerie de l'émetteur du courriel;
-   **utilisateur possède le profil** : l'utilisateur possède un profil
    donné;
-   **utilisateur possède une seule fois le profil** : l'utilisateur
    possède une seule fois un profil donné. C'est à dire qu'il ne
    dispose pas du profil affecté sur plusieurs entités distinctes;
-   **utilisateur possède un seul profil** : l'utilisateur possède un et
    un seul profil dans GLPI. Si le profil est associé à plusieurs
    entités différentes, alors c'est celle qui est définie comme entité
    par défaut dans les options de personnalisation de l'utilisateur qui
    sera l'entité du ticket. Si aucune n'est définie dans les
    préférences, la règle n'est pas vérifiée.

Les actions sont soit le refus du ticket (avec ou sans notification du
refus à l'émetteur), soit l'import dans une entité (manuel, depuis TAG,
depuis domaine de messagerie, depuis profil de l'utilisateur).

Important: le moteur s'arrête à la première règle vérifiée.

Un exemple d'utilisation du moteur est le suivant :

1.  règle refusant les courriels dont le domaine de messagerie est
    inconnu (non prise en compte des spams);
2.  règle refusant les messages des listes de diffusions;
3.  règles affectant les courriels si l'utilisateur n'a qu'un profil
    (cas des utilisateurs de l'interface simplifiée);
4.  Règle affectant les courriels à une entité si l'utilisateur possède
    un profil particulier (par exemple pour des super administrateurs,
    qui ont accès à toutes les entités, mais sont physiquement dans un
    en particulier).

**Parent topic:** [Gérer les règles
métiers](../glpi/administration_rule.html "Les règles métiers se gèrent depuis le menu Administration > Règles")
