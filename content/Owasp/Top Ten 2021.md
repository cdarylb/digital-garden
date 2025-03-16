## OWASP Top Ten 2020

Le OWASP Top Ten est une liste des dix principales vulnérabilités de sécurité des applications web identifiées par l'OWASP (Open Web Application Security Project). Voici la version 2020 :

### 1. [A01:2021] Broken Access Control
**(Contrôle d'accès insuffisant)**
- Mauvaise mise en œuvre des restrictions d'accès
- Accès non autorisé aux données ou aux fonctionnalités
- Exemple : Accès aux fichiers ou aux comptes d'autres utilisateurs

### 2. [A02:2021] Cryptographic Failures
**(Échecs cryptographiques, anciennement Exposition de données sensibles)**
- Mauvaise gestion des données sensibles
- Chiffrement faible ou inexistant
- Manque de confidentialité des communications

### 3. [A03:2021] Injection
- Inclusion de commandes non contrôlées (SQL, NoSQL, OS, etc.)
- Exploitation des entrées utilisateurs mal filtrées
- Exemple : Attaques SQLi, XSS, LDAP injection

### 4. [A04:2021] Insecure Design
**(Conception non sécurisée, nouvelle catégorie en 2021)**
- Mauvaise gestion des contrôles de sécurité dès la conception
- Manque d’analyses des risques et de validation des modèles de menace
- Défaut d’implémentation de principes comme le “Least Privilege”

### 5. [A05:2021] Security Misconfiguration
**(Mauvaise configuration de sécurité)**
- Paramètres par défaut laissés actifs
- Services et fonctionnalités inutiles exposés
- Exemples : pages d'erreur informatives, accès à des consoles d'administration non protégées

### 6. [A06:2021] Vulnerable and Outdated Components
**(Composants vulnérables et obsolètes)**
- Utilisation de bibliothèques, frameworks ou systèmes non à jour
- Dépendances avec des failles de sécurité connues
- Manque de suivi des mises à jour

### 7. [A07:2021] Identification and Authentication Failures
**(Échecs d'identification et d'authentification, anciennement Broken Authentication)**
- Mots de passe faibles, mal stockés ou récupérables
- Absence de MFA (authentification multifactorielle)
- Sessions non sécurisées

### 8. [A08:2021] Software and Data Integrity Failures
**(Défaillances de l'intégrité des logiciels et des données, nouvelle catégorie en 2021)**
- Manque de vérification d'intégrité des mises à jour et des dépendances
- Exemples : attaques par supply chain, injection de dépendances malveillantes

### 9. [A09:2021] Security Logging and Monitoring Failures
**(Défaillances des journaux de sécurité et de la surveillance, anciennement Insufficient Logging & Monitoring)**
- Logs de sécurité insuffisants ou inexistants
- Manque de surveillance active des incidents de sécurité
- Absence d’alerte sur les activités suspectes

### 10. [A10:2021] Server-Side Request Forgery (SSRF)
**(Falsification de requêtes côté serveur, nouvelle entrée en 2021)**
- Exploitation de services internes à travers des requêtes serveur non sécurisées
- Exemple : Un attaquant peut scanner un réseau interne via un service exposé


- [OWASP Official](https://owasp.org/www-project-top-ten/)
- [Rapport complet](https://owasp.org/www-pdf-archive/OWASP_Top_Ten_2021.pdf)