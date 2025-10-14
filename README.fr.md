# Dépôt .github

[🇬🇧 English version](README.md)

Ce dépôt contient les **fichiers de santé communautaire par défaut** et templates pour tous les dépôts de l'organisation **AbsyssLab**.

## 📂 Contenu

Ce dépôt fournit des valeurs par défaut à l'échelle de l'organisation qui seront utilisées par tous les dépôts AbsyssLab qui n'ont pas leurs propres versions de ces fichiers.

### 🏛️ Profil de l'Organisation

- **[profile/README.md](profile/README.md)** - Profil public de l'organisation affiché sur [github.com/AbsyssLab](https://github.com/AbsyssLab)

### 📋 Templates d'Issues

Situés dans `ISSUE_TEMPLATE/` :

- **[bug_report.yml](ISSUE_TEMPLATE/bug_report.yml)** - Template pour les rapports de bugs
- **[feature_request.yml](ISSUE_TEMPLATE/feature_request.yml)** - Template pour les demandes de fonctionnalités
- **[connector_request.yml](ISSUE_TEMPLATE/connector_request.yml)** - Template pour les propositions de nouveaux connecteurs
- **[config.yml](ISSUE_TEMPLATE/config.yml)** - Configuration des templates d'issues

### 🔄 Template de Pull Request

- **[pull_request_template.md](PULL_REQUEST_TEMPLATE/pull_request_template.md)** - Template standard de PR

### ⚙️ Templates de Workflows

Situés dans `workflow-templates/` :

- **[python-ci.yml](workflow-templates/python-ci.yml)** - Workflow CI/CD pour projets Python
  - Linting (flake8, pylint)
  - Tests (pytest)
  - Scanning de sécurité (bandit, safety)
  - Build Docker
- **[release.yml](workflow-templates/release.yml)** - Workflow de release automatisé
  - Génération de changelog
  - Artefacts de release
  - Publication d'images Docker

### 📚 Fichiers de Santé Communautaire

- **[CONTRIBUTING.md](CONTRIBUTING.md)** - Comment contribuer ([🇫🇷 Français](CONTRIBUTING.fr.md))
- **[CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)** - Directives communautaires ([🇫🇷 Français](CODE_OF_CONDUCT.fr.md))
- **[SECURITY.md](SECURITY.md)** - Politique de sécurité et signalement de vulnérabilités ([🇫🇷 Français](SECURITY.fr.md))
- **[SUPPORT.md](SUPPORT.md)** - Comment obtenir de l'aide ([🇫🇷 Français](SUPPORT.fr.md))
- **[LICENSE](LICENSE)** - Apache License 2.0

## 🌍 Support Linguistique

Ce dépôt fournit la documentation en :
- **Anglais** (principal) - Tous les fichiers
- **Français** - Fichiers de santé communautaire avec l'extension `.fr.md`

Chaque version linguistique inclut des liens pour basculer entre les langues.

## 🎯 Objectif

### Pour les Mainteneurs de Dépôts

Ces valeurs par défaut assurent la cohérence entre tous les dépôts AbsyssLab :
- Directives de contribution standardisées
- Templates d'issues et PR unifiés
- Standards de code cohérents
- Pratiques de sécurité communes
- Workflows GitHub Actions réutilisables

### Pour les Contributeurs

Trouvez tout ce dont vous avez besoin pour contribuer :
- Directives de contribution claires
- Templates de rapport de bugs
- Processus de demande de fonctionnalités
- Signalement de vulnérabilités de sécurité
- Ressources de support

## 📖 Comment Ça Fonctionne

GitHub utilise automatiquement les fichiers de ce dépôt `.github` comme valeurs par défaut pour tout dépôt de l'organisation qui n'a pas ses propres versions.

### Précédence

```
Fichiers au niveau du dépôt > Fichiers du dépôt .github > Valeurs par défaut GitHub
```

Si un dépôt a son propre `CONTRIBUTING.md`, celui-ci sera utilisé à la place de celui de ce dépôt.

### Portée

Ces valeurs par défaut s'appliquent à :
- ✅ Dépôts publics
- ✅ Dépôts privés
- ✅ Tous les membres de l'organisation
- ✅ Contributeurs externes

## 🚀 Utilisation des Templates de Workflows

Les templates de workflows peuvent être utilisés lors de la création de nouveaux workflows dans n'importe quel dépôt :

1. Allez dans l'onglet **Actions** du dépôt
2. Cliquez sur **New workflow**
3. Voir la section **Workflows created by AbsyssLab**
4. Choisissez un template et configurez-le

Les templates incluent :
- Pipeline CI/CD Python
- Gestion de release automatisée

## 📝 Personnalisation pour Votre Dépôt

Si un dépôt a besoin de directives différentes :

1. **Copiez le fichier** depuis `.github` vers votre dépôt
2. **Modifiez-le** selon vos besoins
3. **Commitez** - votre version remplacera la valeur par défaut

Exemple :
```bash
# Copier CONTRIBUTING.md dans votre dépôt
cp ../.github/CONTRIBUTING.md .
# Éditer et personnaliser
vim CONTRIBUTING.md
# Commiter
git add CONTRIBUTING.md
git commit -m "Ajout de directives de contribution personnalisées"
```

## 🔧 Maintenance de ce Dépôt

### Mise à Jour des Templates

Lors de la mise à jour des templates :

1. **Testez les changements** dans un dépôt d'exemple d'abord
2. **Documentez les changements** dans la pull request
3. **Notifiez** via GitHub Discussions si changements majeurs
4. **Versionnez** les changements significatifs (utilisez des tags)

### Bonnes Pratiques

- Gardez les templates génériques et réutilisables
- Évitez les informations spécifiques au dépôt
- Utilisez des placeholders pour le contenu dynamique
- Maintenez les versions anglaise et française
- Testez les templates avant de merger
- Obtenez des retours des mainteneurs

### Calendrier de Révision

- **Mensuel** - Révision et mise à jour si nécessaire
- **Trimestriel** - Collecte de retours de la communauté
- **Annuel** - Révision majeure si nécessaire

## 📊 Ce Qui Est Appliqué Où

| Fichier | Utilisé Pour | Repli Sur |
|---------|--------------|-----------|
| CONTRIBUTING.md | Directives de contribution | Défaut GitHub |
| CODE_OF_CONDUCT.md | Standards communautaires | Aucun |
| SECURITY.md | Politique de sécurité | Aucun |
| SUPPORT.md | Ressources de support | Aucun |
| LICENSE | Licence par défaut | Aucun |
| Templates d'issues | Création d'issues | Défauts GitHub |
| Template de PR | Création de pull requests | Défaut GitHub |
| Templates de workflows | Workflows Actions | Aucun |

## 🤝 Contribuer à ce Dépôt

Vous voulez améliorer les valeurs par défaut de l'organisation ?

1. **Ouvrez une issue** pour discuter des changements majeurs
2. **Soumettez une PR** avec vos améliorations
3. **Testez** dans un dépôt d'exemple
4. **Documentez** ce que vous avez changé et pourquoi

Voir [CONTRIBUTING.md](CONTRIBUTING.fr.md) pour les directives détaillées.

## 📞 Questions ?

- 💬 [Discussions](https://github.com/orgs/AbsyssLab/discussions) - Posez des questions
- 🐛 [Issues](https://github.com/AbsyssLab/.github/issues) - Signalez des problèmes
- 📖 [Guide de Support](SUPPORT.fr.md) - Obtenez de l'aide

## 📚 Ressources

### Documentation GitHub

- [Création d'un fichier de santé communautaire par défaut](https://docs.github.com/fr/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)
- [À propos des templates d'issues et de pull requests](https://docs.github.com/fr/communities/using-templates-to-encourage-useful-issues-and-pull-requests/about-issue-and-pull-request-templates)
- [Création de templates de workflows](https://docs.github.com/fr/actions/using-workflows/creating-starter-workflows-for-your-organization)

### Ressources AbsyssLab

- [Profil de l'Organisation](https://github.com/AbsyssLab)
- [Tous les Dépôts](https://github.com/orgs/AbsyssLab/repositories)
- [Connecteurs VTOM](https://github.com/AbsyssLab?q=vtom&type=all)

## 📄 Licence

Ce dépôt et tous les fichiers par défaut sont sous licence [Apache License 2.0](LICENSE).

## 🌟 Impact

Ce dépôt aide à maintenir la qualité et la cohérence sur :
- **18+ connecteurs** pour Visual TOM
- **Plusieurs contributeurs** de diverses organisations
- **Divers cas d'usage** en environnements de production

---

<div align="center">
  <strong>Construire de meilleures pratiques open source chez AbsyssLab</strong>
  <br/>
  <sub>Dernière mise à jour : Octobre 2025</sub>
</div>

