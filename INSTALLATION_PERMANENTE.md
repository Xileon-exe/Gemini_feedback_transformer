# Installation Permanente - Gemini Feedback Transformer

Ce document explique comment installer l'extension de manière permanente pour qu'elle reste active après chaque redémarrage de Firefox.

## ⚠️ Important
L'extension est maintenant en **Manifest V3** et packagée en `.xpi`. Elle nécessite une installation permanente pour éviter d'être supprimée à chaque redémarrage de Firefox.

## 🎯 Méthodes d'Installation Permanente

### Méthode 1 : Installation via about:addons (Recommandée pour usage personnel)

Cette méthode nécessite une signature, mais c'est la plus simple.

1. **Obtenir une extension signée**
   - Créez un compte sur [addons.mozilla.org](https://addons.mozilla.org)
   - Allez dans "Gérer mes modules"
   - Cliquez sur "Soumettre un nouveau module"
   - Choisissez "Sur cette plate-forme seulement" (Unlisted)
   - Téléversez le fichier `gemini-feedback-transformer-v3.xpi`
   - Téléchargez la version signée

2. **Installation**
   - Ouvrez Firefox et allez dans `about:addons`
   - Cliquez sur l'icône ⚙️ en haut à droite
   - Sélectionnez "Installer un module depuis un fichier..."
   - Choisissez votre fichier `.xpi` signé
   - L'extension restera active après redémarrage

### Méthode 2 : Politique d'Entreprise (Pour contrôle complet)

Cette méthode force l'installation via les politiques de groupe Firefox.

**Sur Windows :**

1. **Créer le dossier de distribution**
   ```cmd
   mkdir "%PROGRAMFILES%\Mozilla Firefox\distribution"
   ```

2. **Créer le fichier policies.json**
   Créez `%PROGRAMFILES%\Mozilla Firefox\distribution\policies.json` avec :
   ```json
   {
     "policies": {
       "Extensions": {
         "Install": ["file:///C:/path/to/your/gemini-feedback-transformer-v3.xpi"]
       },
       "ExtensionSettings": {
         "*": {
           "installation_mode": "allowed"
         },
         "gemini-feedback-transformer@example.com": {
           "installation_mode": "force_installed",
           "install_url": "file:///C:/path/to/your/gemini-feedback-transformer-v3.xpi"
         }
       }
     }
   }
   ```

3. **Permissions nécessaires**
   - Vous devez être administrateur
   - Remplacez le chemin par l'emplacement réel de votre fichier .xpi
   
4. **Redémarrer Firefox**
   - L'extension sera automatiquement installée
   - Elle restera active définitivement

**Sur macOS :**
Créez `/Applications/Firefox.app/Contents/Resources/distribution/policies.json`

**Sur Linux :**
Créez `/usr/lib/firefox/distribution/policies.json`

### Méthode 3 : Installation développeur (Temporaire)

⚠️ Cette méthode n'est PAS permanente mais utile pour les tests :

1. Ouvrez `about:debugging`
2. Cliquez sur "Ce Firefox"
3. Cliquez sur "Charger un module complémentaire temporaire"
4. Sélectionnez le fichier `manifest.json`

L'extension sera supprimée au redémarrage de Firefox.

## 🔧 Résolution de Problèmes

### L'extension disparaît au redémarrage
- Vous utilisez probablement la méthode 3 (temporaire)
- Utilisez la méthode 1 ou 2 pour une installation permanente

### Erreur "Extension non signée"
- Utilisez la méthode 1 avec une extension signée par Mozilla
- Ou utilisez la méthode 2 avec les politiques d'entreprise

### Permission refusée sur le fichier policies.json
- Vous devez être administrateur système
- Sur Windows, lancez l'éditeur de texte en tant qu'administrateur

## 🚀 Test de l'Installation

1. Installez l'extension avec une des méthodes ci-dessus
2. Allez sur [gemini.google.com](https://gemini.google.com)
3. Testez avec un message comme : `[4 étoiles: Très bonne réponse]`
4. Redémarrez Firefox
5. Vérifiez que l'extension est toujours active dans `about:addons`

## 📝 Notes

- **Méthode 1** : Idéale pour usage personnel, nécessite compte Mozilla
- **Méthode 2** : Parfaite pour déploiement en entreprise ou contrôle total
- Le fichier `.xpi` contient l'extension complète (Manifest V3, icônes, scripts)