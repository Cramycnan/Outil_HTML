# Outil HTML - Fiche Client Compositeur

![Version](https://img.shields.io/badge/version-1.0-blue.svg)
![License](https://img.shields.io/badge/license-MIT-green.svg)
![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)

## 📝 Description

Application web de prise d'information client pour **compositeurs de musique à l'image**. Cet outil professionnel permet de recueillir de manière structurée toutes les informations essentielles au début d'un projet de composition musicale (film, documentaire, série TV, jeu vidéo, publicité, etc.).

### ✨ Caractéristiques principales

- 🎯 **8 sections thématiques** couvrant tous les aspects d'un projet
- 📊 **46 champs de données** pour une prise d'information exhaustive
- 💾 **Sauvegarde automatique** dans le navigateur (localStorage)
- 📥 **Import/Export** en JSON et TXT
- 📈 **Suivi de progression** en temps réel (% de complétion)
- 🖨️ **Version imprimable** optimisée
- 📱 **Responsive** adapté mobile/tablette/desktop
- ⌨️ **Raccourcis clavier** (Ctrl+S pour sauvegarder, Ctrl+E pour exporter)
- 🎨 **Interface moderne** avec design épuré et animations fluides

## 🚀 Installation et utilisation

### Pré-requis

- Navigateur web moderne (Chrome, Firefox, Safari, Edge)
- Aucune installation requise
- Aucune connexion internet nécessaire après téléchargement

### Lancement

1. **Téléchargez** le fichier `composer-client-checklist.html`
2. **Double-cliquez** sur le fichier pour l'ouvrir dans votre navigateur
3. **Commencez** à remplir le formulaire !

**Alternative avec serveur local :**
```bash
# Python 3
python3 -m http.server 8000

# PHP
php -S localhost:8000

# Node.js (avec npx http-server)
npx http-server -p 8000
```

Puis accédez à : `http://localhost:8000/composer-client-checklist.html`

## 📋 Sections du formulaire

### 1. Informations sur le Projet
- Type de projet (film, documentaire, série, jeu vidéo, etc.)
- Durée totale du projet
- Synopsis et pitch
- Public cible
- Plateformes de diffusion

### 2. Aspects Financiers
- Budget alloué à la musique
- Mode de paiement
- Coûts additionnels (musiciens, studio, etc.)

### 3. Spécifications Musicales
- Durée musicale estimée
- Thèmes et émotions recherchées
- Style et genre musical
- Instrumentation souhaitée
- Références et inspirations

### 4. Planning et Délais
- Timeline globale
- Dates clés et jalons
- Disponibilité du compositeur

### 5. Production Technique
- Présence d'un ingénieur du son
- Formats de livraison
- Contraintes de synchronisation

### 6. Aspects Juridiques et Droits
- Inscription SACEM
- Cession de droits
- Crédits et mentions
- Utilisation portfolio

### 7. Modalités de Collaboration
- Interlocuteurs et contacts
- Processus de validation
- Nombre de révisions incluses

### 8. Éléments Complémentaires
- Temp tracks existants
- Contraintes techniques
- Besoins futurs
- Coordonnées de facturation

## 💾 Gestion des données

### Sauvegarde automatique
Le formulaire sauvegarde **automatiquement** vos données à chaque modification dans le stockage local de votre navigateur.

### Export manuel
- **Export JSON** : Données structurées pour backup ou traitement ultérieur
- **Export TXT** : Format texte lisible pour impression ou partage
- **Raccourci** : `Ctrl + E`

### Import de données
Glissez-déposez un fichier JSON exporté précédemment pour restaurer les données d'un projet.

### Réinitialisation
Bouton "Réinitialiser" pour effacer toutes les données (avec confirmation de sécurité).

## ⌨️ Raccourcis clavier

| Raccourci | Action |
|-----------|--------|
| `Ctrl + S` | Sauvegarde manuelle |
| `Ctrl + E` | Exporter les données |
| `Ctrl + P` | Imprimer le formulaire |

## 🎨 Personnalisation

Le fichier est autonome et peut être personnalisé directement :

- **Couleurs** : Modifiez les gradients CSS (lignes 18, 33)
- **Logo** : Ajoutez votre logo dans le header (ligne 32-37)
- **Champs** : Ajoutez/supprimez des questions dans les sections
- **Langue** : Traduisez les labels et textes

## 📊 Indicateur de progression

Un cercle de progression affiché en bas à droite indique :
- **Pourcentage** de champs remplis
- **Nombre** de champs complétés / total
- **Code couleur** : vert = rempli, neutre = vide

## 🔒 Confidentialité et sécurité

- ✅ **Aucune donnée** n'est envoyée sur internet
- ✅ **Stockage 100% local** dans votre navigateur
- ✅ **Aucun tracking** ou analytics
- ✅ **Aucun cookie** externe
- ⚠️ **Important** : Les données sont liées au navigateur. Pensez à exporter régulièrement !

## 🐛 Problèmes connus

- Les données sont effacées si vous nettoyez le cache du navigateur
- Pas de synchronisation entre appareils (solution : export/import manuel)
- Nécessite JavaScript activé

## 🛠️ Technologies utilisées

- **HTML5** - Structure
- **CSS3** - Design responsive et animations
- **JavaScript Vanilla** - Logique et interactions
- **localStorage API** - Persistance des données

## 📄 Licence

Ce projet est sous licence MIT. Vous êtes libre de l'utiliser, le modifier et le distribuer.

## 🤝 Contribution

Les contributions sont les bienvenues ! Pour proposer des améliorations :

1. Forkez le projet
2. Créez une branche (`git checkout -b feature/amelioration`)
3. Committez vos changements (`git commit -m 'Ajout fonctionnalité X'`)
4. Pushez vers la branche (`git push origin feature/amelioration`)
5. Ouvrez une Pull Request

## 💡 Suggestions d'améliorations futures

Consultez le fichier [IMPROVEMENTS.md](./IMPROVEMENTS.md) pour la liste complète des améliorations envisagées.

Priorités :
- 🔜 Système multi-projets
- 🔜 Export PDF professionnel
- 🔜 Templates de projets
- 🔜 Mode sombre

## 📞 Support

Pour toute question ou suggestion :
- Ouvrez une issue sur GitHub
- Consultez la documentation dans [CLAUDE.md](./CLAUDE.md)

## 📚 Ressources

- [Guide compositeur musique à l'image](https://www.sacem.fr)
- [Tarification musique à l'image](https://www.saccef.fr)
- [Contrats types SACEM](https://www.sacem.fr/espace-professionnel/contrats)

---

**Développé avec ❤️ pour les compositeurs de musique à l'image**

*Version 1.0 - 2025*
