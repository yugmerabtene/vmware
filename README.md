### Module 1. Introduction à la Virtualisation

**Objectif :** Comprendre les concepts de base de la virtualisation et les différences entre les types d’hyperviseurs.

**Contenu :**

- **Concept de la Virtualisation**  
   La virtualisation est une technique permettant de créer plusieurs machines virtuelles (VM) sur un même matériel physique. Cela optimise l'utilisation des ressources et facilite la gestion informatique.

- **Types de Virtualisation :**
   - **Type 1 (Hyperviseur Bare-Metal)** : Exemple avec VMware ESXi. Installation directe sur le matériel, utilisée dans les environnements de production.
   - **Type 2 (Hyperviseur Hébergé)** : Exemple avec VMware Workstation. Installation sur un système d'exploitation hôte, souvent utilisée pour le développement et les tests.

**Procédure Pratique :**  
- **Installation de VMware Workstation (Type 2) :**
   1. Télécharger VMware Workstation.
   2. Lancer l’installation en suivant les instructions, puis créer une VM de test pour se familiariser avec l’interface.
- **Préparation de l'installation d'ESXi (Type 1) :**
   1. Préparer un serveur physique et un support de démarrage (clé USB, CD).
   2. Configurer le BIOS pour démarrer sur le support d’installation.

---

### Module 2. Installation et Configuration d'un Serveur ESXi

**Objectif :** Installer ESXi sur un serveur physique et configurer les paramètres de base pour le démarrage d’un environnement de virtualisation.

**Contenu :**

- **Installation d’ESXi :**
   - Préparer le support d'installation (clé USB ou CD avec l'image ESXi).
   - Insérer le support dans le serveur, démarrer et suivre l'installation pas à pas.

- **Configuration Initiale Post-Installation :**
   1. Accéder à l'interface de configuration d'ESXi via le DCUI (Direct Console User Interface).
   2. Configurer les paramètres réseau (adresse IP, masque de sous-réseau, passerelle).
   3. Paramétrer les accès administratifs.

**Procédure Pratique :**
   - **Démarrage de l’installation d’ESXi** : Assurez-vous d’avoir les paramètres réseau du serveur. 
   - **Accès et configuration via vSphere Client** :
      1. Depuis un PC connecté au même réseau, ouvrir vSphere Client.
      2. Connectez-vous à l’hôte ESXi pour configurer les options supplémentaires.

---

### Module 3. Gestion du Stockage Partagé (vSAN)

**Objectif :** Configurer vSAN pour centraliser et optimiser le stockage, permettant la création d’un pool de stockage partagé à partir des disques des hôtes ESXi.

**Contenu :**

- **Configuration de vSAN :**
   - Créer un cluster vSAN dans vCenter.
   - Ajouter les hôtes ESXi au cluster et activer vSAN pour utiliser le stockage local comme stockage partagé.

- **Fonctionnalités vSAN :**
   - **Redondance et Tolérance aux pannes** : Configurer des politiques de redondance pour les VM (réplication de données pour éviter la perte).
   - **Surveillance de la santé** : Utiliser les outils de vCenter pour surveiller l’état de santé de vSAN.

**Procédure Pratique :**
   - **Création du cluster vSAN** :
      1. Dans vCenter, créer un nouveau cluster.
      2. Activer vSAN dans les paramètres du cluster, choisir une politique de redondance.
      3. Surveiller l’état du cluster avec les outils de diagnostic intégrés.

---

### Module 4. Administration Centralisée avec vCenter

**Objectif :** Utiliser vCenter pour centraliser l’administration des hôtes ESXi et des machines virtuelles.

**Contenu :**

- **Installation et Configuration de vCenter :**
   - Télécharger vCenter Appliance (VCSA) et l’installer sur un hôte ESXi.
   - Configurer l’accès à vCenter, créer des datacenters et des clusters.

- **Fonctionnalités Clés de vCenter :**
   - **Gestion des utilisateurs et rôles** : Créer des comptes utilisateurs, définir les permissions et rôles.
   - **Automatisation des tâches** : Automatiser des tâches récurrentes comme les snapshots ou la surveillance.

**Procédure Pratique :**
   - **Installation de vCenter** :
      1. Depuis vSphere Client, déployer le fichier OVA de vCenter sur un hôte ESXi.
      2. Configurer l’IP et les paramètres d’administration.
   - **Ajout d’un hôte ESXi à vCenter** :
      1. Ouvrir l’interface de vCenter.
      2. Ajouter un hôte ESXi en entrant son adresse IP et les informations de connexion.

---

### Module 5. Migration de Machines Virtuelles à Chaud (vMotion)

**Objectif :** Maîtriser la migration à chaud des VM sans interruption de service pour garantir la flexibilité opérationnelle.

**Contenu :**

- **Configuration de vMotion :**
   - Configurer des réseaux dédiés à vMotion pour optimiser la vitesse de migration.
   - Paramétrer les options de compatibilité pour garantir que les VM peuvent être déplacées entre les hôtes.

- **Mise en Pratique de vMotion :**
   - Initiation de la migration d’une VM en utilisant vMotion pour tester la continuité de service.

**Procédure Pratique :**
   - **Configuration d’un réseau vMotion** :
      1. Créer un nouveau commutateur virtuel dans vCenter.
      2. Assigner ce commutateur aux opérations vMotion pour éviter la congestion du réseau principal.

---

### Module 6. Mise en Cluster d'Hyperviseurs

**Objectif :** Créer et configurer des clusters d’hyperviseurs pour faciliter la gestion et optimiser l’utilisation des ressources.

**Contenu :**

- **Configuration d’un Cluster** :
   - Créer un cluster dans vCenter, ajouter des hôtes ESXi, configurer les ressources partagées.

- **Fonctionnalités du Cluster :**
   - **Tolérance aux pannes et redondance** : Configurer des paramètres pour assurer la redondance et tolérance aux pannes.

**Procédure Pratique :**
   - **Création d’un Cluster** :
      1. Dans vCenter, accéder à l’onglet "Clusters".
      2. Créer un cluster, ajouter des hôtes, et configurer les options de tolérance aux pannes.

---

### Module 7. Mise en Place du High Availability (HA)

**Objectif :** Configurer le HA pour minimiser les temps d’arrêt en cas de panne matérielle.

**Contenu :**

- **Activation de HA** :
   - Activer le HA dans un cluster pour assurer le redémarrage automatique des VM en cas de panne d’un hôte.

- **Configuration des Options de HA :**
   - Définir les seuils et niveaux de tolérance pour maximiser la disponibilité.

**Procédure Pratique :**
   - **Activation de HA** :
      1. Dans les paramètres du cluster, activer l’option HA.
      2. Configurer les priorités de redémarrage des VM pour assurer une reprise rapide.

---

### Module 8. Mise en Place du Distributed Resource Scheduler (DRS)

**Objectif :** Optimiser l’utilisation des ressources avec DRS pour équilibrer les charges de travail.

**Contenu :**

- **Configuration de DRS** :
   - Activer DRS dans un cluster, définir les seuils de répartition des charges.

- **Politiques de DRS** :
   - Définir des politiques pour prioriser les performances ou la consommation de ressources.

**Procédure Pratique :**
   - **Activation de DRS** :
      1. Accéder aux paramètres du cluster, activer DRS.
      2. Configurer les seuils de sensibilisation pour équilibrer les charges.

---

### Module 9. Audit et Supervision des Serveurs ESXi

**Objectif :** Superviser les performances et auditer la sécurité des hôtes ESXi.

**Contenu :**

- **Surveillance des Performances** :
   - Utiliser les outils de vCenter pour analyser l’utilisation des ressources (CPU, mémoire, stockage).

- **Audit de la Sécurité** :
   - Configurer des alertes pour identifier les anomalies et garantir la sécurité.

**Procédure Pratique :**
   - **Utilisation des Outils de Supervision** :
      1. Accéder aux tableaux de bord de performance dans vCenter.
      2. Analyser les rapports et ajuster les ressources en fonction des besoins.

---

