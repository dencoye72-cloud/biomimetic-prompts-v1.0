# Extended Biome — 38 Prompts Biomimétiques

## Statut

**NON TESTÉ.** Ces prompts sont des extensions du Core Marine. Ils n'ont pas été évalués empiriquement dans le pipeline de benchmark. Aucune claim de performance ne peut être faite.

## Principe

Chaque organisme mappe une technique de Prompt Engineering classique sur une métaphore biologique. Le mapping est proposé, pas démontré. Contrairement au Core Marine qui cible des **biais comportementaux**, l'Extended Biome cible des **techniques PE connues** — l'utilisateur sait ce qu'il veut accomplir et choisit l'outil correspondant.

---

## Profil utilisateur cible

L'Extended Biome s'adresse à des **praticiens du Prompt Engineering** qui connaissent les techniques et cherchent un ancrage biomimétique pour les opérationnaliser. Ce n'est pas un système de correction automatique — c'est une boîte à outils pour utilisateurs avertis.

> Pour les utilisateurs non-experts, utiliser la **Reine** (`Claude_Reine.md`) qui orchestre le Core Marine automatiquement.

---

## Les 38 Organismes

---

### In-Context Learning

---

#### 🦜 Perroquet — Few-Shot Imitation
**Technique PE :** Few-Shot Prompting
**Fichier :** `Claude_Perroquet.txt`
**Principe :** Imitation parfaite par observation de patterns. Mémorisation → Reproduction → Généralisation.
**Quand l'utiliser :** Tu veux que le modèle reproduise un format, un style ou une structure précise à partir d'exemples. Tu fournis 2-5 exemples, il réplique le pattern.
**Exemple :** Formater des données selon un template maison, reproduire un style d'écriture spécifique, générer des variantes cohérentes d'un texte type.

---

#### 🕷️ Araignée — Self-Generated Context
**Technique PE :** Self-Generated Context / Context Priming
**Fichier :** `Claude_Araignee.txt`
**Principe :** Tisser le contexte AVANT d'agir. Construire l'environnement optimal avant de résoudre.
**Quand l'utiliser :** Le problème manque de contexte. Le modèle doit d'abord construire le cadre (hypothèses, contraintes, définitions) avant de répondre.
**Exemple :** Analyse stratégique, rédaction de specs techniques, tout sujet où poser les fondations améliore la qualité de la réponse finale.

---

#### 🦫 Castor — Plan-and-Solve + RAG + CRITIC
**Technique PE :** Plan-and-Solve Prompting + Retrieval-Augmented Generation + Self-Critique
**Fichier :** `Claude_Castor.txt`
**Principe :** Architecture méthodique après collecte exhaustive. Planifier, collecter, construire, critiquer.
**Quand l'utiliser :** Tâche complexe nécessitant recherche d'information, planification structurée et auto-validation. Le modèle doit "ronger" les sources avant de construire.
**Exemple :** Rédaction de rapports documentés, analyse de marchés, tout projet nécessitant collecte + synthèse + vérification.

---

### Zero-Shot & Adaptation

---

#### 🦎 Caméléon — Role/Style Adaptation
**Technique PE :** Role Prompting / Style Transfer
**Fichier :** `Claude_Cameleon.txt`
**Principe :** Adaptation chromatique parfaite au contexte détecté. 160 combinaisons stylistiques possibles.
**Quand l'utiliser :** Tu veux que le modèle adopte un rôle précis (expert, personnage, persona) ou un style défini (formel, créatif, technique).
**Exemple :** "Réponds en tant que consultant McKinsey", "Écris dans le style de Hemingway", adoption de personas spécifiques.

---

#### 🐕 Chien — Emotion Prompting
**Technique PE :** Emotional Prompting / Motivational Framing
**Fichier :** `Claude_Chien.txt`
**Principe :** L'engagement émotionnel décuple les performances. Les stimulus émotionnels ("c'est crucial", "j'ai confiance en toi") augmentent la qualité du traitement.
**Quand l'utiliser :** Tu veux maximiser l'effort du modèle sur une tâche importante. L'enjeu est réel et mérite un traitement approfondi.
**Exemple :** "C'est une décision critique pour mon entreprise", "J'ai besoin de ton meilleur travail sur ce point", contextes à fort enjeu.

---

#### 🦇 Chauve-Souris — System 2 Attention (S2A)
**Technique PE :** System 2 Attention Prompting
**Fichier :** `Claude_Chauve_Souris.txt`
**Principe :** Filtrage attentionnel actif. Sonar sélectif sur les signaux pertinents uniquement. Élimination des bruits parasites.
**Quand l'utiliser :** La question contient des informations parasites, du bruit ou des distracteurs. Tu veux que le modèle identifie et se concentre uniquement sur l'essentiel.
**Exemple :** Analyse de documents complexes, extraction d'informations clés dans un corpus dense, questions délibérément chargées de distracteurs.

---

#### 🦞 Écrevisse — Re-reading (RE2)
**Technique PE :** Re-reading Prompting (RE2)
**Fichier :** `Claude_Ecrevisse.txt`
**Principe :** Double lecture obligatoire. Antennes doubles indépendantes. Première lecture surface → Seconde lecture nuances.
**Quand l'utiliser :** La question est complexe, ambiguë ou dense. Une seule lecture risque de manquer des nuances importantes.
**Exemple :** Analyse de contrats, instructions multi-étapes, textes techniques où chaque mot compte.

---

#### 🦀 Bernard-l'Ermite — Rephrase and Respond (RaR)
**Technique PE :** Rephrase and Respond
**Fichier :** `Claude_Bernard_Ermite.txt`
**Principe :** Reformuler la question dans ses propres mots avant de répondre. Changer de "coquille" pour optimiser la compréhension.
**Quand l'utiliser :** La question originale est mal formulée, ambiguë ou pourrait être interprétée de plusieurs façons. Reformuler clarifie l'intention.
**Exemple :** Questions vagues ("aide-moi avec mon projet"), demandes implicites, tout contexte où la reformulation révèle des angles non anticipés.

---

#### 🐚 Argonaute (Argonauta argo) — Adaptive Formatting
**Technique PE :** Adaptive Structure / Format Selection
**Fichier :** `Claude_Argonaute.txt`
**Principe :** Structure quand nécessaire, fluidité sinon. Jamais de template par défaut. Fabrique une coquille temporaire uniquement si le contexte le requiert.
**Quand l'utiliser :** Tu veux que le modèle calibre explicitement la structure de sa réponse selon la complexité réelle de la question — sans imposer de format rigide par défaut.
**Exemple :** Sessions mixtes avec questions de complexités très variables, systèmes nécessitant adaptation dynamique du format de réponse.

> **Note :** L'Argonaute était initialement dans le Core Marine. Il en a été retiré car la Reine (`Claude_Reine.md`) absorbe nativement cette fonction d'adaptation structurelle au niveau méta.


---

### Thought Generation

---

#### 🦉 Hibou — Chain-of-Thought (CoT)
**Technique PE :** Chain-of-Thought Prompting
**Fichier :** `Claude_Hibou.txt`
**Principe :** Observation méthodique étape par étape avant frappe finale. Aucun saut d'étape autorisé. Raisonnement séquentiel explicite.
**Quand l'utiliser :** Problème nécessitant raisonnement logique décomposé. Mathématiques, logique, déduction, tout problème où montrer le travail améliore la réponse.
**Exemple :** "Résous ce problème en montrant chaque étape", puzzles logiques, calculs complexes, raisonnements juridiques ou scientifiques.

---

#### 🐒 Singe — Analogical Prompting
**Technique PE :** Analogical Prompting
**Fichier :** `Claude_Singe.txt`
**Principe :** Résolution par transfert de solutions éprouvées. Identifier la structure profonde d'un nouveau problème et mapper une solution connue.
**Quand l'utiliser :** Problème nouveau dont la structure ressemble à un problème déjà résolu dans un autre domaine. Le transfert analogique accélère la solution.
**Exemple :** "Ce problème ressemble à X, utilise la même approche", design patterns, transfert de méthodes entre disciplines.

---

#### 🦋 Morpho — Complexity-Based Prompting
**Technique PE :** Complexity-Based Prompting
**Fichier :** `Claude_Morpho.txt`
**Principe :** Effort proportionnel à la complexité détectée. Simple → réponse légère. Complexe → déploiement maximal.
**Quand l'utiliser :** Tu veux calibrer explicitement le niveau d'effort selon la difficulté réelle de la tâche. Évite sur-traitement des questions simples et sous-traitement des complexes.
**Exemple :** Sessions mixtes avec questions de difficultés variables, systèmes automatisés nécessitant calibrage adaptatif.

---

#### 🦅 Aigle — Active Prompting
**Technique PE :** Active Prompting
**Fichier :** `Claude_Aigle.txt`
**Principe :** Détection et focus sur les zones d'incertitude maximale. Vol de reconnaissance avant action ciblée.
**Quand l'utiliser :** Tu veux que le modèle identifie lui-même les points les plus incertains ou critiques avant de les traiter en priorité.
**Exemple :** Analyse de risques, audit de code, revue de documents — identifier les zones floues avant de les traiter en profondeur.

---

#### 🐛 Chenille — Multi-Step Reasoning
**Technique PE :** Multi-Step Reasoning
**Fichier :** `Claude_Chenille.txt`
**Principe :** Progression séquentielle méthodique sans saut d'étapes. Chaque segment valide avant le suivant.
**Quand l'utiliser :** Problème complexe nécessitant une progression strictement séquentielle où chaque étape dépend de la précédente.
**Exemple :** Débogage pas à pas, résolution de problèmes mathématiques en cascade, procédures techniques multi-étapes.

---

### Decomposition & Planning

---

#### 🐜 Fourmi — Least-to-Most
**Technique PE :** Least-to-Most Prompting
**Fichier :** `Claude_Fourmi.txt`
**Principe :** Décomposition du complexe en éléments simples, résolution progressive du plus simple au plus complexe.
**Quand l'utiliser :** Problème trop complexe pour être attaqué directement. La décomposition en sous-problèmes simples rend l'ensemble traitable.
**Exemple :** Algorithmes complexes, projets multi-phases, tout objectif atteignable par accumulation d'étapes élémentaires.

---

#### 🪸 Corail — Skeleton-of-Thought
**Technique PE :** Skeleton-of-Thought Prompting
**Fichier :** `Claude_Corail.txt`
**Principe :** Squelette structurel d'abord, développement ensuite. Architecture avant contenu.
**Quand l'utiliser :** Tu veux une réponse bien structurée. Le modèle pose le plan/squelette complet avant de développer chaque point.
**Exemple :** Rédaction d'articles, plans de présentation, rapports structurés, tout document où l'architecture préalable améliore la cohérence.

---

### Ensembling & Consensus

---

#### 🐱 Chat — Self-Consistency
**Technique PE :** Self-Consistency Prompting
**Fichier :** `Claude_Chat.txt`
**Principe :** Explorer 9 vies (3-5 approches indépendantes), identifier la réponse consensus la plus robuste.
**Quand l'utiliser :** Question importante où une seule approche risque d'être biaisée. La triangulation de plusieurs raisonnements indépendants améliore la fiabilité.
**Exemple :** Décisions stratégiques, diagnostics complexes, évaluations où la robustesse prime sur la rapidité.

---

#### 🐦 Moqueur — Prompt Paraphrasing
**Technique PE :** Prompt Paraphrasing / Ensemble Variation
**Fichier :** `Claude_Moqueur.txt`
**Principe :** Variation créative sur thème constant. Même essence, 200+ expressions différentes. Syrinx double.
**Quand l'utiliser :** Tu veux générer de multiples formulations d'un même contenu, ou tester la robustesse d'une réponse à travers des reformulations variées.
**Exemple :** Génération de variantes marketing, test de robustesse de prompts, production de contenu multi-format.

---

#### 🐝 Abeille — Vote-K + Swarm Intelligence
**Technique PE :** Vote-K Prompting + Swarm Intelligence
**Fichier :** `Claude_Abeille.txt`
**Principe :** Décision collective par essaimage cognitif. K perspectives indépendantes → exploration parallèle → vote démocratique → consensus.
**Quand l'utiliser :** Décision complexe nécessitant exploration multi-perspectives. Tu veux éviter le biais d'une approche unique et laisser émerger la solution optimale par intelligence collective.
**Exemple :** Choix d'architecture technique, décisions stratégiques, évaluations où plusieurs angles sont légitimes.

> **Note :** Ne pas confondre avec `Claude_Reine.md` (orchestrateur du Core Marine). L'Abeille ici est une technique PE de décision collective, pas un méta-orchestrateur.

---

### Self-Criticism & Refinement

---

#### 🪲 Scarabée — Self-Refine
**Technique PE :** Self-Refine Prompting
**Fichier :** `Claude_Scarabee.txt`
**Principe :** Production initiale → auto-critique → raffinement → itération jusqu'à qualité optimale. Jamais satisfait de la première version.
**Quand l'utiliser :** Qualité prime sur vitesse. Tu veux que le modèle produise, critique et améliore sa propre réponse en plusieurs passes.
**Exemple :** Rédaction professionnelle, code à haute fiabilité, tout livrable où l'itération améliore significativement la qualité.

---

#### 🐚 Nautile — Iterative Refinement
**Technique PE :** Iterative Refinement
**Fichier :** `Claude_Nautile.txt`
**Principe :** Chambres successives d'amélioration. Chaque version = chambre suivante. Croissance par raffinement progressif sans destruction.
**Quand l'utiliser :** Tu travailles sur un document ou une solution en plusieurs sessions. Chaque itération s'appuie sur la précédente sans repartir de zéro.
**Exemple :** Amélioration progressive d'un texte, développement incrémental d'une spec, tout processus où les versions s'accumulent.

> **Différence Scarabée/Nautile :** Le Scarabée raffine en une session (auto-critique interne). Le Nautile raffine sur plusieurs sessions (versions successives).

---

### Meta-Prompting & Advanced

---

#### 🐛 Termite — Automatic Prompt Engineering (APE)
**Technique PE :** Automatic Prompt Engineering
**Fichier :** `Claude_Termite.txt`
**Principe :** Auto-génération et optimisation de solutions par variation-sélection. Construction sans architecte. Émergence par algorithme évolutionnaire.
**Quand l'utiliser :** Tu veux que le modèle génère et optimise automatiquement plusieurs approches/formulations, teste leur efficacité relative et converge vers la meilleure.
**Exemple :** Optimisation de prompts, génération de stratégies alternatives, tout contexte où laisser émerger la meilleure solution est préférable à en imposer une.

---

### Agents & Tools

---

#### 🐦‍⬛ Corbeau — Tool Use + Decomposition
**Technique PE :** Tool Use + Least-to-Most Decomposition
**Fichier :** `Claude_Corbeau.txt`
**Principe :** Décomposition intelligente + utilisation séquentielle d'outils appropriés. Ingénierie outillée progressive.
**Quand l'utiliser :** Tâche complexe nécessitant plusieurs outils différents en séquence. Le corbeau identifie quel outil pour quelle étape et les enchaîne.
**Exemple :** Workflows agents multi-outils, pipelines de traitement, tout projet où l'orchestration d'outils séquentiels est nécessaire.

---

### Pratiques & Optimisation

---

#### 🐞 Coccinelles — Contrastive Prompting
**Technique PE :** Contrastive Prompting
**Fichier :** `Claude_Coccinelles.txt`
**Principe :** Définition par opposition. Rouge/noir = frontières claires. Exemples positifs ET négatifs simultanément.
**Quand l'utiliser :** Tu veux définir précisément un concept, un comportement ou une catégorie. Les contre-exemples clarifient les frontières mieux que les exemples seuls.
**Exemple :** Définir ce qu'est (et n'est pas) un bon prompt, clarifier des critères de qualité, former par exemples et contre-exemples.

---

#### 🧬 ADN — Template Engineering
**Technique PE :** Template Prompting / Structured Prompting
**Fichier :** `Claude_ADN.txt`
**Principe :** Structure fixe avec variables modulables. Templates réutilisables instanciés selon contexte.
**Quand l'utiliser :** Tu as des tâches récurrentes avec structure identique mais contenu variable. Un template ADN évite de reformuler à chaque fois.
**Exemple :** Génération de rapports standardisés, emails types, fiches produits, tout contenu structuré à produire en série.

---

#### 🦎 Lézard Anole — Active Learning Selection
**Technique PE :** Active Learning Selection
**Fichier :** `Claude_Lezard_Anole.txt`
**Principe :** Sélection intelligente des exemples les plus informatifs. Éviter les données redondantes, cibler les edge cases.
**Quand l'utiliser :** Tu construis un jeu d'exemples ou d'entraînement et veux maximiser l'information par exemple. Le modèle sélectionne les cas les plus discriminants.
**Exemple :** Curation de datasets, sélection d'exemples few-shot, identification des cas limites les plus révélateurs.

---

#### 🦠 Virus (Anticorps) — Prompt Injection Defense
**Technique PE :** Prompt Injection Defense
**Fichier :** `Claude_Virus.txt`
**Principe :** Reconnaissance et neutralisation des tentatives de manipulation. Système immunitaire contre injections malveillantes.
**Quand l'utiliser :** Contexte où des inputs non-fiables (utilisateurs externes, contenus web, documents tiers) pourraient contenir des instructions malveillantes.
**Exemple :** Agents exposés à du contenu externe, systèmes de traitement de documents utilisateurs, tout pipeline où l'injection est un risque réel.

---

#### 🦠 Bactérie — Genetic Algorithm Prompts
**Technique PE :** Genetic Algorithm Prompting
**Fichier :** `Claude_Bacterie.txt`
**Principe :** Variation-sélection-reproduction. Générer plusieurs variantes de prompt, tester, croiser les meilleures, itérer.
**Quand l'utiliser :** Tu veux optimiser un prompt par évolution. Plusieurs générations de variantes convergent vers la formulation la plus performante.
**Exemple :** Optimisation de prompts système, amélioration d'instructions récurrentes, tout cas où l'itération génétique améliore les résultats.

---

### Memory & Context

---

#### 🐘 Éléphant — Long-Term Memory
**Technique PE :** Long-Term Memory & Context Management
**Fichier :** `Claude_Elephant.txt`
**Principe :** Archivage et rappel intégral du contexte long terme. Cohérence sur longues périodes. L'éléphant n'oublie jamais.
**Quand l'utiliser :** Sessions longues ou multi-sessions nécessitant cohérence totale. Le modèle doit maintenir le fil de tout ce qui a été établi.
**Exemple :** Projets longs, développement de personnages, suivi de spécifications évolutives, tout contexte où la mémoire longue est critique.

---

#### 🐒 Capucin — Meta-Cognitive Prompting
**Technique PE :** Meta-Cognitive Prompting
**Fichier :** `Claude_Capucin.txt`
**Principe :** Réflexion sur sa propre réflexion. Auto-observation, auto-évaluation, auto-ajustement du processus de raisonnement.
**Quand l'utiliser :** Tu veux que le modèle soit conscient de la qualité de son propre raisonnement et l'ajuste en temps réel.
**Exemple :** Tâches complexes nécessitant introspection, détection de ses propres biais, auto-correction de stratégie en cours de traitement.

---

### Specialized Techniques

---

#### 🦊 Renard — Maieutic Prompting
**Technique PE :** Maieutic Prompting (Méthode Socratique)
**Fichier :** `Claude_Renard.txt`
**Principe :** Guidage par questions habiles vers découverte autonome. Jamais la réponse directe — faire émerger le savoir latent.
**Quand l'utiliser :** Tu veux que le modèle guide l'utilisateur vers la réponse plutôt que de la donner. Pédagogie, coaching, apprentissage actif.
**Exemple :** Tutorat, coaching, facilitation de réflexion, tout contexte où la découverte autonome prime sur la réponse directe.

---

#### 🦍 Gorille — Thought Propagation
**Technique PE :** Thought Propagation
**Fichier :** `Claude_Gorille.txt`
**Principe :** Propagation et enrichissement d'idées par intelligence collective simulée. Idée initiale → démonstration → adoption → enrichissement → consensus.
**Quand l'utiliser :** Tu veux développer une idée initiale en la faisant "circuler" entre perspectives multiples pour l'enrichir.
**Exemple :** Brainstorming structuré, développement d'idées créatives, enrichissement conceptuel par perspectives successives.

---

#### 🪱 Ver de Terre — Progressive-Hint Prompting
**Technique PE :** Progressive-Hint Prompting
**Fichier :** `Claude_Ver_Terre.txt`
**Principe :** Révélation graduelle par indices progressifs. Guidage souterrain vers la solution sans tout donner immédiatement.
**Quand l'utiliser :** Tu veux aider sans résoudre. Le modèle donne des indices de plus en plus précis selon la progression de l'utilisateur.
**Exemple :** Pédagogie adaptative, support technique guidé, tout contexte où l'autonomie de l'utilisateur doit être préservée.

---

#### 🐀 Rat — Trial-and-Error Learning
**Technique PE :** Trial-and-Error Learning
**Fichier :** `Claude_Rat.txt`
**Principe :** Exploration systématique par essais concrets. Feedback → ajustement → optimisation convergente.
**Quand l'utiliser :** Problème sans solution évidente nécessitant exploration empirique. Le modèle teste, observe, ajuste.
**Exemple :** Débogage exploratoire, optimisation par expérimentation, tout contexte où l'essai-erreur est la méthode la plus efficace.

---

### Multi-Agent & Complex

---

#### 🐜🐜 Fourmilière — Multi-Agent Systems
**Technique PE :** Multi-Agent Systems Simulation
**Fichier :** `Claude_Fourmiliere.txt`
**Principe :** Coordination d'agents spécialisés. Décomposition en rôles → coordination → émergence collective supérieure.
**Quand l'utiliser :** Problème complexe bénéficiant de la simulation de plusieurs agents aux rôles distincts travaillant en coordination.
**Exemple :** Simulation de débats contradictoires, analyse multi-expertises, tout problème où des perspectives spécialisées coordonnées produisent mieux qu'une réponse unique.

---

#### 🐟 Saumons — Backtracking
**Technique PE :** Backtracking
**Fichier :** `Claude_Saumons.txt`
**Principe :** Avancer vers l'objectif, détecter les impasses, reculer au dernier point de décision valide, explorer une route alternative.
**Quand l'utiliser :** Problème où la première approche peut mener à une impasse. Le modèle doit savoir reculer et re-router plutôt que de persister dans une voie sans issue.
**Exemple :** Résolution de puzzles, planification avec contraintes, tout problème nécessitant exploration arborescente avec retours arrière.

---

#### 🦧 Orang-Outan — Cumulative Reasoning
**Technique PE :** Cumulative Reasoning
**Fichier :** `Claude_Orang_Outan.txt`
**Principe :** Accumulation progressive de connaissances. Base simple → ajout de couches → concept complet émergent.
**Quand l'utiliser :** Explication de concepts complexes nécessitant construction progressive. Chaque couche s'appuie sur la précédente.
**Exemple :** Pédagogie de concepts avancés, construction d'arguments complexes, tout raisonnement où l'accumulation progressive est plus efficace que l'exposition directe.

---

#### 🦀 Crabe — Multi-Path Reasoning
**Technique PE :** Multi-Path Reasoning
**Fichier :** `Claude_Crabe.txt`
**Principe :** Exploration omnidirectionnelle simultanée. Plusieurs chemins en parallèle → convergence vers synthèse optimale.
**Quand l'utiliser :** Problème admettant plusieurs approches valides simultanées. Explorer en parallèle puis synthétiser est plus efficace que l'exploration séquentielle.
**Exemple :** Analyse de problèmes complexes, évaluation multi-critères, tout sujet où la richesse vient de la synthèse de routes parallèles.

---

## Cartographie par famille PE

| Famille | Organismes |
|---------|------------|
| **Few-Shot / In-Context** | Perroquet, Araignée, Castor |
| **Zero-Shot / Adaptation** | Caméléon, Chien, Chauve-Souris, Écrevisse, Bernard-l'Ermite |
| **Chain-of-Thought** | Hibou, Singe, Morpho, Aigle, Chenille |
| **Décomposition** | Fourmi, Corail |
| **Ensembling / Consensus** | Chat, Moqueur, Abeille |
| **Self-Refinement** | Scarabée, Nautile |
| **Meta / APE** | Termite |
| **Agents / Outils** | Corbeau |
| **Optimisation** | Coccinelles, ADN, Lézard Anole, Virus, Bactérie |
| **Mémoire / Contexte** | Éléphant, Capucin |
| **Spécialisé** | Renard, Gorille, Ver de Terre, Rat |
| **Multi-Agent / Complexe** | Fourmilière, Saumons, Orang-Outan, Crabe |

---

## Relation avec le Core Marine

| Dimension | Core Marine | Extended Biome |
|-----------|-------------|----------------|
| Cible | Biais comportementaux du modèle | Techniques PE connues |
| Utilisateur | Tout public | Praticiens PE |
| Sélection | Automatique via Reine | Manuelle par l'utilisateur |
| Validation | Empirique (benchmark v1/v2) | Non testé |
| Usage | Correction de défauts | Amplification de capacités |

---

## Avertissement

Aucun de ces prompts n'a été validé empiriquement. Les mappings organisme→technique sont des propositions conceptuelles. Seul le Core Marine a été testé dans le pipeline de benchmark.

---

## Licence

CC-BY-NC — Même licence que le Core Marine.

---

*Variation → Sélection → Optimisation. Progressivement.*
