# Changelog - Gemini Feedback Transformer

Toutes les modifications notables de ce projet sont documentées dans ce fichier.

## [1.1.0] - 2025-10-15

### ✨ Ajouté
- **Migration vers Manifest V3** : Extension maintenant compatible avec les standards modernes de Firefox
- **Icônes d'extension** : Ajout d'icônes PNG aux tailles 16x16, 32x32, 48x48, 128x128
- **Installation permanente** : Plusieurs méthodes pour installer l'extension de façon permanente
- **Package .xpi** : Extension empaquetée et prête à installer
- **Documentation d'installation** : Guide détaillé pour l'installation permanente (`INSTALLATION_PERMANENTE.md`)
- **Support des politiques d'entreprise** : Possibilité d'installation forcée via policies.json

### 🔧 Modifié
- **manifest.json** : Migré de la version 2 vers la version 3
- **Permissions** : Remplacement de `activeTab` par `host_permissions` et `storage`
- **Version** : Passage de 1.0.0 à 1.1.0
- **Icônes** : Mise à jour des références vers les nouvelles icônes PNG

### 🚀 Améliorations
- **Compatibilité future** : Manifest V3 assure la compatibilité avec les futures versions de Firefox
- **Sécurité renforcée** : Permissions plus granulaires et sécurisées
- **Performance** : Exécution des content scripts optimisée avec `document_idle`
- **Installation robuste** : Fini les extensions éphémères qui disparaissent au redémarrage

### 📝 Documentation
- Ajout du guide d'installation permanente
- Mise à jour du README avec les nouvelles instructions
- Documentation des trois méthodes d'installation

### 🔗 Méthodes d'installation disponibles
1. **Via addons.mozilla.org** (Signature officielle - Recommandé)
2. **Politique d'entreprise** (Installation forcée via policies.json)
3. **Installation développeur** (Temporaire pour tests)

---

## [1.0.0] - 2025-10-15

### ✨ Version initiale
- **Détection automatique** des messages de feedback de Gemini entre crochets
- **Transformation visuelle** en blocs avec étoiles et commentaires colorés
- **Formats supportés** : `[X étoiles: commentaire]` et format JSON
- **Design responsive** avec animations et effets hover
- **Mode sombre** automatique selon les préférences système
- **Content script robuste** avec MutationObserver pour détecter les nouveaux messages
- **Styles CSS avancés** avec dégradés et transitions fluides

### 🎨 Caractéristiques V1.0
- Support des formats français et anglais
- Système d'étoiles colorées (1-5 étoiles)
- Blocs colorés selon la note (rouge → vert)
- Détection sur gemini.google.com et bard.google.com
- Traitement en temps réel des nouveaux messages