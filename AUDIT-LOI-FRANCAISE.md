# Audit loi française — Fastclique (30/10/2026)

Audit fait avec le prompt de la vidéo TikTok « L'IA dans votre app peut coûter 75 000 € ».
Les corrections ont été appliquées dans le projet Lovable « Fastclique ». Les 141 tests passent et le code compile.

> Ce travail ne remplace pas un avocat.

| Point | Statut | Correction |
|---|---|---|
| 1. Mineurs à l'inscription | Corrigé | Case « J'ai 15 ans ou plus ». Sous 15 ans : newsletter bloquée, accord parental pour la carte Google. Case CGU séparée de la newsletter. |
| 1. Alcool | Corrigé | Case « Je certifie avoir 18 ans » obligatoire si le panier contient de l'alcool. Elle est enregistrée avec la commande. Rappel de vérifier une pièce d'identité affiché au livreur et au commerçant. |
| 2. Polices et services tiers | Corrigé | Plus Jakarta Sans hébergée dans l'app, Google Fonts retiré. Avant tout clic, seule la base de données est contactée. |
| 3. Cookies et Google Maps | Corrigé | Bannière « Tout accepter » / « Tout refuser » de même taille, plus « Personnaliser ». La carte reste masquée tant que l'utilisateur n'a pas accepté, avec un bouton « Afficher la carte (Google Maps) ». Le choix est gardé 6 mois maximum. « Gérer mes cookies » est accessible dans le profil, la page Cookies et en bas de l'accueil. |
| 4. E-mails marketing | Partiel | L'expéditeur « Fastclique », les règles d'envoi et la page de désinscription sont prêts. Il manque un service d'e-mails marketing séparé, avec un lien de désinscription en un clic. |
| 5. Paiement | Corrigé | Le « Total TTC » s'affiche juste avant le bouton, renommé « Commande avec obligation de paiement ». Ajout de l'information sur la rétractation de 14 jours et sur l'exception de l'art. L221-28. Chaque formule affiche son prix, sa durée et le renouvellement automatique. Bouton « Résilier mon abonnement » ajouté. |
| 6. Pages légales | Corrigé | Mentions légales, CGU/CGV, Politique de confidentialité et Cookies, avec les champs `[À COMPLÉTER]`. |
| 6. Signaler un contenu | Corrigé | Formulaire ouvert aux visiteurs, limité à 10 envois par heure. Les signalements s'exportent depuis l'admin. |
| 6. Licences des images | À faire | Les photos coca, oreo, lu, oasis, chips, cafe, pate-tartiner, pates et jus-orange montrent des marques et leur origine est inconnue. Il faut les remplacer ou obtenir une autorisation. |

## Reste à faire
- Remplir les champs `[À COMPLÉTER]` : raison sociale, forme juridique, SIRET, siège, directeur de publication, hébergeur, e-mail, médiateur de la consommation.
- Faire passer la connexion Google par la case 15 ans et la case CGU.
- Rappeler aux commerçants de classer les alcools dans le rayon « Alcool », car la détection se fait sur le rayon et le nom de l'article.
- Tester une commande payée de bout en bout (mode test).
- Faire valider les textes juridiques et les durées de conservation par un juriste.
