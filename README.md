# Doranco-projet-windows-server-2022

### Projet Windows Server 2022 : Gestion d'un Domaine d'Entreprise  
**Niveau :** Intermédiaire à Avancé  
**Objectif pédagogique :**  
Apprendre à configurer un environnement réseau sous **Windows Server 2022**, incluant la gestion d'un **contrôleur de domaine (Active Directory)**, des rôles réseau (DNS, DHCP), et des stratégies de groupe (GPO).  

---

### **Énoncé du Projet :**  

Vous êtes un administrateur système chargé de configurer l'infrastructure réseau d'une entreprise fictive appelée **TechCorp**. L'objectif est de mettre en place un domaine fonctionnel avec les rôles réseau nécessaires et une gestion fine des utilisateurs et des permissions.

---

#### **1. Prérequis techniques :**
- Une machine physique ou virtuelle avec Windows Server 2022.
- Une ou plusieurs machines clientes avec Windows 10/11 (virtuelles ou physiques).
- Un logiciel de virtualisation comme **VMware Workstation** ou **VirtualBox** (si nécessaire).
- Un réseau local simulé.

---

#### **2. Étapes à réaliser :**

##### **Partie 1 : Installation et configuration initiale**
1. **Installation de Windows Server 2022** :  
   Installez et configurez une machine Windows Server 2022. Attribuez-lui une IP fixe (exemple : 192.168.1.10).
   
2. **Nom de la machine** :  
   Renommez la machine en **SRV-DC01**.

##### **Partie 2 : Mise en place d'un contrôleur de domaine (AD DS)**  
1. Installez le rôle **Active Directory Domain Services (AD DS)**.  
2. Créez un nouveau domaine nommé : `techcorp.local`.  
3. Configurez **DNS** pour résoudre les noms du domaine.  

##### **Partie 3 : Gestion des utilisateurs et groupes**
1. Créez les **utilisateurs suivants** dans Active Directory :  
   - `admin-tech` : Administrateur du domaine.  
   - `user-john` : Employé du département IT.  
   - `user-sarah` : Employée du département RH.  
   
2. Créez les **groupes suivants** :  
   - `IT-Dept`  
   - `HR-Dept`  

3. Ajoutez `user-john` dans le groupe `IT-Dept` et `user-sarah` dans le groupe `HR-Dept`.

##### **Partie 4 : Gestion des stratégies de groupe (GPO)**  
1. Configurez une **GPO** pour appliquer un fond d’écran personnalisé sur tous les ordinateurs des utilisateurs.  
2. Configurez une **GPO** pour bloquer l'accès au **Panneau de configuration** pour les utilisateurs du groupe `HR-Dept`.

##### **Partie 5 : Configuration DHCP et DNS**
1. Configurez un serveur DHCP sur la machine Windows Server 2022 avec :  
   - Une plage d'adresses : `192.168.1.100` à `192.168.1.200`.  
   - Une passerelle par défaut : `192.168.1.1`.  
   - Une attribution DNS pointant vers `192.168.1.10`.

2. Testez le fonctionnement DHCP avec une machine cliente.

##### **Partie 6 : Test et documentation**  
1. Connectez une machine cliente au domaine `techcorp.local`.  
2. Vérifiez que les GPO s'appliquent correctement.  
3. Rédigez une documentation technique (une page minimum) expliquant les étapes suivies pour chaque partie.

---

#### **Critères de notation (sur 20 points) :**

1. **Installation et configuration initiale (4 points)**  
   - Configuration IP et nom de la machine.  
   - Installation du rôle AD DS.  

2. **Création du domaine et gestion des utilisateurs (4 points)**  
   - Domaine créé correctement.  
   - Utilisateurs et groupes ajoutés avec précision.  

3. **Configuration des GPO (4 points)**  
   - Application correcte des stratégies.  
   - Vérification sur les machines clientes.

4. **Mise en place DHCP et DNS (4 points)**  
   - Serveur DHCP fonctionnel avec plage d’adresses valide.  
   - Résolution DNS correcte.

5. **Tests et documentation (4 points)**  
   - Documentation claire et précise des étapes.  
   - Résultats des tests validés sur les machines clientes.

---

### **Bonus (2 points supplémentaires)**  
- Si les étudiants ajoutent des fonctionnalités supplémentaires, comme un serveur de fichiers ou une gestion fine des permissions sur des dossiers partagés.

