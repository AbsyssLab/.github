# Support

[🇬🇧 English version](SUPPORT.md)

Bienvenue sur le support des connecteurs VTOM d'Absyss ! 👋

Ce document vous aidera à trouver l'assistance dont vous avez besoin.

## 📚 Documentation

Avant d'ouvrir une issue, veuillez consulter la documentation disponible :

### Documentation Spécifique aux Connecteurs

Chaque connecteur possède son propre README avec :
- Instructions d'installation
- Guide de configuration
- Exemples d'utilisation
- Section de dépannage
- Référence API

### Ressources Générales

- [Guide de Contribution](CONTRIBUTING.fr.md) - Comment contribuer
- [Code de Conduite](CODE_OF_CONDUCT.fr.md) - Directives communautaires
- [Politique de Sécurité](SECURITY.fr.md) - Comment signaler les problèmes de sécurité

## 🆘 Obtenir de l'Aide

### 1. Rechercher les Issues Existantes

Avant de créer une nouvelle issue, veuillez rechercher :
- [Issues de l'organisation](https://github.com/search?q=org%3AAbsyssLab+type%3Aissue)
- Issues du dépôt spécifique
- Issues fermées (votre question peut déjà avoir une réponse)

### 2. GitHub Discussions 💬

Pour les questions, idées et interactions communautaires :
- [Discussions de l'organisation](https://github.com/orgs/AbsyssLab/discussions)

**Bon pour :**
- Questions générales
- Bonnes pratiques
- Discussions de cas d'usage
- Brainstorming de fonctionnalités
- Aide communautaire

### 3. Créer une Issue 🐛

Utilisez le template approprié :

- **[Rapport de Bug](https://github.com/AbsyssLab/.github/issues/new?template=bug_report.yml)**
  - Quelque chose ne fonctionne pas
  - Comportement inattendu
  - Messages d'erreur

- **[Demande de Fonctionnalité](https://github.com/AbsyssLab/.github/issues/new?template=feature_request.yml)**
  - Nouvelle fonctionnalité
  - Amélioration d'une fonctionnalité existante
  - Amélioration de performance

- **[Demande de Connecteur](https://github.com/AbsyssLab/.github/issues/new?template=connector_request.yml)**
  - Proposer un nouveau connecteur
  - Intégration avec un nouvel outil/plateforme

## 🔍 Dépannage

### Problèmes Courants

#### Erreurs de Connexion

**Symptômes :** Impossible de se connecter à l'API/service cible

**Solutions :**
1. Vérifier que les identifiants sont corrects
2. Vérifier la connectivité réseau
3. Vérifier les règles de pare-feu
4. S'assurer que le service cible est accessible
5. Vérifier les exigences de proxy
6. Examiner les URLs des endpoints API

#### Échecs d'Authentification

**Symptômes :** Erreurs 401/403, messages "Unauthorized"

**Solutions :**
1. Vérifier que les clés API/tokens sont valides
2. Vérifier l'expiration des tokens
3. S'assurer que les permissions appropriées sont accordées
4. Vérifier la configuration du compte de service
5. Vérifier les exigences MFA

#### Échecs d'Exécution de Job

**Symptômes :** Les jobs échouent avec des codes d'erreur

**Solutions :**
1. Vérifier les logs VTOM (stdout/stderr)
2. Vérifier les paramètres du job
3. S'assurer que toutes les dépendances sont installées
4. Vérifier la compatibilité de la version Python
5. Vérifier les variables d'environnement
6. Examiner la disponibilité des ressources (espace disque, mémoire)

#### Problèmes de Performance

**Symptômes :** Exécution lente, timeouts

**Solutions :**
1. Vérifier la latence réseau
2. Examiner les limites de débit API
3. Optimiser les paramètres de requête
4. Augmenter les valeurs de timeout
5. Considérer les opérations par batch
6. Surveiller les ressources système

### Mode Debug

La plupart des connecteurs supportent le mode debug pour une journalisation détaillée :

```bash
# Définir la variable d'environnement de debug
export DEBUG=1
export VTOM_LOG_LEVEL=DEBUG

# Exécuter avec sortie verbeuse
python connector.py --debug
```

### Analyse des Logs

Lors du signalement de problèmes, incluez :
- Messages d'erreur complets
- Stack traces
- Extraits de logs pertinents (avec données sensibles retirées)
- Sortie du job VTOM
- Version du connecteur
- Détails de l'environnement

## 📋 Informations à Fournir

Lorsque vous demandez de l'aide, veuillez inclure :

### Environnement
- Version Visual TOM
- Version du connecteur
- Version Python
- Système d'exploitation
- Version du service/API cible

### Configuration
- Configuration pertinente (retirer les données sensibles)
- Variables d'environnement utilisées
- Définition du job (si applicable)

### Détails de l'Erreur
- Message d'erreur complet
- Stack trace
- Étapes pour reproduire
- Comportement attendu vs réel
- Logs (nettoyés)

### Format d'Exemple

```markdown
**Environnement :**
- VTOM : 6.4.0
- Connecteur : vtom-azure-data-factory v1.2.0
- Python : 3.10.5
- OS : Ubuntu 20.04
- Azure Data Factory : V2

**Problème :**
Le job échoue lors du déclenchement du pipeline avec paramètres

**Erreur :**
```
Error: Pipeline trigger failed
Status code: 400
Message: Invalid parameter format
```

**Étapes pour Reproduire :**
1. Configurer le job avec les paramètres : {...}
2. Exécuter le job depuis VTOM
3. L'erreur se produit

**Attendu :** Le pipeline devrait se déclencher avec succès
**Réel :** Erreur 400 retournée
```

## 🚀 Guides de Démarrage Rapide

### Installation

```bash
# Cloner le connecteur
git clone https://github.com/AbsyssLab/<nom-connecteur>.git

# Installer les dépendances
pip install -r requirements.txt

# Configurer
cp config.example.yaml config.yaml
# Éditer config.yaml avec vos paramètres

# Tester
python connector.py --test
```

### Configuration de Base

La plupart des connecteurs nécessitent :
1. **Identifiants API** - Token, clé, ou username/password
2. **URL Endpoint** - URL du service cible
3. **Paramètres de connexion** - Timeout, retry, etc.
4. **Intégration VTOM** - Définition du job, paramètres

### Intégration avec VTOM

1. **Copier le connecteur** dans le répertoire des scripts VTOM
2. **Créer le job** dans l'application VTOM
3. **Configurer les paramètres** comme variables de job
4. **Définir les variables** d'environnement pour les identifiants
5. **Tester l'exécution** manuellement d'abord
6. **Planifier le job** une fois fonctionnel

## 📞 Options de Contact

### Support Communautaire (Gratuit)

- GitHub Discussions - Questions et aide communautaire
- GitHub Issues - Rapports de bugs et demandes de fonctionnalités
- Documentation publique - README, guides

**Temps de réponse :** Meilleur effort, piloté par la communauté

### Support Professionnel

Pour les organisations nécessitant :
- Support avec SLA
- Corrections de bugs prioritaires
- Développement personnalisé
- Formation et consulting
- Support technique direct

Veuillez contacter les mainteneurs via GitHub.

## ⏰ Temps de Réponse

**Support Communautaire :**
- Questions : Généralement sous 2-5 jours
- Rapports de bugs : Accusé de réception sous 1 semaine
- Demandes de fonctionnalités : Examinées mensuellement

**Problèmes Critiques :**
- Vulnérabilités de sécurité : Sous 48 heures
- Bugs critiques : Priorisés selon l'impact

## 🌐 Support Linguistique

- **Anglais** - Langue principale pour toute la documentation et les issues
- **Français** - Traductions communautaires disponibles pour certains documents

Lors d'une demande d'aide dans d'autres langues que l'anglais, veuillez noter que
les temps de réponse peuvent être plus longs.

## 📖 Ressources d'Apprentissage

### Ressources Visual TOM
- [Site Officiel Absyss](https://www.absyss.com)
- Documentation Visual TOM
- Référence API VTOM

### Développement de Connecteurs
- [Bonnes Pratiques Python](https://docs.python-guide.org/)
- Guides d'Intégration API
- GitHub Actions CI/CD

### Contribution
- [Comment Contribuer](CONTRIBUTING.fr.md)
- [Code de Conduite](CODE_OF_CONDUCT.fr.md)
- Directives de Pull Request

## ✅ Checklist de Support

Avant de demander de l'aide :

- [ ] J'ai lu le README du connecteur
- [ ] J'ai recherché dans les issues existantes
- [ ] J'ai consulté le guide de dépannage
- [ ] J'ai vérifié ma configuration
- [ ] J'ai testé avec la journalisation de debug activée
- [ ] J'ai toutes les informations requises prêtes
- [ ] J'ai retiré les données sensibles des logs

## 🤝 Communauté

Rejoignez notre communauté :
- ⭐ Étoiler les dépôts que vous trouvez utiles
- 👀 Surveiller les dépôts pour les mises à jour
- 🍴 Forker et expérimenter
- 💬 Participer aux discussions
- 🐛 Signaler des bugs
- ✨ Suggérer des fonctionnalités
- 🔧 Contribuer du code

## 📜 Avertissement

Les connecteurs VTOM d'Absyss sont fournis "tels quels" sous licence Apache 2.0.
Bien que nous nous efforcions de fournir des logiciels et un support de qualité,
il n'y a aucune garantie. Voir la [LICENSE](LICENSE) pour les détails.

---

**Merci d'utiliser les connecteurs VTOM d'Absyss ! 🙏**

<div align="center">
  <sub>Des questions ? N'hésitez pas à demander dans les Discussions !</sub>
</div>

