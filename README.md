# 🦊 Dictée Maligne

**Des mots, des syllabes et des phrases à réviser avec des exercices variés.**

Dictée Maligne est une application web pour s’entraîner à la lecture, à l’encodage et à l’orthographe à partir de ses propres listes. Elle propose des réglages du **CP au CM2**, une lecture audio et un suivi des résultats par élève.

Créée par **Chloé Denner-Jerez**, elle peut être utilisée en classe ou à la maison, directement dans un navigateur, sans création de compte.

👉 [Ouvrir Dictée Maligne](https://cdenner-jerez-collab.github.io/dictee-maligne/)

## Fonctionnalités

- Préparation de séances à partir de mots, de syllabes, de phrases et de familles de mots.
- Neuf types d’exercices, à sélectionner selon les besoins.
- Profils d’élèves avec historique des résultats.
- Lecture avec une voix française et une vitesse réglable.
- Révision intelligente basée sur les réponses précédentes.
- Bilan de séance, reprise des exercices ratés et fiche à imprimer.
- Export et import des données au format JSON.
- Lecture d’une liste photographiée par reconnaissance de texte.
- Génération de phrases de conjugaison à partir du CE2.

## Démarrage rapide

1. Ouvrir l’application et créer un profil avec **« Nouvel élève »**.
2. Choisir le niveau de classe et la longueur de séance.
3. Saisir la liste à travailler, avec une entrée par ligne.
4. Vérifier le découpage en syllabes proposé.
5. Choisir les exercices, la voix et la vitesse de lecture.
6. Cliquer sur **« Commencer la séance »**.
7. Consulter le bilan, rejouer les erreurs ou imprimer une fiche à réviser.

Les formats **courte** et **normale** correspondent à une base de 15 ou 30 exercices. Le nombre peut être supérieur lorsque la liste contient beaucoup de mots ou lorsque la révision intelligente ajoute des répétitions. Le format **complète** utilise tous les exercices générés, avant l’adaptation liée à l’historique.

## Préparer une liste

### Mots et syllabes

Saisir un mot ou une syllabe par ligne :

```text
chapeau
tortue
ba
bi
so
os
```

Pour imposer le découpage d’un mot, séparer ses syllabes avec des tirets :

```text
cha-peau
tor-tue
```

Sans tirets, le découpage est automatique et doit être vérifié. Les tirets servent de séparateurs et sont retirés du mot utilisé dans les exercices.

Pour saisir plusieurs syllabes sur une même ligne, cocher **« Découper chaque ligne en mots/syllabes séparés »** :

```text
so sa si os
```

Cette option produit quatre entrées distinctes. Sans elle, une ligne contenant plusieurs mots est traitée comme une phrase.

### Phrases

Saisir une phrase par ligne. Pour choisir le mot ciblé dans les exercices, l’entourer d’astérisques :

```text
Le *chat* dort sur le tapis.
La *tortue* avance doucement.
```

Sans astérisques, l’application choisit automatiquement une cible. Une phrase avec un mot entre astérisques reste une phrase, même si l’option de découpage des lignes est cochée.

### Familles de mots

Utiliser le format `mot > dérivé1, dérivé2` :

```text
dent > dentiste, dentifrice
jardin > jardinier, jardinage
```

Cocher **« Mots de la même famille »** pour générer les exercices correspondants.

### Liste photographiée

Cliquer sur **« Lire une photo de la liste »**, puis sélectionner une image. Le texte reconnu est ajouté à la liste existante.

Relire et corriger le résultat avant de commencer : la reconnaissance peut comporter des erreurs et nécessite une connexion Internet.

## Les exercices

| Exercice | Ce que fait l’élève |
| --- | --- |
| Écoute et clique sur la bonne syllabe | Écouter puis choisir la syllabe parmi plusieurs propositions. |
| Remets les lettres de la syllabe dans l’ordre | Reconstituer une syllabe avec des lettres mélangées. |
| Autres façons d’écrire ce son | Identifier une autre graphie d’un même son. |
| Remets les lettres dans l’ordre | Reconstituer un mot ; certains mots longs sont proposés en tuiles de syllabes à partir du CE2. |
| Dictée flash | Observer un mot ou une phrase, puis le saisir de mémoire après sa disparition. |
| Phrase à trous | Choisir la bonne forme pour compléter une phrase. |
| Chasse à l’erreur | Écouter et reconnaître l’orthographe attendue parmi plusieurs propositions. |
| Mot mystère | Retrouver un mot à l’aide d’indices progressifs. |
| Mots de la même famille | Choisir un dérivé du mot proposé. |

Le changement de niveau applique une sélection d’exercices par défaut.

Le module des graphies est proposé en CP et désactivé par défaut ; les phrases à trous sont proposées à partir du CE2. Les familles de mots nécessitent leur format de saisie spécifique.

## Conjugaison

À partir du CE2, un champ permet de saisir des verbes à l’infinitif, un par ligne :

```text
chanter
finir
être
aller
```

Les temps disponibles sont :

- le **présent** ;
- le **futur** ;
- l’**imparfait** ;
- le **passé composé**.

L’application génère des phrases qui alimentent les exercices activés.

Le moteur utilise des règles simplifiées et une liste de verbes irréguliers : il ne couvre pas tous les verbes ni tous les accords. Vérifier l’aperçu et les formes proposées ; pour maîtriser précisément le contenu, saisir ses propres phrases dans la liste.

## Audio et correction

Choisir une voix française parmi celles disponibles dans le navigateur. La vitesse est réglable ; le bouton **🐢** permet une écoute ralentie dans les exercices qui le proposent.

Pour les réponses saisies, l’option **« Tolérance accents et ponctuation »**, activée par défaut, accepte l’absence d’accents et ignore certains signes de ponctuation. La désactiver pour exiger ces éléments.

La casse reste ignorée et les espaces entre les mots restent significatifs.

La disponibilité des voix et leur fonctionnement hors connexion dépendent du navigateur et du système : une voix peut utiliser un service local ou distant.[^voix]

## Suivi et révision intelligente

Le bouton **« Suivi »** affiche une vue des profils et le détail de l’élève sélectionné : résultats, mots à revoir et cibles classées par l’algorithme comme maîtrisées ou en difficulté.

Jusqu’à **50 séances terminées** sont conservées par élève ; le détail affiche les dix dernières. Une séance interrompue n’apparaît pas comme une séance terminée dans l’historique.

Lorsque **« Révision intelligente »** est cochée :

- Une cible est écartée lorsque son nombre de réussites dépasse son nombre d’erreurs d’au moins trois.
- Une cible ayant davantage d’erreurs que de réussites peut être proposée plus souvent.
- Si toutes les cibles sont écartées, changer la liste ou décocher cette option pour les retravailler.

Ces catégories correspondent aux règles internes de l’application.

## Sauvegardes et données

Les profils, les résultats, la liste et les réglages sont enregistrés dans le **stockage local du navigateur** (`localStorage`).

La liste et les réglages sont communs aux profils ; l’historique et les compteurs de réussite sont propres à chaque élève.

Il n’y a pas de synchronisation automatique entre appareils ou navigateurs.

- **Exporter** télécharge le fichier `dictee-maligne-sauvegarde.json` avec l’ensemble des données enregistrées.
- **Importer** restaure une sauvegarde produite par l’application. **L’import remplace les données courantes ; il ne fusionne pas les profils.**

Exporter régulièrement pour conserver une copie et transférer les données.

L’effacement des données du navigateur supprime la sauvegarde locale. En navigation privée, les données sont effacées à la fermeture de la session privée ; pour un fichier ouvert directement depuis l’ordinateur, le comportement du stockage peut varier selon le navigateur.[^stockage]

## Utilisation locale et connexion Internet

Le fichier HTML peut être téléchargé et ouvert directement dans un navigateur avec JavaScript activé. Les exercices sont générés dans la page, sans serveur applicatif.

Certaines fonctions ou ressources dépendent toutefois d’Internet :

- **Reconnaissance de texte** : chargement de Tesseract.js et de ses ressources.
- **Polices** : chargement de Baloo 2 et Atkinson Hyperlegible depuis Google Fonts.
- **Lecture audio** : connexion éventuelle selon la voix utilisée.

L’application ne contient pas de mécanisme dédié de mise en cache hors connexion du site publié.

## Publication sur GitHub Pages

Pour publier l’application depuis la racine d’une branche du dépôt :

1. Ajouter le fichier de l’application sous le nom **`index.html`**, en minuscules, à la racine du dépôt.
2. Ajouter ce fichier **`README.md`** au même emplacement.
3. Ouvrir **Settings → Pages**.
4. Choisir **Deploy from a branch** comme source.
5. Sélectionner la branche contenant les fichiers, par exemple `main`, puis le dossier **`/ (root)`**, et enregistrer.
6. Consulter l’adresse publiée dans les réglages de GitHub Pages.

Le fichier d’entrée doit se trouver au niveau supérieur du dossier choisi comme source de publication.[^pages]

| Fichier | Rôle |
| --- | --- |
| `index.html` | Application : structure HTML, styles CSS et logique JavaScript. |
| `README.md` | Présentation du projet et mode d’emploi. |

## Technologies

- **HTML, CSS et JavaScript**, réunis dans un fichier.
- **Web Speech API** pour la synthèse vocale.
- **localStorage** pour les données enregistrées dans le navigateur.
- **Tesseract.js 5.0.4**, chargé à la demande pour la reconnaissance de texte.
- **Google Fonts** pour les polices de l’interface.

Aucune installation de dépendances ni compilation n’est nécessaire pour ouvrir le fichier HTML.

## Références

Les fonctionnalités décrites correspondent au code du fichier `dictée-maligne.html` fourni pour rédiger cette documentation.

[^pages]: GitHub Docs, [Configuration d’une source de publication](https://docs.github.com/fr/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) et [Création d’un site GitHub Pages](https://docs.github.com/fr/pages/getting-started-with-github-pages/creating-a-github-pages-site), consultées le 30 septembre 2026.

[^stockage]: Contributeurs de MDN, [Window : propriété localStorage](https://developer.mozilla.org/fr/docs/Web/API/Window/localStorage), page mise à jour le 1er août 2026, consultée le 30 septembre 2026.

[^voix]: Contributeurs de MDN, [SpeechSynthesisVoice: localService property](https://developer.mozilla.org/en-US/docs/Web/API/SpeechSynthesisVoice/localService), consultée le 30 septembre 2026.
