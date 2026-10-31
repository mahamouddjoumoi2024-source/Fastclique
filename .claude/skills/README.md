# Skills son pour le montage vidéo

Skills Claude Code pour faire le son des vidéos (pubs, TikTok, démos de l'app).
Copiés depuis https://github.com/Leonxlnx/earshot (commit 591fa3e, licence MIT, voir `LICENSE-earshot`).

| skill | à quoi il sert |
|---|---|
| `earshot` | donne des « oreilles » à Claude : décrire un son, vérifier la synchro avec l'image, critiquer la bande-son |
| `real-sound` | construit une bande-son avec de vrais sons sous licence (Freesound, Mixkit, Pixabay), calés sur les coupes |

## Installation (une fois, sur ta machine)

Les skills ont besoin du programme earshot et de ffmpeg :

```
git clone https://github.com/Leonxlnx/earshot
cd earshot && python -m venv .venv && .venv/bin/pip install -e ".[mcp]"
.venv/bin/python -m earshot doctor
```

Optionnel, pour que Claude garde les modèles chargés :
`claude mcp add earshot --scope user -- /chemin/vers/earshot/.venv/bin/python -m earshot mcp`

## Openverse

Openverse (https://openverse.org) n'est pas un skill : c'est un moteur de recherche gratuit de sons sous
licence libre. Vérifie toujours la licence de chaque son (certaines demandent de citer l'auteur ou
interdisent l'usage commercial).
