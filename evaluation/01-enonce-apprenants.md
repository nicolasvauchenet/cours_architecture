# Évaluation : Architectures et Hébergement

### Travail individuel - Durée : 1h30

---

## 1. QCM (5 questions - 10 points)

**Consigne : Une seule réponse correcte par question.**

1. Quelle architecture est la plus adaptée pour une application nécessitant une séparation stricte entre la gestion des
   utilisateurs, la gestion des paiements et l'affichage des contenus ?
    - [ ] Monolithique
    - [ ] N-tiers
    - [ ] Microservices
    - [ ] Hébergement mutualisé

2. Dans une architecture n-tiers, quel élément est responsable du stockage et de la gestion des données ?
    - [ ] Frontend
    - [ ] Middleware
    - [ ] Backend
    - [ ] Base de données

3. Quelle technologie est spécifiquement conçue pour permettre le déploiement et l’exécution d’applications sous forme
   de conteneurs isolés ?
    - [ ] Ansible
    - [ ] Docker
    - [ ] Apache
    - [ ] PostgreSQL

4. Quelle est l’utilité principale d’un reverse proxy dans une architecture web ?
    - [ ] Gérer les transactions bancaires
    - [ ] Servir uniquement des fichiers statiques
    - [ ] Distribuer les requêtes vers plusieurs serveurs backend
    - [ ] Remplacer un pare-feu pour filtrer les accès

5. Quelle solution permet de garantir une meilleure isolation entre les applications hébergées sur un même serveur ?
    - [ ] Hébergement mutualisé
    - [ ] Virtualisation avec VPS
    - [ ] Serveur dédié sans conteneurisation
    - [ ] Stockage local sans partitionnement

---

## 2. Vrai/Faux (5 questions - 10 points)

**Consigne : Indiquez si l’affirmation est vraie ou fausse, puis justifiez votre réponse en une phrase.**

1. Une API REST peut être utilisée dans une architecture monolithique. (Vrai / Faux)

2. Un hébergement mutualisé est recommandé pour un site web à fort trafic. (Vrai / Faux)

3. Docker et une machine virtuelle offrent exactement le même type d’isolation. (Vrai / Faux)

4. Une application en microservices facilite les mises à jour et la scalabilité. (Vrai / Faux)

5. Les sauvegardes automatiques ne sont pas nécessaires si une base de données est bien optimisée. (Vrai / Faux)

---

## 3. Questions courtes (5 questions - 10 points)

**Consigne : Répondez en 2 à 3 phrases maximum.**

1. Pourquoi une architecture n-tiers améliore-t-elle la sécurité par rapport à un monolithe ?

2. Quelles sont les différences majeures entre un VPS et un hébergement mutualisé ?

3. Comment un administrateur peut-il limiter les risques d’attaques sur un serveur web ?

4. Pourquoi les logs d’un serveur sont-ils importants pour un administrateur ?

5. Citez une situation où l’utilisation de microservices serait contre-productive.

---

## 4. Étude de cas / Analyse d’un problème (30 min - 15 points)

**Consigne : Lisez le cas suivant et répondez aux questions en expliquant vos choix.**

### Contexte

Une entreprise spécialisée dans la vente de matériel informatique en ligne souhaite développer une nouvelle plateforme
e-commerce.  
Le site doit permettre aux utilisateurs de :

- Naviguer dans un catalogue de produits (PC, composants, accessoires).
- Ajouter des produits au panier et passer commande.
- Gérer leur compte utilisateur et suivre leurs commandes.

L’entreprise veut une solution évolutive et sécurisée, capable de supporter une montée en charge lors d’événements
promotionnels.  
L’équipe technique est composée de développeurs et d’administrateurs système.

---

### Questions d’analyse

1. Quelle architecture recommandez-vous ?

- Justifiez votre choix entre monolithique, n-tiers et microservices.

2. Comment héberger cette application ?

- Proposez une solution simple d’hébergement (serveur physique, VPS, cloud).

3. Quelles sont les contraintes techniques à prendre en compte ?

- Par rapport aux performances et à la scalabilité.

4. Quelles mesures de sécurité appliquer ?

- Donnez trois bonnes pratiques pour sécuriser le système.

---

## 5. Rédaction technique / Justification d’un choix (30 min - 15 points)

Consigne : Choisissez l’un des sujets suivants et rédigez une réponse argumentée (10-15 lignes).

### Sujet 1

- Votre entreprise décide d’héberger une application sur un serveur VPS.
- Expliquez les étapes de mise en place (installation, configuration, déploiement) et les risques à éviter.

### Sujet 2

- Vous devez sécuriser une API REST en production.
- Listez et expliquez trois bonnes pratiques essentielles à mettre en place.

### Sujet 3

- Votre application doit gérer un grand volume de requêtes simultanées.
- Expliquez comment optimiser les performances du backend pour éviter les ralentissements.

---

Notation : 60 points au total

- QCM : 10 points
- Vrai/Faux + justification : 10 points
- Questions courtes : 10 points
- Étude de cas : 15 points
- Rédaction technique : 15 points

Bonne chance !
