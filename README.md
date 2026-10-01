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
| 🎯 **Activités** | Voler (arraché → fourgon blindé), agression, **vol de véhicules**, **boîte de nuit**, **vol à la tire**, **racket de passants et de commerçants**, **salle de sport**, consommer, cure de désintox, hôpital/soins, chirurgie, **emploi légal**, se mettre au vert. En prison : musculation, bagarres, trafic, surin, protection, corruption, évasion. |
| 💊 **Trafic & Marché** | Stock, achat en gros, vente au détail (clients limités par mois), vente en gros, comparateur de prix par ville, Go Fast (mini-jeu à choix), importations (mule, camion, conteneur, avion privé), voyages, laboratoires. En détention, l'onglet devient **🚬 Trafic en détention**. |
| 🕴️ **Mafia & Business** | Hiérarchie (Guetteur → Dealeur → Lieutenant → Boss local → Parrain), recrutement, sous-fifres (féliciter, sanctionner, virer, éliminer, quotas), guerres de territoire, **arsenal & trafic d'armes**, clubs & entreprises (dont **strip clubs**), blanchiment, banque & usuriers, **corruption de la police**. |
| 💎 **Achats & Patrimoine** | Vêtements par emplacement (haut, bas, chaussures, veste — de Zara à Stüssy, Ami Paris, Rick Owens et Chrome Hearts), bijoux & montres (Rolex Daytona, Audemars Piguet, chaînes serties), véhicules, immobilier (capacité de planque, coffre, garage, sécurité), armurerie et modifications d'armes, **planques de cash**, **garage**, profil & style, statistiques. |

**Mécaniques clés**

- **Combat au tour par tour** (altercations, agressions, règlements de compte, bagarres en boîte, prison) : barres de PV, journal de combat, actions *Attaquer / Tirer* ou *S'enfuir*, riposte automatique de l'adversaire. L'arme équipée et la musculature modulent les dégâts ; les combats armés se terminent par la mort d'un des deux participants ou une fuite réussie, les bagarres à mains nues par un K.O.
- **Musculature / Force** (0–100 %) : salle de sport (musculation, cardio, boxe), fonte si tu ne t'entraînes pas ; **stéroïdes anabolisants** (force ↑↑, agressivité, dépendance, cœur et foie abîmés).
- **Mini-jeux de consommation réalistes** : séquences animées pas à pas selon l'origine du produit — flacon ambré américain « Rx Pharmacy » à bouchon sécurité (dévisser → faire tomber un cachet → avaler), boîte de pharmacie française à bandeau coloré, sirop codéiné (vraie pinte Actavis de 473 ml ou flacon Euphon en verre de 300 ml) versé dans un double cup, complété au Sprite, puis glaçons, héroïne (cuillère → briquet → seringue → injection avec distorsion de l'écran), pochette zippée d'ecstasy au logo imprimé, cigarettes (paquet neutre, volé ou de contrebande → briquet → fumer), pipe en verre (crack, méth), fiole de GHB, joint, poudre. Une étape peut rater et doit être recommencée ; les effets s'appliquent à la fin.
- **Stress** 😰 : monte avec les descentes, règlements de compte, combats, la prison, les dettes et le manque ; baisse avec le sport, la fête, la clope, le cannabis, les opiacés… Au-delà de 60 %, malus aux crimes et aux combats ; au-delà de 80 %, la santé trinque.
- **Emploi légal** (chauffeur-livreur, manutentionnaire, agent de sécurité, barman, gérant) : salaire propre versé en banque, mais le **casier judiciaire** bloque certains postes et fait chuter les chances d'embauche.
- **Corruption** : police locale achetée par ville (versement mensuel ou gros pot-de-vin de 12 mois) → contrôles, descentes et interceptions de go fast fortement réduits ; au tribunal, **graisser la patte du juge** ou **l'acheter**.
- **Vol de véhicules** (discrétion, habileté) : revente au receleur ou garage — les voitures volées servent de véhicules sacrifiables et intraçables pour les go fast.
- **Trafic en détention** : cantine clandestine payée en paquets de cigarettes (doses, poinçon, protection), **téléphone clandestin** (codétenu ou surveillant corrompu) indispensable pour gérer la mafia depuis la cellule — confisqué lors des fouilles.
- **Planques de cash** : chaque bien a un coffre plafonné (studio 50 000 €, villa 2 M€, strip club 1 M€) à l'abri des vols et contrôles ; une descente peut toutefois en découvrir une.
- **Arsenal** : modifications d'armes (silencieux, chargeur tambour, laser, canon long), caisses d'armes (×10, ×50 AK-47) qui augmentent la **puissance militaire** (guerres, dissuasion), revente internationale et ateliers clandestins de **ghost guns** (imprimantes 3D, usinage).
- **Dealeurs automatiques** : ils écoulent le produit le plus rentable du stock selon un quota réglable ; postés dans ta boîte de nuit ou ton strip club, ils vendent MDMA, cocaïne et kétamine à forte marge, sans risque si la police locale est achetée.
- **Strip clubs** : revenus légaux, blanchiment, coffre, stockage d'armes ; améliorations (sécurité, salons VIP, sono & déco) ; escortes (majeures) dont les revenus dépendent du prestige et de la protection armée — avec un risque d'enquête pour proxénétisme aggravé si la police n'est pas tenue.
- **Mode détention** : interface dédiée (thème orange, « Purger +1 mois »), journal mois par mois, corvées, trafics internes, alliances de détenus et **menace des cartels rivaux** (intimidations, tentatives d'assassinat) selon ton historique. Choix : se défendre, soudoyer les gardes ou négocier sa protection.
- **Profil & Style** : touche ton avatar pour voir ta tenue portée (silhouette), tes accessoires et ton bonus de respect / statut social.
- 21 produits (médicaments détournés dont Subutex, Skenan, Rohypnol et Adderall, drogues dures dont crack, fentanyl et GHB, drogues douces, stéroïdes anabolisants, cigarettes légales, volées ou de contrebande) avec marques, qualité 1–100 et prix dynamiques propres à 6 villes (Marseille, Paris, Amsterdam, Medellín, Culiacán, Miami).
- Les gros volumes font bouger les prix ; les chocs de marché (pénuries, arrivages massifs) tombent chaque mois.
- Consommation : boosts temporaires (énergie, réussite des crimes, respect), addiction, crises de manque, overdoses (mélange opioïdes + benzos très dangereux), rechutes.
- Deux argents : le **liquide** (sale, saisissable lors des descentes) et la **banque** (blanchie via tes commerces, idéale pour l'immobilier et le luxe sans éveiller les soupçons).
- Jauge **Police** : descentes, contrôles, infiltrés, flics ripoux ; la sécurité de ton logement, la chirurgie clandestine et la corruption la font baisser.
- Justice : avocats (commis d'office → ténor du barreau), juge graissé ou acheté, casier judiciaire détaillé.
- Énergie ⚡ : 4 actions par mois (plus avec des stimulants, une de moins avec un emploi légal).

## Architecture du code

JavaScript vanille, structuré en objets dans la balise `<script>` :

- `PlayerData` – état du joueur, stats dérivées (respect, puissance de feu, capacité…)
- `MarketData` – prix, qualité, tendances et demande par ville
- `Inventory` – stock de marchandise (quantité / qualité moyenne)
- `Actions` – toutes les actions du joueur (crimes, marché, justice, finances…)
- `GoFast`, `Crew`, `Shop` – mini-jeu go fast, gestion de l'équipe, boutiques et garde-robe
- `Combat`, `Ritual`, `Night`, `Street`, `Gym`, `Prison`, `Profile` – combats au tour par tour, mini-jeux de consommation, vie nocturne, délits de rue, musculation, détention (cantine, téléphone, fouilles), profil & style
- `Police`, `Jobs`, `Cars`, `Vault`, `Arsenal`, `Armory`, `Strip` – corruption, emploi légal, vol de véhicules, planques de cash, arsenal & ateliers, modifications d'armes, strip clubs
- `Monthly` – boucle mensuelle (équipe, labos, blanchiment, charges, dettes, police…)
- `Events` – événements aléatoires à choix multiples
- `UI` / `V` – rendu (HUD, journal, panneaux, modales) et vues des onglets
- `Game` – création, vieillissement, mort, sauvegarde `localStorage` et migration des anciennes sauvegardes (v1 → v3)
