# Cap

Suivi strict de quatre lignes — **porno, weed, malbouffe, achats compulsifs** —
adossé à un budget mensuel réel.

Parce que ces quatre-là ne coûtent pas seulement du temps et de l'estime :
elles coûtent précisément l'argent qu'on n'arrive jamais à mettre de côté. Tant
qu'on ne met pas le chiffre en face, on continue.

**→ [Ouvrir l'application](https://keanaulegoff08-dot.github.io/kea-suivi/)**

---

## Sur iPhone

1. Ouvre le lien ci-dessus **dans Safari**.
2. Bouton *Partager* (le carré avec la flèche, en bas).
3. *Sur l'écran d'accueil* → *Ajouter*.

L'app s'ouvre alors en plein écran, sans barre d'adresse, et **fonctionne hors
ligne** — donc à 23 h comme à 3 h du matin, c'est-à-dire aux heures où elle sert.

---

## Tes données

Le dépôt est public : il contient le code et la configuration de départ
(revenus, charges fixes, coûts de référence).

**Ce que tu saisis au quotidien ne quitte jamais ton téléphone.** Check-ins,
dépenses, notes du journal, séries, envies traversées : tout vit dans le
`localStorage` de Safari. Pas de serveur, pas de compte, aucune requête réseau.
Personne d'autre que toi ne voit une ligne de ça, y compris en clonant ce dépôt.

Conséquence : **exporte régulièrement** (Stats → Exporter). Vider les données de
site dans Safari efface tout.

---

## Les cinq écrans

| Écran | À quoi il sert |
|---|---|
| **Aujourd'hui** | Ce qui reste à dépenser, les 4 séries en cours, les missions du jour, le check-in du soir, la saisie éclair d'une dépense. |
| **Argent** | Solde, trajectoire du cycle, enveloppes, épargne, zone rouge comparée à ta référence, charges fixes, dépenses. |
| **Plan** | Le budget du mois, le plan de survie jusqu'à la paie, les 6 règles, les 5 semaines, les objectifs, le protocole soirée. |
| **Stats** | Calendrier, score sur 30 jours, rechutes par ligne, déclencheurs, argent non dépensé, journal, export/import. |
| **SOS** | Minuteur 10 minutes, respiration 4·7·8, tes chiffres en face, 8 actions de remplacement, journal des envies traversées. |

---

## Ce qui la rend stricte

- **Le check-in du soir est obligatoire.** Un jour non rempli casse la série et
  laisse un trou visible dans le calendrier.
- **Rattrapage limité à 48 h.** Au-delà, la journée est verrouillée : on ne
  réécrit pas le passé, c'est ce qui rend le reste crédible.
- **Score du jour pondéré** — porno 30, weed 25, budget 15, achats compulsifs
  10, malbouffe 10, sport 5, projet 5.
- **L'enveloppe du jour retient la contrainte la plus serrée** : ce qui reste
  sur le compte, ou ce qui reste dans les enveloppes du mois.
- **La zone rouge a un budget de 0 €.** Chaque euro qui y passe s'affiche à côté
  de ce que ce poste te coûtait avant.

## Ce qui la rend encourageante

- Anneaux de progression vers le prochain palier : 1, 3, 7, 14, 21, 30, 60, 90 jours.
- Compteur d'**argent non dépensé**, au coût réel mesuré.
- Journal des envies traversées : la preuve, les soirs où tu n'y crois plus, que
  tu en as déjà traversé.
- Après une rechute, l'app demande le **déclencheur**, jamais une justification.
  En deux semaines, le schéma devient évident.

---

## Modifier la configuration

Tout est éditable dans l'app — *Stats → Mes paramètres* : revenus, jour de paie,
charges fixes (ajout et suppression), enveloppes, objectif d'épargne, coûts de
référence de la zone rouge.

`profil-exemple.json` est le modèle de fichier profil, si tu veux repartir de
zéro ou transférer la configuration sur un autre appareil.

---

## Technique

- `index.html` : l'application entière — HTML, CSS et JS, zéro dépendance.
- Graphiques SVG écrits à la main (calendrier, courbes, barres, colonnes), avec
  survol et vue tableau.
- Palette data-viz validée en clair **et** en sombre : bandes de luminance,
  plancher de chroma, séparation pour les daltonismes, contraste sur la surface.
- PWA : `manifest.json` (icônes en data-URI) + `sw.js` pour le hors-ligne.
- Stockage : `localStorage`, clé `cap.v1`.
- Déploiement : GitHub Actions → GitHub Pages, à chaque push sur `main`.

---

## Si ça déborde

- **Drogues Info Service** — 0 800 23 13 13, anonyme et gratuit, 8 h-2 h
- **Fil Santé Jeunes** — 0 800 235 236, 9 h-23 h
- **CSAPA / Consultation Jeunes Consommateurs** — gratuit, sans rendez-vous
- **3114** — souffrance psychique, 24 h/24

Une app aide à voir clair. Elle ne remplace pas quelqu'un en face de toi.

---

MIT.
