# Introduction aux architectures applicatives

## Objectifs de cette section

Dans cette introduction, nous allons poser les bases de l’architecture applicative et comprendre son importance.  
À la fin de cette section, vous serez capable de :

- Définir ce qu’est une **architecture applicative** et pourquoi elle est essentielle.
- Identifier les critères qui influencent **le choix d’une architecture**.
- Comprendre comment **UML** va nous aider à représenter et analyser les architectures.
- Mettre en place un **projet backend simple (gestion de tâches)** qui servira d’exemple tout au long du cours.

---

## 1. Qu'est-ce qu'une architecture applicative ?

L’architecture d’une application définit **comment ses composants sont organisés et interagissent entre eux**. Elle
structure le code et impacte directement :

- **La maintenabilité** : facilité à faire évoluer l’application.
- **La scalabilité** : capacité à supporter une charge croissante.
- **La performance** : rapidité et efficacité du traitement des données.
- **La sécurité** : protection des données et des interactions entre les services.

### Exemple concret :

Une simple **application de gestion de tâches** peut être architecturée de plusieurs façons :

- **En monolithique**, tout le code est regroupé dans une seule application.
- **En n-tiers**, le frontend, le backend et la base de données sont séparés.
- **En microservices**, chaque fonctionnalité (gestion des tâches, des utilisateurs, etc.) est un service indépendant.

---

## 2. Comment choisir une architecture ?

Il n’existe pas d’**architecture parfaite**, mais un ensemble de **compromis** adaptés aux besoins.

### Les critères de choix :

| Critère                            | Impact sur l’architecture                                                                                                         |
|------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **Complexité du projet**           | Un petit projet fonctionne bien en **monolithique**, un projet plus vaste peut nécessiter du **n-tiers** ou du **microservices**. |
| **Fréquence des mises à jour**     | Une mise à jour fréquente de certaines fonctionnalités favorise une **approche modulaire** (microservices, hexagonale).           |
| **Performance et scalabilité**     | Une application avec **beaucoup d’utilisateurs simultanés** doit être **scalable** (microservices, API séparées).                 |
| **Coût et temps de développement** | Un monolithe **est rapide à développer**, alors qu’une architecture microservices **est plus longue et coûteuse**.                |

---

## 3. UML : un outil essentiel pour comprendre les architectures

Nous utiliserons **UML (Unified Modeling Language)** pour représenter **les architectures et leurs composants**.  
Pas besoin d’être expert, l’idée est d’utiliser **quelques diagrammes simples** :

- **Diagramme de cas d’utilisation** : interactions entre l’utilisateur et le système.
- **Diagramme de composants** : organisation des blocs applicatifs.
- **Diagramme de classes** : modélisation des entités principales.
- **Diagramme de déploiement** : où et comment sont hébergés les composants.

### Exemple UML : Diagramme de cas d'utilisation pour notre gestion de tâches

![Diagramme de cas d'utilisation](../images/cas-utilisation-gestion-taches.png)

---

## 4. Mise en place du projet backend : les développeurs à l'oeuvre

Nous allons développer **une application de gestion de tâches** qui nous servira d’exemple tout au long du cours.  
Elle sera proposée **en PHP et en JavaScript (Node.js)** pour que chacun puisse travailler avec son langage préféré.

### **Arborescence du projet**

```bash
/gestion-taches
├── /php                   # Implémentation en PHP
│   ├── index.php          # Point d'entrée
│   ├── db.php             # Connexion à la base de données
│   ├── Task.php           # Modèle Task
│   ├── taskController.php # Contrôleur des tâches
│   ├── api.php            # API REST pour gérer les tâches
│   ├── .env               # Configuration de la base de données
│   ├── composer.json      # Dépendances PHP
│
├── /nodejs                # Implémentation en Node.js
│   ├── index.js           # Point d'entrée
│   ├── db.js              # Connexion à la base de données
│   ├── task.js            # Modèle Task
│   ├── taskController.js  # Contrôleur des tâches
│   ├── api.js             # API REST pour gérer les tâches
│   ├── .env               # Configuration de la base de données
│   ├── package.json       # Dépendances Node.js
│
└── README.md              # Documentation
```

---

## 5. Mise en pratique pour les administrateurs infrastructure

L’objectif est d’analyser l’infrastructure nécessaire au bon fonctionnement de l’application et d’anticiper son
déploiement, sa gestion et sa maintenance.

### Identification des composants techniques

**Objectif :**  
Recenser les éléments techniques nécessaires à l’hébergement et au fonctionnement de l’application.

- Quels sont **les services clés** qui composent l’application ?
- Quels sont les **besoins spécifiques** en matière de serveur web, base de données et API ?
- Quels sont les **fichiers de configuration** et variables d’environnement à prendre en compte ?

**Livrable attendu** : Un schéma des composants de l’application avec une brève description de leur rôle.

---

### Préparation de l’environnement d’hébergement

**Objectif :**  
Identifier la meilleure solution d’hébergement et prévoir une configuration adaptée.

- Quelle solution choisir entre **serveur physique, VPS, hébergement cloud ou conteneurs** ?
- Quelle **configuration minimale** (CPU, RAM, stockage) serait recommandée pour un environnement de test et un
  environnement de production ?
- Quels logiciels et dépendances doivent être installés sur le serveur pour exécuter l’application ?
    - (Ex : PHP + MySQL ou Node.js + PostgreSQL)

**Livrable attendu** : Un document précisant les prérequis matériels et logiciels pour héberger l’application.

---

### Planification des sauvegardes et maintenance

**Objectif :**  
Définir une stratégie de sauvegarde et de maintenance.

- Quels fichiers et bases de données doivent être sauvegardés ?
- À quelle fréquence effectuer des **sauvegardes automatiques** ? (quotidien, hebdomadaire…)
- Quels outils peuvent être utilisés pour les sauvegardes et la restauration ? (ex : `mysqldump`, `pg_dump`, snapshots,
  sauvegarde S3…)
- Comment planifier des **mises à jour régulières** des dépendances et du serveur ?

**Livrable attendu** : Un plan de sauvegarde avec les fichiers concernés et la fréquence recommandée.

---

### Sécurité et gestion des accès

**Objectif :**  
Établir les bonnes pratiques de sécurité pour protéger l’application.

- Quels ports réseau doivent être ouverts et quels services doivent être protégés ?
- Quels mécanismes d’**authentification et de gestion des accès** mettre en place ?
    - Gestion des **droits sur le serveur** (utilisateur root vs utilisateur restreint).
    - Utilisation d’un **pare-feu (iptables, UFW)**.
    - Restriction d’accès aux **services sensibles**.
- Comment chiffrer les données sensibles stockées sur le serveur (ex: fichiers `.env`, bases de données) ?

**Livrable attendu** : Une liste des mesures de sécurité à appliquer sur le serveur d’hébergement.

---

### Hébergement et mise en production

**Objectif :**  
Préparer une stratégie de déploiement pour un environnement de production stable.

- Comment structurer un **workflow de déploiement** : manuel, semi-automatisé ou CI/CD ?
- Quels outils peuvent être utilisés pour l’automatisation du déploiement ? (Ex: Ansible, Docker, GitHub Actions, GitLab
  CI/CD)
- Quelle **stratégie de monitoring** mettre en place pour suivre l’état du serveur et des services ? (Ex: Prometheus,
  Grafana, Zabbix…)
- Comment prévoir la montée en charge et la scalabilité de l’application en fonction du trafic ?

**Livrable attendu** : Un document listant les outils et stratégies recommandés pour le déploiement et la
surveillance.
