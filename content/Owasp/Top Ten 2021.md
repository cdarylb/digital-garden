## OWASP Top Ten 2021

### 1. [A01:2021] Broken Access Control
**(Contrôle d'accès insuffisant)**
- Mauvaise gestion des permissions
- Accès non autorisé à des fichiers ou fonctionnalités
- Exploitation des failles pour contourner les restrictions d’accès

### 2. [A02:2021] Cryptographic Failures
**(Échecs cryptographiques, anciennement Exposition de données sensibles)**
- Mauvaise protection des données sensibles
- Utilisation de protocoles obsolètes ou non sécurisés
- Absence de chiffrement ou mauvaise mise en œuvre

### 3. [A03:2021] Injection
- Inclusion de commandes non contrôlées (SQL, NoSQL, OS, etc.)
- Exploitation des entrées utilisateur mal filtrées
- Exemples : Attaques SQLi, XSS, LDAP injection

### 4. [A04:2021] Insecure Design
**(Conception non sécurisée, nouvelle catégorie en 2021)**
- Défaut de mise en œuvre des principes de sécurité dès la conception
- Manque d'analyse des risques et d'évaluation des modèles de menace
- Faible protection des flux critiques

### 5. [A05:2021] Security Misconfiguration
**(Mauvaise configuration de sécurité)**
- Paramètres par défaut non modifiés
- Services et fonctionnalités inutiles exposés
- Mauvaise gestion des en-têtes HTTP de sécurité

### 6. [A06:2021] Vulnerable and Outdated Components
**(Composants vulnérables et obsolètes)**
- Utilisation de bibliothèques, frameworks ou systèmes non mis à jour
- Dépendances avec des vulnérabilités connues
- Manque de suivi des versions et correctifs de sécurité

### 7. [A07:2021] Identification and Authentication Failures
**(Échecs d'identification et d'authentification, anciennement Broken Authentication)**
- Mots de passe faibles ou mal stockés
- Absence d’authentification multifactorielle (MFA)
- Sessions non sécurisées ou mal gérées

### 8. [A08:2021] Software and Data Integrity Failures
**(Défaillances de l'intégrité des logiciels et des données, nouvelle catégorie en 2021)**
- Manque de vérification de l'intégrité des mises à jour et des dépendances
- Attaques par supply chain
- Déploiement de packages non signés

### 9. [A09:2021] Security Logging and Monitoring Failures
**(Défaillances des journaux de sécurité et de la surveillance, anciennement Insufficient Logging & Monitoring)**
- Logs de sécurité insuffisants ou absents
- Surveillance et détection des menaces inefficaces
- Manque d’alerte en cas d’activité suspecte

### 10. [A10:2021] Server-Side Request Forgery (SSRF)
**(Falsification de requêtes côté serveur, nouvelle entrée en 2021)**
- Exploitation des services internes via des requêtes serveur non sécurisées
- Scanner un réseau interne via un service exposé
- Contourner les restrictions de pare-feu

### Références
- [OWASP Official](https://owasp.org/www-project-top-ten/)
- [Rapport complet](https://owasp.org/www-pdf-archive/OWASP_Top_Ten_2021.pdf)
