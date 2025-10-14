# Politique de Sécurité

[🇬🇧 English version](SECURITY.md)

## 🔒 Signaler une Vulnérabilité

L'équipe AbsyssLab prend les bugs de sécurité au sérieux. Nous apprécions vos
efforts pour divulguer vos découvertes de manière responsable, et nous ferons
tout notre possible pour reconnaître vos contributions.

### Comment Signaler

**⚠️ Veuillez NE PAS signaler les vulnérabilités de sécurité via les issues GitHub publiques.**

Au lieu de cela, veuillez signaler les vulnérabilités de sécurité par :

1. **Ouvrir un Avis de Sécurité** (préféré)
   - Allez dans l'onglet Security du dépôt
   - Cliquez sur "Report a vulnerability"
   - Remplissez les détails

2. **Envoyer un email**
   - Envoyez un email aux mainteneurs avec les détails
   - Utilisez l'objet : `[SECURITY] Brève description`

3. **Issue privée**
   - Contactez un mainteneur pour créer une issue privée

### Que Inclure

Pour nous aider à mieux comprendre et résoudre le problème, veuillez inclure :

- **Type de vulnérabilité** (ex: injection SQL, XSS, contournement d'authentification)
- **Chemin complet** du ou des fichiers source concernés
- **Emplacement** du code source affecté (tag/branche/commit ou URL directe)
- **Instructions étape par étape** pour reproduire le problème
- **Preuve de concept ou code d'exploitation** (si possible)
- **Impact** de la vulnérabilité
- **Votre évaluation** de la gravité
- **Mitigation proposée** (si vous avez des suggestions)

### À Quoi S'Attendre

- **Réponse initiale** - Sous 48 heures
- **Évaluation** - Nous évaluerons la gravité et l'impact
- **Développement du correctif** - Nous travaillerons sur un correctif et vous tiendrons informé
- **Divulgation** - Divulgation coordonnée après publication du correctif
- **Crédit** - Les avis de sécurité créditeront le rapporteur (sauf demande d'anonymat)

## 🛡️ Politique de Mise à Jour de Sécurité

### Versions Supportées

Nous fournissons des mises à jour de sécurité pour les versions suivantes :

| Version | Supportée          |
| ------- | ------------------ |
| Dernière| ✅ Oui             |
| < Dernière| ⚠️ Meilleur effort |

Nous recommandons fortement d'utiliser toujours la dernière version de nos connecteurs.

### Mises à Jour de Sécurité

- Les correctifs de sécurité sont publiés dès que possible après confirmation d'une vulnérabilité
- Les mises à jour sont annoncées via :
  - GitHub Security Advisories
  - Releases du dépôt
  - GitHub Discussions (si critique)

## 🔐 Bonnes Pratiques de Sécurité

Lors de l'utilisation des connecteurs VTOM d'AbsyssLab, suivez ces bonnes pratiques de sécurité :

### 1. Gestion des Identifiants

**❌ À NE PAS FAIRE :**
- Hard-coder les identifiants dans les scripts
- Stocker les mots de passe en clair
- Commiter les identifiants dans le contrôle de version
- Partager les identifiants dans les logs ou issues

**✅ À FAIRE :**
- Utiliser des variables d'environnement
- Utiliser des systèmes de gestion de secrets (HashiCorp Vault, Azure Key Vault, AWS Secrets Manager)
- Utiliser la gestion intégrée des credentials de VTOM
- Faire tourner les identifiants régulièrement
- Utiliser des comptes de service avec les permissions minimales requises

### 2. Sécurité Réseau

**Recommandations :**
- Utiliser TLS/SSL pour toutes les communications API
- Implémenter la segmentation réseau
- Utiliser des pare-feu pour restreindre l'accès
- Activer la limitation de débit API quand disponible
- Utiliser des réseaux privés pour les opérations sensibles

### 3. Contrôle d'Accès

**Recommandations :**
- Appliquer le principe du moindre privilège
- Utiliser le contrôle d'accès basé sur les rôles (RBAC)
- Auditer régulièrement les permissions utilisateur
- Supprimer les comptes inutilisés
- Activer l'authentification multi-facteurs (MFA) où supporté

### 4. Journalisation et Surveillance

**Recommandations :**
- Activer la journalisation d'audit
- Surveiller les activités suspectes
- Masquer les données sensibles dans les logs
- Examiner régulièrement les logs
- Configurer des alertes pour les événements de sécurité

### 5. Mises à Jour et Correctifs

**Recommandations :**
- Maintenir les connecteurs à jour
- S'abonner aux avis de sécurité
- Tester les mises à jour dans des environnements hors production d'abord
- Avoir un plan de rollback
- Documenter vos procédures de mise à jour

## 🚨 Considérations de Sécurité Connues

### Clés API et Tokens

De nombreux connecteurs nécessitent des clés API ou tokens. Toujours :
- Les stocker en toute sécurité
- Ne jamais les exposer dans le code ou les logs
- Utiliser des variables d'environnement ou gestionnaires de secrets
- Les faire tourner périodiquement
- Révoquer les tokens inutilisés

### Conteneurs Docker

Si vous utilisez des connecteurs conteneurisés :
- Utiliser des images de base officielles
- Maintenir les images de base à jour
- Scanner les images pour les vulnérabilités
- Ne pas exécuter les conteneurs en root
- Utiliser des systèmes de fichiers en lecture seule quand possible

### Dépendances Externes

- Mettre à jour régulièrement les dépendances Python
- Utiliser `pip-audit` ou `safety` pour vérifier les vulnérabilités connues
- Épingler les versions de dépendances en production
- Examiner les licences et historiques de sécurité des dépendances

## 📋 Checklist de Sécurité

Avant de déployer un connecteur en production :

- [ ] Identifiants stockés en toute sécurité (pas en dur)
- [ ] TLS/SSL activé pour les communications API
- [ ] Permissions minimales requises configurées
- [ ] Journalisation d'audit activée
- [ ] Données sensibles masquées dans les logs
- [ ] Dernière version du connecteur installée
- [ ] Dépendances à jour et scannées
- [ ] Accès réseau restreint de manière appropriée
- [ ] Surveillance et alertes configurées
- [ ] Plan de réponse aux incidents documenté
- [ ] Procédures de sauvegarde et récupération testées

## 🔍 Calendrier de Divulgation des Vulnérabilités

1. **Jour 0** - Vulnérabilité signalée
2. **Jour 1-2** - Réponse initiale et accusé de réception
3. **Jour 3-7** - Vulnérabilité évaluée et gravité déterminée
4. **Jour 7-30** - Correctif développé et testé
5. **Jour 30** - Correctif publié (peut être plus tôt pour les problèmes critiques)
6. **Jour 30+** - Divulgation publique dans l'avis de sécurité

Pour les vulnérabilités critiques, nous visons un calendrier plus rapide.

## 📞 Contact

Pour les questions liées à la sécurité qui ne sont pas des vulnérabilités :
- Ouvrez une discussion dans le dépôt
- Étiquetez-la avec le label `security`

Pour les questions générales sur la sécurité :
- Consultez notre [Guide de Support](SUPPORT.fr.md)

## 🏆 Hall of Fame

Nous reconnaissons les chercheurs en sécurité qui nous aident à garder nos projets sécurisés :

<!-- Les chercheurs en sécurité seront listés ici après divulgation responsable -->

*Soyez le premier à nous aider à améliorer notre sécurité !*

---

**Merci d'aider à garder les connecteurs VTOM d'AbsyssLab sécurisés ! 🙏**

