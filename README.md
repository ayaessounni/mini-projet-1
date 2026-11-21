# Mini-projet 1 : application Flask conteneurisée

Petite application web Flask qui affiche un message configurable.

## Image Docker Hub
`ayaessounni/mini-app` (versions : 1.0.0, 1.0.1, alias 1.0)

## Lancer l'application
    docker run -d --name app -p 5000:5000 \
      -e MESSAGE="Salut" --memory 256m --cpus 0.5 \
      ayaessounni/mini-app:1.0.1

Puis ouvrir http://localhost:5000

## Variables d'environnement
| Variable | Défaut | Rôle |
|----------|--------|------|
| MESSAGE | Bonjour depuis Docker v1.0.1 ! | Message affiché sur la page |

## Construire l'image
    docker build -t ayaessounni/mini-app:1.0.1 .
