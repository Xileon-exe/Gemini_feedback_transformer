# ✨ Gemini Feedback Transformer

[![Mozilla Add-on](https://img.shields.io/amo/v/{addon-id}?label=Firefox%20Add-on&logo=firefox)](https://addons.mozilla.org/firefox/addon/your-addon-slug/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Manifest](https://img.shields.io/badge/Manifest-V3-brightgreen.svg)](https://developer.mozilla.org/en-US/docs/Mozilla/Add-ons/WebExtensions/manifest.json)

Une extension Firefox qui transforme automatiquement les messages de feedback de Gemini en blocs visuels élégants avec étoiles et commentaires colorés.

## 🎆 Aperçu

**Avant :** `[4 étoiles: Très bonne réponse]`

**Après :** 🌟🌟🌟🌟☆ **Très bonne réponse** (bloc coloré)

## 🚀 Caractéristiques

- ✨ **Détection automatique** des messages de feedback entre crochets
- 🌟 **Système d'étoiles** colorées (1-5 étoiles)
- 🎨 **Blocs colorés** selon la note (rouge → vert)
- 📱 **Design responsive** avec animations fluides
- 🌙 **Mode sombre** automatique
- ⚡ **Performance optimisée** avec MutationObserver
- 🔒 **Sécurisé** avec Manifest V3

## 📦 Installation

### 🎆 Via Mozilla Add-ons (Recommandé)

**[Installer depuis Mozilla Add-ons](https://addons.mozilla.org/firefox/addon/your-addon-slug/)** ← **Version officielle signée**

- ✅ Installation en un clic
- ✅ Mises à jour automatiques
- ✅ Extension permanente (ne disparaît pas au redémarrage)

### 🔧 Installation développeur

1. **Cloner le dépôt**
   ```bash
   git clone https://github.com/votre-username/gemini-feedback-firefox-extension.git
   cd gemini-feedback-firefox-extension
   ```

2. **Charger l'extension**
   - Ouvrez Firefox et allez dans `about:debugging`
   - Cliquez sur "Ce Firefox"
   - Cliquez sur "Charger un module complémentaire temporaire"
   - Sélectionnez le fichier `manifest.json`

   ⚠️ **Note :** L'installation développeur est temporaire et disparaîtra au redémarrage de Firefox.

### 📄 Installation alternative

Consultez [`INSTALLATION_PERMANENTE.md`](INSTALLATION_PERMANENTE.md) pour d'autres méthodes d'installation permanente.

## 🎁 Utilisation

1. **Visitez Gemini** : Allez sur [gemini.google.com](https://gemini.google.com)
2. **Automatique** : L'extension détecte et transforme les feedbacks instantanément
3. **Profitez** : Vos messages de feedback sont maintenant visuellement élégants !

### 📝 Formats supportés

| Format | Exemple | Résultat |
|--------|---------|----------|
| **Français** | `[4 étoiles: Très utile]` | 🌟🌟🌟🌟☆ **Très utile** |
| **Anglais** | `[5 stars: Perfect!]` | 🌟🌟🌟🌟🌟 **Perfect!** |
| **Tiret** | `[3 étoiles - Correct]` | 🌟🌟🌟☆☆ **Correct** |
| **JSON** | `{"note":5,"description":"Génial"}` | 🌟🌟🌟🌟🌟 **Génial** |

## 🎨 Caractéristiques

- **Détection automatique** : Pas besoin d'action manuelle
- **Design adaptatif** : S'intègre parfaitement dans l'interface Gemini
- **Couleurs dynamiques** : Les blocs changent de couleur selon la note
- **Responsive** : Optimisé pour mobile et desktop
- **Mode sombre** : Support automatique du thème sombre
- **Performance** : Impact minimal sur les performances

## 🔧 Développement

### 📁 Structure du projet

```
gemini-feedback-firefox-extension/
├── manifest.json              # Configuration Manifest V3
├── content-script.js          # Script principal (ES6+)
├── styles.css                # Styles CSS3 avec animations
├── icons/                    # Icônes PNG (16,32,48,128px)
├── README.md                 # Documentation
├── CHANGELOG.md              # Historique des versions
├── LICENSE                   # Licence MIT
└── INSTALLATION_PERMANENTE.md # Guide installation
```

### 🛠️ Technologies

- ⚙️ **Manifest V3** : Standard moderne Firefox
- 📜 **JavaScript ES6+** : Classes, MutationObserver, DOM API
- 🎨 **CSS3** : Gradients, animations, responsive design
- 🔍 **MutationObserver** : Détection temps réel des nouveaux messages
- 🔒 **Content Security Policy** : Sécurité renforcée

### 📝 Développement local

1. **Fork** ce dépôt
2. **Cloner** votre fork
3. **Modifier** les fichiers source
4. **Tester** : Rechargez l'extension dans `about:debugging`
5. **Valider** sur [gemini.google.com](https://gemini.google.com)

## 🐛 Dépannage

<details>
<summary><b>L'extension ne fonctionne pas</b></summary>

- ✅ Vérifiez que l'extension est **activée** dans `about:addons`
- 🔄 **Rechargez** la page Gemini
- 🛠️ Ouvrez la **console développeur** (F12) pour voir les erreurs
- 🔄 **Redémarrez** Firefox si nécessaire

</details>

<details>
<summary><b>Les blocs ne s'affichent pas</b></summary>

- 📝 Vérifiez le **format** : `[X étoiles: commentaire]` ou `[X stars: comment]`
- 🌐 Confirmez que vous êtes sur **gemini.google.com**
- ⏱️ Attendez quelques secondes (détection automatique)
- 🔄 Essayez de **recharger l'extension** dans `about:debugging`

</details>

## 🤝 Contribution

Les contributions sont les bienvenues ! 🎉

### 🚀 Comment contribuer

1. 🍴 **Fork** ce dépôt
2. 🌱 **Créez** une branche : `git checkout -b feature/amazing-feature`
3. ✨ **Développez** votre fonctionnalité
4. ✅ **Testez** sur Gemini
5. 📝 **Commitez** : `git commit -m 'feat: Add amazing feature'`
6. 🚀 **Push** : `git push origin feature/amazing-feature`
7. 📨 **Ouvrez** une Pull Request

### 💡 Idées de contribution

- 🌍 Support d'autres langues
- 🎨 Nouveaux thèmes visuels
- 🔧 Améliorations des performances
- 📝 Documentation
- 🐛 Corrections de bugs

## 📄 Licence

[MIT License](LICENSE) - Libre d'utilisation, modification et distribution

## 👥 Crédits

- 🚀 **Développé** par [Xiléon](https://github.com/votre-username) avec ❤️
- 🤖 **Assisté** par Warp AI pour l'optimisation
- 🎆 **Inspiré** par le besoin d'améliorer l'expérience Gemini

## 🔗 Liens utiles

- 🌐 **[Mozilla Add-on Store](https://addons.mozilla.org/firefox/addon/your-addon-slug/)** ← Version officielle
- 🐛 **[Signaler un bug](https://github.com/votre-username/gemini-feedback-firefox-extension/issues)**
- 💬 **[Discussions](https://github.com/votre-username/gemini-feedback-firefox-extension/discussions)**
- 📚 **[Guide détaillé](INSTALLATION_PERMANENTE.md)**

---

<div align="center">

**⭐ Si cette extension vous a aidé, n'hésitez pas à lui donner une étoile sur GitHub ! ⭐**

</div>
