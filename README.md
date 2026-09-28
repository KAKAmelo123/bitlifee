# Crime Life 🩸

Simulation de vie textuelle façon **BitLife**, dans un univers « Crime & Mafia » sombre, pensée pour le navigateur mobile.
De guetteur à parrain : chaque clic sur **« Vieillir +1 mois »** fait avancer ta vie d'un mois.

> Œuvre de fiction. Aucune incitation à la consommation de drogues ni à la commission de crimes.

## Lancer le jeu

Tout tient dans un seul fichier : **`index.html`** (HTML + CSS + JavaScript vanille, aucune dépendance).

- En local : ouvrir `index.html` dans un navigateur.
- En ligne : héberger le fichier tel quel (GitHub Pages, Netlify, n'importe quel serveur statique).

La partie est sauvegardée automatiquement dans le `localStorage` du navigateur. Pour recommencer : ⚙️ → Nouvelle vie.

## Contenu

| Onglet | Contenu |
| --- | --- |
| 🎯 **Activités** | Voler (arraché → fourgon blindé), agression, **boîte de nuit**, **vol à la tire**, **racket de passants et de commerçants**, **salle de sport**, consommer, cure de désintox, hôpital/soins, chirurgie, se mettre au vert. En prison : musculation, bagarres, trafic, surin, protection, corruption, évasion. |
| 💊 **Trafic & Marché** | Stock, achat en gros, vente au détail (clients limités par mois), vente en gros, comparateur de prix par ville, Go Fast (mini-jeu à choix), importations (mule, camion, conteneur, avion privé), voyages, laboratoires. |
| 🕴️ **Mafia & Business** | Hiérarchie (Guetteur → Dealeur → Lieutenant → Boss local → Parrain), recrutement, sous-fifres (féliciter, sanctionner, virer, éliminer), guerres de territoire, clubs & entreprises, blanchiment, banque & usuriers. |
| 💎 **Achats & Patrimoine** | Vêtements par emplacement (haut, bas, chaussures, veste — de Zara à Chrome Hearts), bijoux & montres, véhicules, immobilier (capacité de planque, sécurité), armurerie, profil & style, statistiques. |

**Mécaniques clés**

- **Combat au tour par tour** (altercations, agressions, règlements de compte, bagarres en boîte, prison) : barres de PV, journal de combat, actions *Attaquer / Tirer* ou *S'enfuir*, riposte automatique de l'adversaire. L'arme équipée et la musculature modulent les dégâts ; les combats armés se terminent par la mort d'un des deux participants ou une fuite réussie, les bagarres à mains nues par un K.O.
- **Musculature / Force** (0–100 %) : salle de sport (musculation, cardio, boxe), fonte si tu ne t'entraînes pas ; **stéroïdes anabolisants** (force ↑↑, agressivité, dépendance, cœur et foie abîmés).
- **Mini-jeux de consommation** : séquences animées pas à pas (comprimés : ouvrir la boîte → blister → prendre ; sirop : dévisser → verser → consommer ; cannabis : effriter → feuille → rouler → allumer). Une étape peut rater et doit être recommencée ; les effets s'appliquent à la fin.
- **Mode détention** : interface dédiée (thème orange, « Purger +1 mois »), journal mois par mois, corvées, trafics internes, alliances de détenus et **menace des cartels rivaux** (intimidations, tentatives d'assassinat) selon ton historique. Choix : se défendre, soudoyer les gardes ou négocier sa protection.
- **Profil & Style** : touche ton avatar pour voir ta tenue portée (silhouette), tes accessoires et ton bonus de respect / statut social.
- 14 substances (médicaments détournés, drogues dures et douces, stéroïdes anabolisants) avec marques, qualité 1–100 et prix dynamiques propres à 6 villes (Marseille, Paris, Amsterdam, Medellín, Culiacán, Miami).
- Les gros volumes font bouger les prix ; les chocs de marché (pénuries, arrivages massifs) tombent chaque mois.
- Consommation : boosts temporaires (énergie, réussite des crimes, respect), addiction, crises de manque, overdoses (mélange opioïdes + benzos très dangereux), rechutes.
- Deux argents : le **liquide** (sale, saisissable lors des descentes) et la **banque** (blanchie via tes commerces, idéale pour l'immobilier et le luxe sans éveiller les soupçons).
- Jauge **Police** : descentes, contrôles, infiltrés, flics ripoux ; la sécurité de ton logement et la chirurgie clandestine la font baisser.
- Justice : avocats (commis d'office → ténor du barreau), corruption du juge, casier judiciaire.
- Énergie ⚡ : 4 actions par mois (plus avec des stimulants).

## Architecture du code

JavaScript vanille, structuré en objets dans la balise `<script>` :

- `PlayerData` – état du joueur, stats dérivées (respect, puissance de feu, capacité…)
- `MarketData` – prix, qualité, tendances et demande par ville
- `Inventory` – stock de marchandise (quantité / qualité moyenne)
- `Actions` – toutes les actions du joueur (crimes, marché, justice, finances…)
- `GoFast`, `Crew`, `Shop` – mini-jeu go fast, gestion de l'équipe, boutiques et garde-robe
- `Combat`, `Ritual`, `Night`, `Street`, `Gym`, `Prison`, `Profile` – combats au tour par tour, mini-jeux de consommation, vie nocturne, délits de rue, musculation, détention, profil & style
- `Monthly` – boucle mensuelle (équipe, labos, blanchiment, charges, dettes, police…)
- `Events` – événements aléatoires à choix multiples
- `UI` / `V` – rendu (HUD, journal, panneaux, modales) et vues des onglets
- `Game` – création, vieillissement, mort, sauvegarde `localStorage`
