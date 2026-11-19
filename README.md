# Creative Sound pour Mac — bêta

Panneau pour parcourir, écouter et poser ta sonothèque dans **DaVinci Resolve Studio**, ici en **version Mac**.
Projet jumeau de [Creative Look pour Mac](https://github.com/procreativenadir-png/creative-look-mac-beta).

> **Première bêta Mac.** Le panneau tourne sur Windows, mais cette version Mac est toute neuve : tu fais partie des
> premiers à l'essayer. Dis-nous ce qui marche et ce qui coince (onglet Issues).

## En bref

- **Il te faut** : un Mac (Apple Silicon ou Intel) avec DaVinci Resolve **Studio**. La version gratuite n'a pas les
  Workflow Integrations.
- **À télécharger** : uniquement `CreativeSound-…-beta-mac.zip`, dans **Releases** (colonne de droite).
- **À ignorer** : « Source code (zip) » et « Source code (tar.gz) ». GitHub les ajoute tout seul sous chaque
  version ; ils ne contiennent que cette page, pas le plugin.
- **À fournir toi-même** : tes sons. Aucun n'est livré : le panneau range ta sonothèque (WAV, MP3, AIFF, FLAC, OGG,
  M4A) sans rien copier ni déplacer.
- **Sur Windows ?** Ce n'est pas la bonne page : la bêta Windows est sur
  [creative-sound-beta](https://github.com/procreativenadir-png/creative-sound-beta).

### Dans l'archive

| Fichier | À faire |
|---|---|
| `Installer Creative Sound.command` | **le seul à double-cliquer**, pour installer comme pour mettre à jour |
| dossier `Creative Sound` | n'y touche pas : l'installeur le copie au bon endroit |
| `LISEZ-MOI.txt` | le mode d'emploi en version courte |
| `Désinstaller Creative Sound.command` | seulement pour retirer le panneau |

## Installer ou mettre à jour

1. Télécharge l'archive de la dernière version dans **Releases** (à droite de cette page).
2. Ferme DaVinci Resolve.
3. Double-clique sur l'archive pour la décompresser, puis double-clique sur **Installer Creative Sound.command**.
   Le Terminal s'ouvre et demande le mot de passe de ta session Mac : rien ne s'affiche pendant que tu le tapes,
   c'est normal. Valide avec Entrée.
4. Ouvre Resolve Studio : Workspace > Workflow Integrations > **Creative Sound**.

L'installeur copie le panneau dans le dossier des plugins de Resolve et y ajoute le module qui le relie à Resolve,
pris dans ton installation de Resolve. Ta bibliothèque et tes favoris restent dans
`~/Library/Application Support/Creative Sound`.

### Si le Mac refuse d'ouvrir l'installeur

Le panneau n'est pas encore signé par Apple, donc le Mac bloque l'installeur au premier double-clic
(« Apple n'a pas pu vérifier… » ou « développeur non identifié »).

- Ouvre **Réglages Système > Confidentialité et sécurité**. Tout en bas, clique sur **Ouvrir quand même**, puis
  relance l'installeur.
- Ou bien ouvre le **Terminal**, tape `bash` suivi d'un espace, glisse l'installeur dans la fenêtre, puis Entrée.

S'il dit « WorkflowIntegration.node introuvable », écris-nous dans Issues. En attendant, tu peux poser un fichier
`WorkflowIntegration.node` à côté de l'installeur : il le prendra en priorité.

## Premier lancement

Bouton **Dossiers** (en bas) > **Ajouter un dossier…** : choisis le ou les dossiers où sont tes sons. Rien n'est
copié ni déplacé. Le panneau lit les noms et les durées, puis range les sons par familles (whooshs, impacts,
risers, ambiances, bruitages, musique…). Sur une grosse sonothèque, la première lecture prend quelques minutes.
Si le Mac demande si Resolve peut accéder à un dossier ou à un disque externe, accepte : sinon le panneau ne voit
pas tes sons.

## L'essentiel

- **Survol** d'un son : écoute. **Clic** : lecteur avec forme d'onde. **Double-clic** : posé à la tête de lecture.
- **Lecteur** : clic = aller à un endroit, glisser = choisir un passage (« Poser le passage »), L = boucle.
- **Piste** : « Auto » pose sur la première piste audio libre ; A1 à A6 forcent une piste.
- **Temps fort** : un riser, un impact ou un whoosh est calé pour que son moment fort tombe sur la tête de lecture.
- **Recherche** en français ou en anglais (pluie = rain), fautes de frappe pardonnées, et tes propres synonymes.
- **Court / Moyen / Long**, tri par durée, et le dé **Surprends-moi**.
- **Poignée ⠿** du lecteur : glisse le son, ou seulement le passage choisi, où tu veux dans la timeline.
- **Effets** (bouton curseurs du lecteur) : hauteur, grave, aigu, étouffé, écho, espace, inverser, normaliser, et des
  préréglages (les tiens aussi). Poser utilise le son retouché, enregistré dans le dossier Sons modifiés ;
  l'original ne change pas.
- **Tempo des musiques** : estimé à la première écoute, affiché en BPM ; recherche « 120 bpm ».
- **≈ Sons proches** (dans le lecteur) : les sons qui ressemblent le plus à celui-ci.
- **Kits** : les sons d'un projet ou d'un client, à copier dans le dossier du projet avec leurs crédits.
- **Clic sur le nom** dans le lecteur : renommer un son ou le changer de famille.
- **Licence** : la capsule du pack, dans le lecteur, passe par Client OK, Perso, À vérifier. Le filtre « Client OK »
  ne montre que les sons utilisables pour un client.
- **Sur Mac, le panneau est une fenêtre libre** : place-la où tu veux à côté de Resolve, elle garde sa place.

### Raccourcis

Dans le panneau : **Espace** écouter, **Entrée** poser, **↑ ↓** son précédent ou suivant, **L** boucle, **D** au
hasard, **T** temps fort, **E** effets, **F** favori, **0 à 6** piste (0 = Auto), **+ et −** volume.

Dans Resolve, même quand le panneau n'a pas la main, avec **Cmd+Option+Maj** :

| Touche | Action |
|---|---|
| J / L | son précédent / suivant (et écoute) |
| K | écouter ou arrêter |
| P | poser à la tête de lecture |
| D | un son au hasard |

Ils ne prennent aucune touche de Creative Look : les deux panneaux peuvent tourner ensemble.

## Un problème, une idée ?

Ouvre une **Issue** sur ce dépôt (modèles « Problème » et « Idée »). Pour un problème, joins le rapport : bouton
**Dossiers** (en bas) > **Rapport pour le support** : le Finder s'ouvre sur un fichier texte. Il contient les
versions, les réglages du panneau et la fin du journal, aucun son ni aucune image ; les chemins des dossiers peuvent
contenir ton nom d'utilisateur.

Ce qui nous aide le plus pour cette première bêta Mac : l'installation s'est-elle bien passée, le panneau
s'ouvre-t-il, tes dossiers de sons sont-ils lus, un son se pose-t-il bien dans la timeline.

## Limites connues

- Pas encore d'aimantation : sur Windows, le panneau se colle au bord de Resolve ; sur Mac, c'est une fenêtre libre.
- Pas encore signé par Apple : d'où le blocage au premier double-clic (voir plus haut).
- Le détail des versions est dans [CHANGELOG.md](CHANGELOG.md).
