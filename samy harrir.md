# Calculateur d'IMC - Projet Flutter

Application mobile réalisée dans le cadre du module Flutter. Elle permet à l'utilisateur de calculer son Indice de Masse Corporelle (IMC) via une interface interactive et d'obtenir une interprétation immédiate de son état de santé.

## Fonctionnalités
- **Saisie interactive** : Utilisation de Sliders pour ajuster la taille et le poids.
- **Calcul en temps réel** : Mise à jour automatique des données via la gestion d'état.
- **Feedback visuel** : Code couleur dynamique (Vert, Orange, Rouge) et messages d'interprétation selon le résultat.
- **Navigation fluides** : Transition entre la page de configuration et la page de résultat.

## Architecture Technique
Le projet respecte une séparation stricte entre la logique métier et l'interface utilisateur (Pattern MVVM simplifié).

### Structure du projet
```text
lib/
├── logic/          # Logique Métier (State Management)
│   └── bmi_provider.dart  -> Contient la formule de calcul et les données (Poids/Taille).
├── screens/        # Interface Utilisateur (UI)
│   ├── input_page.dart    -> Écran de saisie (Sliders).
│   └── result_page.dart   -> Écran de résultat (Affichage passif).
└── main.dart       # Point d'entrée & Configuration du Router