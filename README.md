#  Projet DevOps – Application de Gestion des Absences

## 📌 Présentation du projet

Ce projet consiste à développer et déployer une application web de gestion des absences des étudiants en mettant en œuvre une approche **DevOps**.

L'objectif est d'automatiser et de faciliter le cycle de vie de l'application, depuis son développement jusqu'à son déploiement, en utilisant des outils modernes de conteneurisation, d'orchestration, d'Infrastructure as Code et d'intégration continue.

## 🎯 Objectifs

- Développer une application web de gestion des absences.
- Conteneuriser l'application avec Docker.
- Automatiser les processus avec une pipeline CI/CD.
- Orchestrer le déploiement avec Kubernetes.
- Provisionner l'infrastructure avec Terraform.
- Automatiser la configuration des serveurs avec Ansible.
- Améliorer la portabilité, la maintenabilité et la reproductibilité du déploiement.

## 🛠️ Technologies et outils utilisés

| Technologie | Rôle |
|---|---|
| Python / Flask | Développement de l'application web |
| HTML / CSS | Interface utilisateur |
| SQLite | Stockage des données |
| Docker | Conteneurisation |
| Kubernetes | Orchestration des conteneurs |
| Terraform | Infrastructure as Code |
| Ansible | Automatisation de la configuration |
| GitLab CI/CD | Intégration et automatisation du pipeline |
| Git / GitHub | Gestion et hébergement du code source |

## 📂 Structure du projet

```text
Absence-App/
│
├── app.py
├── requirements.txt
├── Dockerfile
├── absences.db
├── .gitignore
├── .gitlab-ci.yml
├── README.md
│
├── templates/
│   ├── ajouter.html
│   ├── base.html
│   ├── dashboard.html
│   ├── login.html
│   └── statistiques.html
│
├── ansible/
│   ├── inventory.ini
│   └── playbook.yml
│
├── kubernetes/
│   └── deployment.yaml
│
├── terraform/
│   ├── main.tf
│   ├── variables.tf
│   ├── outputs.tf
│   └── ...
│
├── rapport__Projet_devops.pdf
└── presentation_Projet_Devops.pptx
```

## ⚙️ Installation et exécution

### 1. Cloner le dépôt

```bash
git clone https://github.com/Outighli/Absence-App.git
cd Absence-App
```

### 2. Installer les dépendances

Créer un environnement virtuel :

```bash
python -m venv venv
```

Activer l'environnement sous Windows :

```bash
venv\Scripts\activate
```

Installer les dépendances :

```bash
pip install -r requirements.txt
```

### 3. Lancer l'application

```bash
python app.py
```

Accéder à l'application depuis le navigateur :

```text
http://localhost:5000
```

## 🐳 Conteneurisation avec Docker

Construire l'image Docker :

```bash
docker build -t absence-app .
```

Lancer le conteneur :

```bash
docker run -p 5000:5000 absence-app
```

L'application sera accessible à l'adresse :

```text
http://localhost:5000
```

## 🔄 Intégration continue et déploiement continu (CI/CD)

Le projet utilise **GitLab CI/CD**, configuré à travers le fichier `.gitlab-ci.yml`.

La pipeline permet d'automatiser les différentes étapes du cycle de vie de l'application, selon les jobs configurés :

- Construction de l'image Docker (Build).
- Exécution des tests (Test).
- Déploiement de l'application (Deploy), si configuré.

## ☸️ Orchestration avec Kubernetes

Le dossier `kubernetes/` contient les fichiers de configuration nécessaires au déploiement de l'application.

Kubernetes permet notamment de :

- Déployer l'application sous forme de Pods.
- Gérer les ressources de déploiement.
- Configurer les services.
- Faciliter la gestion et la scalabilité de l'application.

## 🏗️ Infrastructure as Code (IaC)

### Terraform

Terraform est utilisé pour automatiser le provisionnement de l'infrastructure à partir de fichiers de configuration déclaratifs.

### Ansible

Ansible permet d'automatiser la configuration et la gestion des serveurs à l'aide de playbooks.

## 📊 Livrables du projet

- Application web de gestion des absences.
- Configuration Docker.
- Pipeline CI/CD.
- Fichiers Kubernetes.
- Scripts Terraform.
- Playbooks Ansible.
- Rapport du projet (PDF).
- Présentation du projet (PowerPoint).

## 👩‍💻 Auteurs

**Layla Ouarrak**  
**Sanae Outighli**

## 🎓 Conclusion

Ce projet met en pratique les principes fondamentaux du DevOps en combinant développement logiciel, conteneurisation, automatisation et orchestration.

Il permet de comprendre comment intégrer les outils DevOps dans le cycle de vie d'une application afin de faciliter son déploiement et sa maintenance.
