#  Fastclique

**La plateforme de livraison rapide pour tous vos commerces**

## 🎯 Vision du projet

Fastclique est une plateforme de livraison rapide multi-commerce.


## 🚀 Phase 1 — Lancement

Le lancement se concentre sur les **commerces de proximité** :
- Alimentations,
- Boulangeries
- Restaurants
- Et aussi un service a la personne (babysitting,laveur de voiture,coiffeur indépendant et aide au déménagement)

## 📈 Développement futur

Une fois la phase 1 stabilisée, la plateforme a vocation à s'ouvrir aux **grandes enseignes** :
- Mode / vêtements (H&M...)
- Beauté (Sephora...)
- Chaussures (Foot Locker...)
- Électronique
- Et d'autres secteurs à définir

Le but est d'obtenir des contrats avec des grande marque pour leur proposer notre système de livraison rapide qui se fait en moins de 30min.


## 🏬 MyAlim by Fastclique

Un projet futur consiste à créer sa propre enseigne d'alimentation, **MyAlim by Fastclique**, basée sur le concept actuel d'Alim 13, disponible directement sur la plateforme Fastclique.

La signature **« by Fastclique »** est pensée comme une marque de groupe, destinée à être réutilisée pour de futurs commerces propres à l'écosystème Fastclique.

## 🔄 État du repositionnement

L'application est en cour de développement il a atteint un stafe ou il peut etre publier 

**Clients**
- Parcourir les commerces, promos et panier sans compte
- Commande, paiement, suivi en temps réel, code de remise
- Favoris, avis commerce/livreur, services à la personne (rendez-vous)

**Commerçants**
- Dossier d'inscription, formules d'abonnement
- Catalogue avec photos, stock, variantes, promos
- Commandes, rendez-vous, graphiques de ventes

**Livreurs**
- Dossier, choix du secteur, offres de course
- Position en temps réel, historique, gains, retraits

**Admin**
- Validation des dossiers, tarifs et formules
- Retraits, modération des avis, boutique officielle

> État : paiements Stripe en mode test, e-mails non activés.


## 🛠️ Stack technique

- **Front** : React 19, TanStack Start, Vite 7, composants shadcn/ui
- **Back** : fonctions serveur TanStack Start, déployées sur Cloudflare Workers
- **Base de données** : PostgreSQL (Supabase via Lovable Cloud), sécurité par RLS, migrations Drizzle
- **Authentification** : e-mail avec vérification, mot de passe oublié, Google
- **Paiements** : Stripe (mode test), webhook signé
- **IA** : Lovable AI (recherche d'articles)
- **Cartes** : Google Maps
- **Outils** : Bun, TypeScript, ESLint, Prettier
- Développée avec [Lovable](https://lovable.dev)

## 📂 Structure du projet

## Structure du projet

    src/
    ├── routes/                      # Pages (routage par fichiers, TanStack Router)
    │   ├── index.tsx                # Accueil
    │   ├── auth.tsx                 # Connexion / choix du profil
    │   ├── reset-password.tsx       # Mot de passe oublié
    │   ├── boutiques.tsx            # Liste des commerces
    │   ├── commerce.$commerceId.tsx # Fiche commerce
    │   ├── promotions.tsx           # Promotions
    │   ├── services.tsx             # Services à la personne
    │   ├── panier.tsx               # Panier
    │   ├── paiement.retour.tsx      # Retour de paiement
    │   ├── commandes.tsx            # Suivi de commande
    │   ├── profil.tsx               # Profil client
    │   ├── contact.tsx              # Contact
    │   ├── devenir-commercant.tsx   # Inscription commerçant
    │   ├── espace-commerce.tsx      # Espace commerçant
    │   ├── livreur.*.tsx            # Espace livreur (courses, dossier, gains, historique, avis)
    │   ├── admin.tsx                # Espace admin
    │   └── api/public/payments/     # Webhook de paiement
    ├── components/                  # Composants (AppHeader, CarteProximite, SuiviCommande...)
    │   ├── avis/                    # Notes et avis
    │   └── ui/                      # Composants shadcn/ui
    ├── lib/                         # Logique (panier, commandes, session, paiements, e-mails)
    ├── integrations/                # Connexion à la base (Supabase)
    └── styles.css
    drizzle/                         # Schéma et migrations de la base
    scripts/                         # Tests SQL


## 🚀 Démarrage local

## Démarrage en local

Prérequis : Node.js 22+ et Bun (ou npm).

    git clone <url-du-dépôt>
    cd <nom-du-dépôt>
    bun install      # ou : npm install
    bun run dev      # ou : npm run dev

Autres commandes : `build`, `preview`, `lint`, `format`.

Les clés (Cloud, Stripe, webhook) se renseignent dans un fichier `.env` local. Ne jamais les publier.

