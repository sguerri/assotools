# Outils pour associations

[![License: ISC](https://img.shields.io/badge/License-ISC-yellow.svg)](https://spdx.org/licenses/ISC)

> Comptabilité (très) simplifiée  
> Suivi des adhésions (simple)  
> Publipostage des reçus fiscaux


## Qu'est-ce ?

Suite à la réalisation de ces fichiers pour l'association [Reseau Salariat](http://www.reseau-salariat.info/), l'on m'a demandé si je pouvais les mettre à disposition pour d'autres associations... donc les voilà !

L'objectif de ces fichiers est de faciliter le suivi comptable des petites associations : avoir un outil simple à prendre en main qui fait le juste nécessaire pour suivre le budget et les dépenses.

**Important:** Même si ces fichiers peuvent servir de base, ils ne seront probablement pas adaptés à votre activité, notamment du fait que la comptabilité de RS est très simple. J'ai eu l'occasion, pour une autre association, de créer un fichier plus complet ; je le mettrai peut-être ici un jour si nécessaire.

*Le mieux à mon sens reste de toute façon d'analyser les besoins spécifiques de chaque structure afin d'adapter les outils au fonctionnement, et non l'inverse.*


## Notes générales sur les fichiers

Habituellement, je saisis des commentaires sur la première ligne des tableaux afin d'indiquer la donnée qui doit être saisie. Si plus de documentation est nécessaire, merci de me contacter.

Je travaille uniquement sous [LibreOffice](https://fr.libreoffice.org/), d'où le format des fichiers. Si vous souhaitez les utiliser dans d'autres logiciels, les fonctions d'export de LibreOffice permettent de les convertir. Il se peut néanmoins que certaines mises en page soient ainsi modifiées.

**Codes couleurs usuels :**
- Fond vert clair : formules
- Fond bleu clair : cellules avec sélection de valeur dans un menu déroulant
- Fond jaune clair ou blanc: saisie manuelle


## Comptabilité (très) simplifiée

Le fichier **compta_simple.ods** permet de saisir dans une page les transactions de l'année et de créer automatiquement un compte de résultat ainsi qu'un suivi analytique du budget.

Nous sommes ici sur une comptabilité de trésorerie. Lors de l'établissement du bilan comptable de fin de période, un ajustement doit être réalisé des créances non encaissées et des dettes non payées.

Ce fichier ne permet pas de comparer les enregistrements avec les comptes en banque. J'avais réalisé cela pour une autre association mais cela n'était pas nécessaire ici. Une autre version de fichier serait nécessaire.

Le plan comptable intégré ne comprend que les quelques comptes nécessaires ici ; il est nécessaire de l'adapter pour d'autres usages. Cela impacte alors la mise en page des rapports.


## Suivi des adhésions

Le fichier **compta_adhesions.ods** est une version améliorée de compta_simple dans laquelle il est possible de saisir les dons / adhésions / abandons de frais des adhérent-es. 

Cependant pour les associations ayant de nombreuses personnes adhérentes, il peut être intéressant (bien que plus complexe) d'envisager un outil spécifique comme [Galette](https://galette.eu/site/fr/). Une version hébergée est peut-être disponible chez un [hébergeur local](https://chatons.org/).


## Publipostage des reçus fiscaux

Le fichier **reçus_fiscaux.odt** permet de faire du publipostage des reçus fiscaux, sur la base des données présentes dans compta-adhesions.

*Note 1 : L'affichage de la ligne dons n'est effectué que si le montant est positif*

*Note 2 : Penser à faire un filtre, au moment du publipostage, sur les personnes ayant une cotisation non nulle. Cela évitera la production de reçus vides inutiles.*


Fonctionnement :
- Vérifier que LibreOffice est bien installé
- Vérifier que LibreOffice Base est bien installé
- Le fichier de compte doit être nommé `compta_adhesions.ods` et être placé dans le même dossier que le fichier de reçus fiscaux (sinon il faut refaire les liens de variables dans le modèles)
- Dans LibreOffice Writer :
    + la barre d'outils `Mail Merge` permet de réaliser le publipostage (nom de menu potentiellement différent en français)
    + si le nom du fichier de comptabilité (ods) a été modifié, cliquer sur `Mail Merge Wizard` puis sur `Exchange Database` pour aller sélectionner le nouveau fichier ods en tant que source de données pour les reçus
    + sinon en cliquant sur l'icône de base de données violet `Data sources` la table de données devrait apparaître
    + vérifier que toutes les informations sont justes (notamment adresse, etc. ainsi que les dates surlignées en jaune)
    + sélectionner quelques enregistrements (avec les boutons droite / gauche de la barre d'outil `Mail Merge`) pour vérifier que toutes les données se mettent bien à jour
    + lancer la création des reçus fiscaux en les éditant de façon individuelle, en les imprimant en PDF, en les envoyant par email... selon votre mode de fonctionnement !


## Problèmes et Questions

Ces fichiers n'ont pas vocation à servir tels quels pour n'importe quelle structure. Je les distribue pour le cas où ils pourraient servir de point de départ pour définir vos propres outils répondant à vos besoins.

Si vous notez des problèmes, ou voulez soumettre des idées d'amélioration, vous pouvez les noter ici : https://github.com/sguerri/assotools/issues

Si vous avez des questions sur comment les utiliser ou les faire évoluer, vous pouvez également me contacter directement.


## L'auteur

Sébastien GUERRI - [Github](https://github.com/sguerri) - sebastien.guerri [at] assos.bmel.fr

Ancien consultant puis responsable de projets informatiques et financiers au sein de grands groupes, j'ai décidé de quitter ce milieu pour découvrir le monde autrement. Suite à un master en sciences humaines et sociales, je cherche aujourd'hui à mettre mes compétences (finance, comptabilité, gestion administrative, gestion de projets, systèmes informatiques, développement) au service de structures porteuses de sens (pour moi).

Après avoir été coordinateur d'une association, adjoint d'une cuisine centrale bio, je suis actuellement en CDD d'1 an à la direction informatique d'une université. Mon cœur navigue entre l'envie d'une situation financièrement stable et le besoin d'avoir une activité qui fait sens. Peut-être un jour serai-je directement au service des associations via un emploi partagé ou en tant que consultant à prix libre - j'y réfléchis. Je suis preneur de tout conseil !


## License

Ce projet est sous license [ISC](https://spdx.org/licenses/ISC).