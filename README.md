# Gemini Feedback Transformer

Une extension Firefox qui transforme l'affichage des messages de feedback de Gemini en blocs visuels avec étoiles et commentaires.

## 📋 Description

Cette extension détecte automatiquement les messages de feedback de Gemini affichés entre crochets (par exemple `[4 étoiles: Très bonne réponse]`) et les transforme en blocs visuels attrayants avec :
- Un système d'étoiles colorées (1-5 étoiles)
- Le commentaire affiché de manière lisible
- Un design adaptatif qui s'intègre naturellement dans la conversation

## 🚀 Installation

### ⭐ Installation Permanente (Recommandée)

L'extension est maintenant en **Manifest V3** et disponible sous forme de package `.xpi` pour une installation permanente.

**📦 Fichier prêt à installer :** `gemini-feedback-transformer-v3.xpi`

#### Méthode 1 : Via addons.mozilla.org (Recommandée)
1. Téléversez le fichier `.xpi` sur [addons.mozilla.org](https://addons.mozilla.org) en mode "Unlisted"
2. Téléchargez la version signée
3. Dans Firefox : `about:addons` → ⚙️ → "Installer un module depuis un fichier..."
4. L'extension restera active après redémarrage ✅

#### Méthode 2 : Politique d'entreprise (Windows)
1. Créez `%PROGRAMFILES%\Mozilla Firefox\distribution\policies.json`
2. Configurez l'installation forcée (voir `INSTALLATION_PERMANENTE.md`)
3. Redémarrez Firefox → Extension installée automatiquement ✅

📋 **Guide détaillé :** Consultez `INSTALLATION_PERMANENTE.md` pour toutes les méthodes

### Installation temporaire (développement uniquement)

⚠️ **Attention :** Cette méthode est temporaire et l'extension disparaîtra au redémarrage de Firefox.

1. **Cloner le projet**
   ```bash
   git clone https://github.com/username/gemini-feedback-firefox-extension.git
   cd gemini-feedback-firefox-extension
   ```

2. **Installation développeur**
   - Ouvrez Firefox : `about:debugging`
   - "Ce Firefox" → "Charger un module complémentaire temporaire"
   - Sélectionnez le fichier `manifest.json`

## 💡 Utilisation

1. **Visitez Gemini** : Rendez-vous sur `gemini.google.com`
2. **Feedback automatique** : L'extension détecte automatiquement les messages de feedback entre crochets
3. **Transformation visuelle** : Les messages sont instantanément transformés en blocs colorés

### Formats supportés

L'extension reconnaît ces formats de feedback :
- `[3 étoiles: Bonne explication]`
- `[5 stars: Excellent response!]`
- `[1 étoile : Réponse insuffisante]`
- `[4 étoiles - Très utile]`

## 🎨 Caractéristiques

- **Détection automatique** : Pas besoin d'action manuelle
- **Design adaptatif** : S'intègre parfaitement dans l'interface Gemini
- **Couleurs dynamiques** : Les blocs changent de couleur selon la note
- **Responsive** : Optimisé pour mobile et desktop
- **Mode sombre** : Support automatique du thème sombre
- **Performance** : Impact minimal sur les performances

## 🔧 Développement

### Structure du projet

```
gemini-feedback-firefox-extension/
├── manifest.json          # Configuration de l'extension
├── content-script.js      # Script principal de transformation
├── styles.css            # Styles pour les blocs de feedback
├── README.md             # Documentation
└── icons/               # Icônes de l'extension (à ajouter)
```

### Technologies utilisées

- **JavaScript ES6+** : Logique de détection et transformation
- **CSS3** : Styles et animations
- **Firefox WebExtensions API** : Intégration navigateur

### Développement local

1. Modifier les fichiers source
2. Recharger l'extension dans `about:debugging`
3. Tester sur `gemini.google.com`

## 🐛 Résolution de problèmes

### L'extension ne fonctionne pas
- Vérifiez que l'extension est activée dans `about:addons`
- Rechargez la page Gemini
- Vérifiez la console du navigateur pour les erreurs

### Les blocs ne s'affichent pas
- Assurez-vous que le format du feedback est correct
- Vérifiez que vous êtes bien sur `gemini.google.com`
- Essayez de recharger l'extension

## 📏 Changelog

### v1.1.0 (Actuel) - 2025-10-15
- ⭐ **Migration vers Manifest V3** : Extension moderne et compatible future
- 💻 **Installation permanente** : Fini les extensions éphémères
- 🎨 **Icônes d'extension** : Visuels professionnels aux bonnes tailles
- 📦 **Package .xpi** : Prêt à installer, signé par Mozilla
- 📄 **Documentation complète** : Guide d'installation permanent détaillé

### v1.0.0 - 2025-10-15
- Détection automatique des messages de feedback
- Transformation en blocs avec étoiles
- Support des formats français et anglais
- Design responsive et mode sombre

Voir `CHANGELOG.md` pour plus de détails.

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour contribuer :

1. Fork le projet
2. Créez une branche pour votre fonctionnalité
3. Committez vos changements
4. Poussez vers la branche
5. Ouvrez une Pull Request

## 📄 Licence

Ce projet est sous licence MIT. Voir le fichier `LICENSE` pour plus de détails.

## 👥 Auteur

Développé avec ❤️ pour améliorer l'expérience utilisateur de Gemini.

## 🔗 Liens

- [Repository GitHub](https://github.com/username/gemini-feedback-firefox-extension)
- [Firefox Add-ons Store](https://addons.mozilla.org) (bientôt disponible)
- [Signaler un bug](https://github.com/username/gemini-feedback-firefox-extension/issues)