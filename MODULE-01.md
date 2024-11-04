### **Module 1 : Introduction à la Virtualisation**

#### **Objectifs pédagogiques :**
1. Comprendre le concept de virtualisation et ses avantages dans un environnement informatique.
2. Apprendre les différences entre les hyperviseurs de type 1 et de type 2.
3. Analyser les différentes couches d’une infrastructure virtualisée.
4. Expérimenter l’installation et la configuration d’un hyperviseur de type 2 (VMware Workstation) pour la création de machines virtuelles de test.

---

### **Contenu détaillé**

---

#### **1. Introduction au Concept de Virtualisation**

**Objectifs de la section :**
- Présenter le concept de virtualisation et ses applications.
- Expliquer pourquoi la virtualisation est une technologie centrale dans l'informatique moderne.

**Théorie :**
- **Définition de la Virtualisation :**  
   La virtualisation est une technique permettant de diviser les ressources physiques d'un ordinateur pour créer plusieurs systèmes indépendants appelés machines virtuelles. Elle sépare le matériel physique et le système d'exploitation.
  
- **Les avantages de la Virtualisation :**
   - **Optimisation des ressources :** Utilise pleinement la puissance des serveurs, souvent sous-utilisés.
   - **Isolation des environnements :** Chaque VM est indépendante, ce qui permet des environnements de développement, de test, et de production distincts.
   - **Mobilité et flexibilité :** Facilite le déplacement des applications et des services.
   - **Haute disponibilité et reprise après sinistre :** Les VM peuvent être sauvegardées, déplacées et restaurées rapidement.

**Exercice d’introduction :**
- **Questionnaire de réflexion :** Les participants notent leurs expériences ou connaissances en matière de virtualisation et les raisons pour lesquelles ils pensent qu’elle est essentielle aujourd’hui. Cela les aide à établir un contexte pour la suite du module.

---

#### **2. Les Types d'Hyperviseurs : Type 1 et Type 2**

**Objectifs de la section :**
- Distinguer les hyperviseurs de type 1 et de type 2.
- Comprendre les avantages et les inconvénients de chaque type.

**Théorie :**
- **Type 1 (Hyperviseur Bare-Metal) :**
   - Un hyperviseur de type 1 est installé directement sur le matériel, sans nécessiter de système d'exploitation intermédiaire.
   - **Exemples :** VMware ESXi, Microsoft Hyper-V, XenServer.
   - **Avantages :** Performances élevées, faible latence, idéal pour les environnements de production.
   - **Inconvénients :** Nécessite un matériel dédié, demande des compétences en administration de systèmes.

- **Type 2 (Hyperviseur Hébergé) :**
   - Un hyperviseur de type 2 fonctionne sur un système d’exploitation hôte (Windows, Linux, macOS).
   - **Exemples :** VMware Workstation, VirtualBox, Parallels Desktop.
   - **Avantages :** Facile à installer et à utiliser pour les tests et le développement.
   - **Inconvénients :** Moins performant que le type 1, dépend des ressources de l’OS hôte.

**Démonstration :**
- **Démonstration d’installation d’un hyperviseur de type 2 (VirtualBox ou VMware Workstation)** : Présentation des étapes d’installation pour initier les participants à l’interface et aux paramètres de base.

---

#### **3. Compréhension des Différentes Couches de Virtualisation et de Leur Fonctionnement**

**Objectifs de la section :**
- Explorer les couches composant une infrastructure virtualisée.
- Expliquer comment chaque couche fonctionne et contribue à la création d’un environnement virtualisé.

**Théorie :**
- **Couche matérielle (Hardware Layer) :** Fournit les ressources physiques, comme le processeur, la mémoire, le stockage et le réseau.
- **Hyperviseur (Virtual Machine Monitor) :** Interagit directement avec le matériel pour gérer les ressources allouées aux VM.
- **Couche de machines virtuelles :** Contient les VM, chacune ayant son propre OS et applications, isolée des autres VM.
- **Couche d'administration et de gestion :** Outils comme vCenter (pour VMware) qui permettent de gérer plusieurs hyperviseurs et VM, d’automatiser les tâches et de surveiller l’infrastructure.

**Exercice :**
- **Illustration des couches :** Les participants créent un schéma détaillant chaque couche de virtualisation et son rôle, en utilisant un cas concret (ex. : un serveur utilisé pour héberger plusieurs VM). Cela les aide à visualiser l’infrastructure.

---

#### **4. Installation d’un Hyperviseur de Type 2**

**Objectifs de la section :**
- Acquérir des compétences pratiques dans l'installation et la configuration d’un hyperviseur de type 2.

**Pratique :**
- **Étapes d'installation de VMware Workstation (ou VirtualBox) :**
   1. Télécharger le logiciel sur le site officiel.
   2. Suivre les étapes de l’installation, configurer les paramètres de base (emplacement d'installation, options de démarrage).
   3. Configurer les préférences (par exemple, allouer de la mémoire et du CPU).
   4. Redémarrer l’ordinateur si nécessaire pour finaliser l’installation.

- **Configuration initiale :**
   - Créer un dossier pour stocker les fichiers des machines virtuelles.
   - Définir les préférences par défaut pour les nouvelles VM (comme l’espace disque et le type de réseau).

---

#### **5. Création et Gestion de Machines Virtuelles**

**Objectifs de la section :**
- Comprendre comment créer et gérer des machines virtuelles dans un hyperviseur de type 2.

**Pratique :**
- **Création d’une VM :**
   1. Dans VMware Workstation, sélectionner "Créer une nouvelle machine virtuelle".
   2. Choisir les options de configuration (installation personnalisée ou recommandée).
   3. Sélectionner un fichier ISO pour l’installation de l’OS ou connecter un CD/DVD.
   4. Configurer les paramètres matériels de la VM (mémoire, processeur, disque dur virtuel).
   5. Démarrer la VM et suivre l’installation de l’OS.

- **Gestion des VM :**
   - **Prendre un Snapshot :** Explication de l’utilité des snapshots pour les tests et les sauvegardes.
   - **Suspendre, Redémarrer, Éteindre une VM :** Utiliser les commandes de gestion de l’alimentation.
   - **Configurer les paramètres réseau** : Choisir entre NAT, Bridge et Host-Only pour les configurations réseau.

**Exercice :**
- **Création de VMs de test** : Les participants créent une ou deux machines virtuelles, installent un système d’exploitation léger (Linux par exemple), et configurent un réseau entre les VM et l’hôte.

---

#### **6. Exercice Pratique et Questions-Réponses**

**Objectifs de la section :**
- Permettre aux participants de renforcer leurs connaissances en réalisant des exercices pratiques.
- Clarifier les points non compris grâce à une session de questions-réponses.

**Exercice pratique final :**
- **Mise en situation :**  
   Les participants simulent un environnement de développement où ils doivent :
   1. Créer deux machines virtuelles avec des configurations spécifiques.
   2. Installer un OS sur chaque VM.
   3. Configurer le réseau pour que les deux VM puissent communiquer entre elles.
   4. Prendre un snapshot de chaque VM après l’installation de l’OS.

**Questions-Réponses :**
- Cette session permet de clarifier les points encore flous, de discuter des cas d’utilisation concrets dans les environnements de production, et de partager les expériences des participants.

---

### **Conclusion et Bilan de la Journée**

- **Révision des concepts principaux :**
