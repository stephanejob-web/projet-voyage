# 🚀 Guide Scrum + GitHub + Kanban (avec exemples)

## 1️⃣ Les Issues : le point de départ  

👉 **Règle d’or** : pas d’issue = pas de tâche.  

Une issue doit toujours contenir :  
- **Titre clair** (verbe à l’infinitif).  
- **Quoi ?** → ce qu’il faut faire.  
- **Pourquoi ?** → la valeur pour l’utilisateur/projet.  
- **Critères de validation (DoD)** → conditions qui prouvent que c’est terminé.  

---

### 🔹 Exemple 1 : nouvelle fonctionnalité  

**Titre :** Ajouter une page de connexion  

**Description :**  
- **Quoi ?** Créer une page avec champs *email* + *mot de passe* + bouton “Se connecter”.  
- **Pourquoi ?** Permettre aux utilisateurs de sécuriser l’accès.  
- **Critères de validation :**  
  1. La page s’affiche correctement.  
  2. L’authentification fonctionne avec des identifiants valides.  
  3. Les tests unitaires passent sans erreur.  

---

### 🔹 Exemple 2 : correction de bug  

**Titre :** Corriger l’affichage du bouton sur mobile  

**Description :**  
- **Quoi ?** Modifier le CSS pour que le bouton “Valider” s’affiche correctement sur petits écrans.  
- **Pourquoi ?** Améliorer l’expérience utilisateur sur mobile.  
- **Critères de validation :**  
  1. Le bouton est bien centré sur tous les formats d’écran.  
  2. Aucun chevauchement avec d’autres éléments.  
  3. Tests manuels validés sur Android et iPhone.  

---

### 🔹 Exemple 3 : amélioration visuelle (style)  

**Titre :** Améliorer le design du formulaire d’inscription  

**Description :**  
- **Quoi ?** Appliquer un design moderne avec Tailwind (couleurs, marges, arrondis).  
- **Pourquoi ?** Améliorer la lisibilité et l’attractivité du site.  
- **Critères de validation :**  
  1. Le formulaire est visuellement harmonieux.  
  2. Les champs sont alignés et lisibles.  
  3. Le design est validé par l’équipe.  

---

### 🔹 Exemple 4 : documentation  

**Titre :** Mettre à jour la documentation de l’API utilisateurs  

**Description :**  
- **Quoi ?** Ajouter les nouveaux endpoints `/users/login` et `/users/register`.  
- **Pourquoi ?** Tenir la documentation à jour pour les développeurs.  
- **Critères de validation :**  
  1. Les nouveaux endpoints apparaissent dans la doc.  
  2. Les exemples de requêtes/réponses sont corrects.  
  3. La documentation est lisible sur GitHub.  

---

### 🔹 Exemple 5 : ajout de tests  

**Titre :** Ajouter des tests pour la fonction `calculatePrice()`  

**Description :**  
- **Quoi ?** Écrire des tests unitaires pour vérifier les calculs avec TVA et réductions.  
- **Pourquoi ?** Garantir la fiabilité du calcul des prix.  
- **Critères de validation :**  
  1. Les tests couvrent tous les cas (normal, remise, gratuité).  
  2. 100% de couverture de la fonction.  
  3. Tous les tests passent avec succès.  

---

### 🔹 Exemple 6 : maintenance / configuration  

**Titre :** Mettre à jour la dépendance React vers la version 19  

**Description :**  
- **Quoi ?** Mettre à jour la version de React dans le projet et corriger les éventuels warnings.  
- **Pourquoi ?** Bénéficier des dernières optimisations et correctifs de sécurité.  
- **Critères de validation :**  
  1. La mise à jour est appliquée sans erreurs.  
  2. L’application fonctionne toujours normalement.  
  3. Les tests passent après la mise à jour.  

---

## 2️⃣ Le Kanban : organiser le travail  

Toutes les issues sont visibles dans un **tableau Kanban GitHub**.  
Ce tableau montre l’avancement de chaque tâche :  

- **To Do** → Tâches créées, pas encore commencées.  
- **In Progress** → Tâche en cours (⚠️ une seule par personne).  
- **Review** → Tâche terminée, en attente de validation.  
- **Done** → Tâche validée et finalisée.  

👉 Exemple :  
- Issue #12 “Ajouter une page de connexion” → *In Progress*  
- Issue #15 “Corriger le bug du bouton mobile” → *Review*  

---

## 3️⃣ Les Branches : une par issue  

👉 Chaque issue a **sa branche dédiée**.  

Convention de nommage :  

issue-<numéro>-<titre-court>


Exemples :  
- Issue #12 → `issue-12-login-page`  
- Issue #15 → `issue-15-fix-button`  

---

## 4️⃣ Les Commits : petits, clairs et typés  

Un bon commit doit être :  
- **Petit** → une seule idée par commit.  
- **Clair** → une phrase courte, à l’impératif, sans point final.  
- **Typé** → grâce à la convention *Conventional Commits*.  

---

### 📌 Les types de commits

| Type        | Signification | Exemple |
|-------------|---------------|---------|
| **feat:**   | Nouvelle fonctionnalité | `feat: ajouter une page de connexion (#12)` |
| **fix:**    | Correction d’un bug | `fix: corriger l’affichage du bouton mobile (#15)` |
| **docs:**   | Documentation uniquement | `docs: mettre à jour la doc API (#20)` |
| **style:**  | Mise en page / indentation (pas de logique) | `style: améliorer le design du formulaire (#18)` |
| **refactor:** | Réorganisation du code sans changer le résultat | `refactor: simplifier la fonction de calcul de prix (#40)` |
| **test:**   | Ajout ou modification de tests | `test: ajouter des tests pour calculatePrice (#25)` |
| **chore:**  | Maintenance / configuration / dépendances | `chore: mettre à jour React vers la v19 (#30)` |

---

### 📌 Exemples de commits

#### `feat:` (nouvelle fonctionnalité)  
```bash
feat: ajouter une page de connexion (#12)
feat: implémenter la recherche de produits (#18)
feat: ajouter le bouton de déconnexion (#21)
```


```bash
feat: ajouter une page de connexion (#12)
feat: implémenter la recherche de produits (#18)
feat: ajouter le bouton de déconnexion (#21)
```

```bash
style: améliorer le design du formulaire d’inscription (#18)
style: corriger l’indentation du fichier App.js (#33)
style: uniformiser les couleurs des boutons (#34)
```

```bash
refactor: simplifier la fonction calculatePrice (#40)
refactor: extraire le composant Header en fichier séparé (#41)
refactor: renommer les variables pour plus de clarté (#42)
```


```bash
test: ajouter des tests unitaires pour calculatePrice (#25)
test: corriger les tests du formulaire d’inscription (#26)
test: ajouter des tests d’intégration pour l’API utilisateurs (#43)

```

```bash
test: ajouter des tests unitaires pour calculatePrice (#25)
test: corriger les tests du formulaire d’inscription (#26)
test: ajouter des tests d’intégration pour l’API utilisateurs (#43)
```

```bash
chore: mettre à jour React vers la version 19 (#30)
chore: configurer ESLint pour le projet (#33)
chore: nettoyer les fichiers inutilisés (#44)
```

**🎯 Exemple d’historique de commits réaliste**

Issue #12 → Ajouter une page de connexion

```bash
feat: créer la page de connexion avec champs email et mot de passe (#12)
style: améliorer le design du formulaire de connexion (#12)
fix: corriger la validation du champ email (#12)
test: ajouter des tests unitaires pour la connexion (#12)
docs: mettre à jour la documentation sur l’authentification (#12)
```


👉 Résultat : une série de petits commits clairs et organisés, faciles à relire.


5️⃣ **Pull Requests (PR)**

Quand une branche est prête :

Ouvrir une Pull Request.

Relier l’issue → Closes #12.

Demander une review à un camarade.

Après validation → merge dans main.


6️⃣ **Scrum et Kanban**

To Do → tâches créées

In Progress → tâche en cours (1 par personne)

Review → tâche terminée, en attente de validation

Done → tâche validée

**Cérémonies Scrum :**

Sprint Planning → choisir les issues du sprint.

Daily (5 min) → dire ce qui est fait, ce qui reste, et si blocage.

Sprint Review → montrer ce qui est terminé.

Rétrospective → voir ce qui marche et ce qu’on peut améliorer.

```
⚡ Règles d’or

Pas d’issue = pas de tâche.

Pas de branche dédiée = pas de code.

Pas de commit clair = travail perdu.
```

1 issue → 1 branche → plusieurs commits → 1 PR → merge → Done ✅

🎯 Pourquoi cette méthode ?

Le projet est organisé et lisible.

Chacun sait qui fait quoi.

Vous travaillez comme une vraie équipe agile.
