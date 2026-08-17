# Notes de version

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
