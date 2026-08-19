# Notes de version

## 1.1 — 18 août 2026

**Identité de l'exécutable**

Le programme se déclarait en 0.0.0.0 et sans éditeur. Il porte désormais une
identité complète : version 1.1.0.0, produit « em7 ROM editor », éditeur
« em7max ». Windows et les antivirus le reconnaissent mieux, et une version
installée se distingue enfin d'une autre.

**Interface**

La colonne de gauche était une liste de onze sections à la file, et les trois
préréglages, posés à sa suite, se retrouvaient coupés dès que la fenêtre était
un peu courte. Les sections sont maintenant rangées en quatre groupes — ce que
vous rencontrez, les règles du jeu, vos outils — et les préréglages restent
visibles en bas, quoi qu'il arrive. Tout tient à l'écran sans défiler.

Les ascenseurs sont enfin sombres : Windows en dessinait de blancs en pleine
page. La liste des lieux de l'éditeur est redessinée aux couleurs du reste, au
lieu du bleu vif du système. Les pages sont centrées quand la fenêtre est
large, et le cadre de sélection jaune ne s'affiche plus qu'au clavier, là où il
sert.

**Fiabilité**

- le module de chromaticité relit désormais chaque repère du `.code` avant
  d'écrire quoi que ce soit, et refuse plutôt que d'écrire au hasard sur une
  ROM déjà modifiée par un autre outil ;
- documentation revue : le LisezMoi détaille les conséquences réelles de
  chaque option plutôt que ses mécanismes internes.

### Empreinte

```
em7-ROM-editor-1.1.zip
SHA-256 : E2402EC637E02B38BE965FD6A4ABC857DC55DD81592DAF9BC6243688376EB2E2
```

---

## 1.0 — 17 août 2026

Première version publique. Le support de la 3DS est complet.

**Jeux** — X, Y, Rubis Oméga, Saphir Alpha, Soleil, Lune, Ultra-Soleil,
Ultra-Lune. Reconnaissance automatique du jeu par son code produit.

**Randomizer** — Pokémon sauvages, dresseurs, starters, statiques et cadeaux,
objets et contenu des boutiques, attaques, CT/CS, types et table d'efficacité,
talents, évolutions, statistiques (permutation à total constant).

**Chromatiques** — taux réglable de 1 sur 4096 jusqu'à 100 %.

**Nuzlocke** — carnet de bord : captures par zone d'après les zones réelles du
jeu chargé, suivi des Pokémon morts, huit règles hardcore décochables.

**Confort** — six niveaux de difficulté, seed reproductible, styles de partie
enregistrables, glisser-déposer (fenêtre, icône, Ctrl+O), barre de progression,
journal détaillé, guide de démarrage et trois styles fournis.

**Sécurité du travail** — la ROM d'origine n'est jamais ouverte en écriture.
Toutes les empreintes sont recalculées : sections de l'ExeFS, superblocs, arbre
IVFC du RomFS. Contrôle de jouabilité avant écriture : starters capables
d'attaquer, CS jamais randomisées, zones jamais vidées, dresseurs pourvus. En
cas de doute, le programme s'arrête au lieu d'écrire.

**Vérifications** — les quatre ROM testées ont été passées avec toutes les
options activées d'un coup, empreintes revérifiées et contenu relu. 60 contrôles
automatisés à chaque compilation.

### Contenu de l'archive

- `em7 ROM editor.exe` — l'application
- `RomTool.exe` — l'outil en ligne de commande, facultatif
- `LisezMoi.txt` — le mode d'emploi complet

### Empreinte

```
SHA-256 : D1E1B32FFB7DB0BDB6C9F0D7096CAC387A548CA4DCDEE578FB79ECFFE315609C
```

### Connu et assumé

- Rien pour la DS ni la GBA
- Échanges internes limités à la 7e génération
- Talent Ramassage : 7e génération seulement
- Programme non signé numériquement : Windows affiche un avertissement
- Signature RSA de la partition non recalculable, comme pour tous les outils du
  genre — émulateur ou console avec patch de signature

**Aucune ROM n'est fournie.** Vous utilisez votre propre copie du jeu.
