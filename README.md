# keycloak-react-native
mon app test react-native avec une authentification keycloak

# creation d'un projet expo : 
npx create-expo-app

# installation des libraires nécessaires : 
npx expo install expo-auth-session expo-crypto
npx expo install expo-web-browser
npx expo install expo-secure-store (à intégrer plus tard pour enregister le accessStore de façon sécurisée via les keychaine de iOs et Android)

# créer les répertoires ios et android : 
expo prebuild
cd ios
pod install (pour installer les dépendances via cocoapods pour iOS) 

# faire les modification des fichiers iOS (config.plist, appDelegate.mm, AppDelegate.h) et Android (AndroidManifest.yml) pour le support du deep linking

# Créer un client keycloak en activant le pkce pour le authorization code flow et mettre les URLs 

# Créer des fonctions asynchrones pour l'authentification : 
- Créer une fonction login avec AuthRequest() qui récupère le code d'autorisation et exchangeCodeAsync() qui l'échange contre le token.
