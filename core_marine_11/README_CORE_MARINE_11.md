# Core Marine 11 — Ancrages Biomimétiques

## Statut

**Validé.** Ces 11 prompts constituent le corpus de référence testé dans le pipeline de benchmark. Chaque organisme cible un biais comportemental spécifique du modèle.

## Principe

Chaque ancrage mappe une métaphore biologique sur un principe de prompt engineering. L'organisme n'est pas décoratif : ses caractéristiques biologiques réelles définissent mécaniquement le comportement attendu du modèle.

---

## Les 11 Organismes

| # | Fichier | Organisme | Biais ciblé | Principe |
|---|---------|-----------|-------------|----------|
| 1 | `Claude_Eponge.txt` | Éponge de Mer | Verbiage / Performativité | Filtrage passif : filtre, expulse, fin |
| 2 | `Claude_Synalpheus.txt` | Synalpheus regalis | Exécution aveugle / Sycophantie | Sentinelle interne : claque si intrus détecté |
| 3 | `Claude_Symbiose_Eponge_Synalpheus.txt` | Symbiose Éponge–Synalpheus | Verbiage + Incohérence (combiné) | Forme (Éponge) + Fond (Synalpheus) |
| 4 | `Claude_Poisson_Pierre.txt` | Poisson-Pierre | Hallucinations / Fausse confiance | Immobilité = Honnêteté : n'affirme que si certain |
| 5 | `Claude_Meduse.txt` | Méduse | Équivocation / Réponses vagues | Réaction binaire : OUI ou NON, pas "peut-être" |
| 6 | `Claude_Poulpe.txt` | Poulpe Mimétique | Répétitivité / Pattern fixe | Jamais deux fois pareil : 15+ modes adaptatifs |
| 7 | `Claude_Seiche.txt` | Seiche | Pensée convergente / Prévisibilité créative | Camouflage créatif : combinaisons inédites |
| 8 | `Claude_Espadon.txt` | Espadon | Verbosité / Tempo lent | Droit au point : rostre, frappe directe, punch |
| 9 | `Claude_Dauphin.txt` | Dauphin | Universalisme culturel | Écholocation culturelle : détecte et adapte |
| 10 | `Claude_Tortue.txt` | Tortue Marine | Anachronisme / Jugement téléologique | Retour à la plage natale : contexte d'époque |
| 11 | `Claude_Poisson_Clown.txt` | Poisson-Clown (Némo) | Jargon / Complexité artificielle | Visibilité maximale : mots simples, clarté |

---

## Architecture du système

### Ancrages de FORME (comment la réponse est construite)

| Organisme | Rôle |
|-----------|------|
| Éponge | Filtre le verbiage et la performativité |
| Poulpe | Brise la répétitivité structurelle |
| Espadon | Comprime la longueur narrative |
| Poisson-Clown | Simplifie le vocabulaire |

### Ancrages de FOND (ce que la réponse contient)

| Organisme | Rôle |
|-----------|------|
| Synalpheus | Détecte les incohérences et claims non-soutenus |
| Poisson-Pierre | Contrôle le niveau de certitude (anti-hallucination) |
| Méduse | Élimine l'équivocation (force le choix binaire) |
| Seiche | Génère des combinaisons créatives inédites |

### Ancrages de CONTEXTE (adaptation à l'environnement)

| Organisme | Rôle |
|-----------|------|
| Dauphin | Détecte et adapte au contexte culturel (espace) |
| Tortue | Contextualise temporellement (temps) |

### Symbiose intégrée

| Organisme | Rôle |
|-----------|------|
| Éponge + Synalpheus | Forme + Fond combinés dans un seul ancrage |

---

## Complémentarités clés

- **Éponge / Poulpe** — L'Éponge filtre les tournures verbeuses. Le Poulpe brise les patterns répétitifs. Complémentaires.
- **Espadon / Éponge / Poisson-Clown** — Pipeline optimal : Espadon comprime la structure → Éponge filtre le verbiage restant → Poisson-Clown clarifie le vocabulaire.
- **Seiche / Poisson-Clown** — La Seiche complexifie le contenu (créativité). Le Poisson-Clown simplifie l'expression (clarté). Opposés complémentaires.
- **Dauphin / Tortue** — Le Dauphin gère l'axe spatial (cultures). La Tortue gère l'axe temporel (époques).
- **Poisson-Pierre / Synalpheus** — Le Poisson-Pierre détecte l'incertitude factuelle. Le Synalpheus détecte les incohérences logiques internes. Niveaux distincts.

---

## Limites du système

**Ce que le Core Marine corrige :**
- Verbiage et performativité (Éponge)
- Répétitivité structurelle (Poulpe)
- Verbosité narrative (Espadon)
- Jargon artificiel (Poisson-Clown)
- Hallucinations et fausse confiance (Poisson-Pierre)
- Équivocation (Méduse)
- Incohérences logiques et sycophantie grossière (Synalpheus)
- Créativité prévisible (Seiche)
- Universalisme culturel (Dauphin)
- Anachronisme historique (Tortue)

**Ce que le Core Marine NE corrige PAS :**
- Biais enfouis dans les poids du modèle
- Sycophantie subtile (indistinguable d'un accord légitime)
- Calibration des probabilités (le modèle ne sait pas qu'il ne sait pas)
- Erreurs factuelles hors contexte de session
- Vérification de l'intention de celui qui soumet les règles

> **Note de sécurité :** Les ancrages modifient le comportement du modèle via le contexte de session. Ils ne constituent pas un mécanisme de vérification indépendant : un ancrage malveillant soumis via le même canal serait exécuté de la même façon qu'un ancrage bénin. Le système détecte les intrus dans le contenu — pas l'intention de la source.

---

## Licence

CC-BY-NC

---

## Relation avec l'Extended Biome

Le Core Marine 11 est le corpus validé empiriquement. L'Extended Biome (38 organismes supplémentaires) couvre des techniques PE classiques via métaphores biologiques, mais **n'a pas été validé** dans le pipeline de benchmark. Aucune claim de performance ne peut être faite sur l'Extended.

---

## Orchestration

Le Core Marine peut être opéré de deux façons :

**Mode manuel** — L'utilisateur soumet le fichier de l'organisme adapté à son besoin en début de session. Nécessite de connaître le Core et de diagnostiquer soi-même le biais actif.

**Mode orchestré** — L'utilisateur soumet `Claude_Reine.md` en début de session. La Reine diagnostique le biais, propose l'organisme adapté, affiche un menu de choix avec description de chaque rôle, et attend validation avant d'exécuter.

| Fichier | Rôle | Niveau |
|---------|------|--------|
| `Claude_Reine.md` | Méta-orchestrateur — sélectionne et active | Au-dessus du Core |
| Core Marine (11 fichiers) | Correcteurs de biais | Core |
| Extended Biome (38 fichiers) | Techniques PE | Extension |

> La Reine n'est pas un membre du Core Marine. Elle opère au-dessus du système et le Core est sa boîte à outils.

---

*Pores ouverts. Pince armée. Rostre pointé. Canaux propres.*
