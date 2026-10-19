# Whanos

> 🚧 Projet en cours : refonte personnelle d'un projet d'infrastructure
> DevOps . L'avancement est détaillé plus bas
> et mis à jour au fur et à mesure.

## Le principe

L'objectif de Whanos est qu'un `git push` sur un dépôt compatible
suffise pour que l'application soit construite dans une image Docker,
publiée dans un registre, puis déployée sur un cluster Kubernetes de
plusieurs machines.

## Architecture prévue

```
Développeur --git push --> Jenkins --> détection du langage
  --> build de l'image --> registre Docker --> cluster Kubernetes (2 nœuds min.)
```

- **Ansible** installe et configure l'infrastructure (Jenkins, registre).
- **Jenkins** surveille les dépôts Git chaque minute et lance la chaîne.
- **Docker** construit les images, une famille d'images par langage.
- **Registre Docker** stocke les images construites.
- **Kubernetes** déploie l'application .

## Langages ciblés

C, Java, JavaScript, Python, Rust

## Avancement

- [ ] Images Docker (standalone et base) pour ~~C~~, ~~Java~~, JavaScript, Python et ~~Rust~~
- [ ] Registre Docker local
- [ ] Jenkins configuré en code
- [ ] Job `link-project` (création automatique d'un job de surveillance)
- [ ] Pipeline de détection du langage, build et push dans le registre
- [ ] Déploiement de l'infrastructure avec Ansible
- [ ] Déploiement Kubernetes sur 2 nœuds

## Lancer le projet

À venir.
