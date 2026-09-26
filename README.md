#  Fastclique

**La plateforme de livraison rapide pour tous vos commerces**

## 🎯 Vision du projet

Fastclique est une plateforme de livraison rapide multi-commerce. Le projet est né d'un ancien concept centré uniquement sur l'alimentation (à Marseille), aujourd'hui repositionné pour couvrir bien plus large : tous types de commerces, pas seulement l'alimentaire.

L'idée est d'adapter l'application/site existant à cette nouvelle vision, plutôt que de repartir de zéro, si la structure actuelle peut être réutilisée.

## 🚀 Phase 1 — Lancement

Le lancement se concentre sur les **commerces de proximité** :
- Alimentations, épiceries, supérettes
- Boulangeries
- Restaurants
- Pharmacies
- Autres commerces de proximité

## 📈 Développement futur

Une fois la phase 1 stabilisée, la plateforme a vocation à s'ouvrir aux **grandes enseignes** :
- Mode / vêtements (H&M...)
- Beauté (Sephora...)
- Chaussures (Foot Locker...)
- Électronique
- Et d'autres secteurs à définir

## 🏬 MyAlim by Fastclique

Un projet futur consiste à créer sa propre enseigne d'alimentation, **MyAlim by Fastclique**, basée sur le concept actuel d'Alim 13, disponible directement sur la plateforme Fastclique.

La signature **« by Fastclique »** est pensée comme une marque de groupe, destinée à être réutilisée pour de futurs commerces propres à l'écosystème Fastclique.

## 🔄 État du repositionnement

L'application (encore nommée « My Alim » en interne) est en cours de bascule vers l'identité Fastclique. Ce qui reste à faire :
- [ ] Remplacer l'identité My Alim par Fastclique dans les écrans, textes et métadonnées
- [ ] Introduire les catégories de commerces et permettre le parcours catégorie → commerce → produits
- [ ] Préserver la carte, la recherche, le panier et les commandes avec un vocabulaire multi-commerce
- [ ] Vérifier l'affichage et le parcours sur ordinateur et mobile ; préciser les limites du paiement et du suivi simulés

## 🛠️ Stack technique

- **Framework** : [TanStack Start](https://tanstack.com/start) (React 19 + TanStack Router + Vite)
- **UI** : Tailwind CSS 4, shadcn/ui (Radix UI), lucide-react
- **Formulaires / validation** : React Hook Form + Zod
- **Carte** : Leaflet
- **Autres** : TanStack Query, Recharts, date-fns, Sonner
- **Outillage** : TypeScript, ESLint, Prettier, Bun (lockfile)
- Développée avec [Lovable](https://lovable.dev)

## 📂 Structure du projet

```
src/
├── routes/                  # Pages (file-based routing TanStack Router)
│   ├── index.tsx             # Accueil
│   ├── auth.tsx               # Connexion / choix du profil
│   ├── boutiques.tsx          # Liste des commerces
│   ├── commerce.$commerceId.tsx  # Fiche commerce
│   ├── panier.tsx             # Panier
│   ├── commandes.tsx          # Suivi de commande
│   └── espace-commerce.tsx    # Espace commerçant
├── components/               # Composants (AppHeader, CarteProximite, SuiviCommande...)
│   └── ui/                   # Composants shadcn/ui
├── lib/                      # Logique (panier, commandes, session, données)
└── styles.css
```

## 🚀 Démarrage local

```sh
git clone <url-du-repo>
cd <nom-du-repo>
npm i
npm run dev
```
