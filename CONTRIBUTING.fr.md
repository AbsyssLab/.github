# Contribuer aux connecteurs VTOM d'AbsyssLab

[🇬🇧 English version](CONTRIBUTING.md)

Merci d'envisager de contribuer aux connecteurs VTOM d'AbsyssLab ! 🎉

Nous accueillons les contributions de la communauté et sommes ravis de vous compter parmi nous.

## 📋 Table des matières

- [Code de conduite](#code-de-conduite)
- [Comment puis-je contribuer ?](#comment-puis-je-contribuer)
- [Configuration du développement](#configuration-du-développement)
- [Standards de code](#standards-de-code)
- [Directives de commit](#directives-de-commit)
- [Processus de Pull Request](#processus-de-pull-request)
- [Tests](#tests)
- [Documentation](#documentation)

## 📜 Code de conduite

Ce projet et tous ceux qui y participent sont régis par notre [Code de conduite](CODE_OF_CONDUCT.fr.md). En participant, vous vous engagez à respecter ce code.

## 🤝 Comment puis-je contribuer ?

### Signaler des bugs 🐛

- Utilisez le [template de rapport de bug](https://github.com/AbsyssLab/.github/issues/new?template=bug_report.yml)
- Vérifiez si le bug n'a pas déjà été signalé
- Incluez les étapes détaillées pour reproduire
- Fournissez les logs et messages d'erreur
- Précisez votre environnement (version VTOM, OS, etc.)

### Suggérer des fonctionnalités ✨

- Utilisez le [template de demande de fonctionnalité](https://github.com/AbsyssLab/.github/issues/new?template=feature_request.yml)
- Décrivez clairement la fonctionnalité et ses bénéfices
- Fournissez des cas d'usage et exemples
- Expliquez pourquoi cette fonctionnalité serait utile pour la majorité des utilisateurs

### Proposer de nouveaux connecteurs 🔌

- Utilisez le [template de demande de connecteur](https://github.com/AbsyssLab/.github/issues/new?template=connector_request.yml)
- Décrivez l'outil/plateforme à intégrer
- Expliquez les cas d'usage
- Fournissez des informations sur les APIs disponibles
- Indiquez si vous êtes prêt à contribuer au développement

### Contribuer du code 💻

1. Forkez le dépôt
2. Créez une branche de fonctionnalité (`git checkout -b feature/fonctionnalite-geniale`)
3. Effectuez vos modifications
4. Commitez en suivant nos directives
5. Poussez vers votre fork
6. Ouvrez une Pull Request

## 🛠️ Configuration du développement

### Prérequis

- Python 3.8 ou supérieur
- Visual TOM 6.x installé (pour les tests)
- Git
- Docker (optionnel, pour les tests conteneurisés)

### Configuration locale

```bash
# Cloner le dépôt
git clone https://github.com/AbsyssLab/<nom-connecteur>.git
cd <nom-connecteur>

# Créer l'environnement virtuel
python -m venv venv
source venv/bin/activate  # Sur Windows: venv\Scripts\activate

# Installer les dépendances
pip install -r requirements.txt
pip install -r requirements-dev.txt  # Si disponible

# Lancer les tests
pytest tests/
```

## 📝 Standards de code

### Guide de style Python

Nous suivons [PEP 8](https://www.python.org/dev/peps/pep-0008/) avec quelques règles spécifiques :

- **Longueur de ligne** : Maximum 120 caractères
- **Indentation** : 4 espaces (pas de tabulations)
- **Guillemets** : Utilisez les guillemets doubles pour les chaînes
- **Nommage** :
  - `snake_case` pour les fonctions et variables
  - `PascalCase` pour les classes
  - `UPPER_CASE` pour les constantes

### Outils de qualité du code

```bash
# Formater le code
black .

# Linter le code
flake8 .
pylint **/*.py

# Vérification des types
mypy .

# Vérifications de sécurité
bandit -r .
```

### Documentation

- Ajoutez des docstrings à toutes les fonctions et classes (style Google)
- Commentez la logique complexe
- Mettez à jour le README.md si vous ajoutez de nouvelles fonctionnalités
- Gardez les commentaires concis et significatifs

Exemple :
```python
def execute_job(job_name: str, parameters: dict) -> dict:
    """
    Exécute un job VTOM avec les paramètres spécifiés.
    
    Args:
        job_name: Nom du job à exécuter
        parameters: Dictionnaire des paramètres du job
        
    Returns:
        Dictionnaire contenant le statut d'exécution et les logs
        
    Raises:
        ConnectionError: Si impossible de se connecter à VTOM
        JobExecutionError: Si l'exécution du job échoue
    """
    # Implémentation
    pass
```

## 📝 Directives de commit

Nous suivons les [Commits Conventionnels](https://www.conventionalcommits.org/) :

### Format

```
<type>(<portée>): <sujet>

<corps>

<pied de page>
```

### Types

- `feat` : Nouvelle fonctionnalité
- `fix` : Correction de bug
- `docs` : Modifications de la documentation
- `style` : Changements de style de code (formatage, etc.)
- `refactor` : Refactorisation du code
- `perf` : Améliorations de performance
- `test` : Ajout ou mise à jour de tests
- `chore` : Tâches de maintenance
- `ci` : Changements CI/CD

### Exemples

```bash
feat(azure): ajout du support des identités managées

Implémente l'authentification via les identités managées Azure
pour une gestion plus sécurisée des credentials.

Closes #123

fix(jenkins): gestion correcte du timeout de connexion

Ajout d'une logique de retry avec backoff exponentiel quand
l'API Jenkins est temporairement indisponible.

Fixes #456

docs: mise à jour des instructions d'installation

Ajout d'une section dépannage pour les problèmes courants.
```

## 🔄 Processus de Pull Request

1. **Mettre à jour la documentation** - Assurez-vous que README, CHANGELOG et docs pertinents sont à jour
2. **Ajouter des tests** - Toutes les nouvelles fonctionnalités doivent inclure des tests
3. **Passer les vérifications CI** - Toutes les vérifications automatisées doivent passer
4. **Demander une revue** - Au moins une revue de mainteneur est requise
5. **Mettre à jour le changelog** - Ajoutez vos changements au CHANGELOG.md (si présent)
6. **Squasher les commits** - Considérez squasher les commits avant la fusion

### Checklist de Pull Request

- [ ] Le code suit les directives de style du projet
- [ ] Auto-revue effectuée
- [ ] Commentaires ajoutés pour le code complexe
- [ ] Documentation mise à jour
- [ ] Tests ajoutés et passants
- [ ] Aucun nouveau warning introduit
- [ ] Informations sensibles retirées (mots de passe, tokens, etc.)

## 🧪 Tests

### Lancer les tests

```bash
# Lancer tous les tests
pytest

# Lancer avec couverture
pytest --cov=. --cov-report=html

# Lancer un fichier de test spécifique
pytest tests/test_connector.py

# Lancer avec sortie verbeuse
pytest -v
```

### Écrire des tests

- Placez les tests dans le répertoire `tests/`
- Utilisez des noms de test descriptifs : `test_should_connect_successfully_with_valid_credentials`
- Testez les scénarios de succès et d'échec
- Mocquez les appels API externes
- Visez >80% de couverture de code

Exemple :
```python
import pytest
from unittest.mock import Mock, patch

def test_should_execute_job_successfully():
    """Test l'exécution réussie d'un job."""
    # Arrange
    connector = VTOMConnector(host="localhost")
    
    # Act
    result = connector.execute_job("test_job", {"param": "valeur"})
    
    # Assert
    assert result["status"] == "success"
    assert "job_id" in result
```

## 📚 Documentation

### Structure du README

Tous les README de connecteurs doivent inclure :

1. **Description** - Ce que fait le connecteur
2. **Prérequis** - Exigences et dépendances
3. **Installation** - Configuration étape par étape
4. **Configuration** - Toutes les options de configuration
5. **Utilisation** - Exemples et cas d'usage
6. **Dépannage** - Problèmes courants et solutions
7. **Contribution** - Lien vers ce guide
8. **Licence** - Apache License 2.0

### Commentaires de code

- Écrivez du code auto-documenté quand possible
- Ajoutez des commentaires pour la logique non évidente
- Gardez les commentaires à jour avec les changements de code
- Évitez les commentaires redondants

## 🏷️ Versioning

Nous utilisons le [Versioning Sémantique](https://semver.org/) :

- **MAJOR** : Changements incompatibles
- **MINOR** : Nouvelles fonctionnalités (rétrocompatibles)
- **PATCH** : Corrections de bugs (rétrocompatibles)

Exemple : `v1.2.3`

## 📞 Obtenir de l'aide

- 📖 Lisez le [Guide de support](SUPPORT.fr.md)
- 💬 Rejoignez les [Discussions](https://github.com/orgs/AbsyssLab/discussions)
- 🐛 Signalez les problèmes via les templates d'issues
- 📧 Contactez les mainteneurs pour les sujets sensibles

## 🎯 Issues pour débutants

Vous cherchez par où commencer ? Consultez les issues étiquetées :

- `good first issue` - Parfait pour les nouveaux venus
- `help wanted` - Nous avons besoin d'aide de la communauté
- `documentation` - Améliorez notre documentation

## 🌟 Reconnaissance

Les contributeurs seront :

- Listés dans CONTRIBUTORS.md (si présent)
- Mentionnés dans les notes de version
- Crédités dans l'historique des commits

## 📄 Licence

En contribuant, vous acceptez que vos contributions soient sous licence Apache License 2.0.

---

**Merci de contribuer à AbsyssLab ! 🙏**

<div align="center">
  <sub>Ensemble, nous améliorons les intégrations VTOM pour tous</sub>
</div>

