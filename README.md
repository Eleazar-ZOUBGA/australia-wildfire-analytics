# Australia Wildfire Dashboard

Une application web interactive développée avec **Dash** et **Plotly** pour analyser et visualiser les données historiques des feux de forêt en Australie à partir de 2005.

---

## Présentation du Projet
Ce tableau de bord interactif permet d'explorer l'activité des incendies de végétation en Australie. L'utilisateur peut filtrer dynamiquement les données par **région** administrative et par **année** pour analyser deux métriques clés : la superficie moyenne estimée des incendies et le nombre moyen de pixels détectant des feux de végétation.

## Fonctionnalités de l'Application
* **Sélection par Boutons Radio :** Choix de la région australienne (ex: Victoria, New South Wales, Queensland, etc.).
* **Menu Déroulant (Dropdown) :** Filtrage temporel par année unique présente dans le jeu de données.
* **Mise à jour en temps réel (Callbacks) :**
  * **Graphique en secteur (Pie Chart) :** Répartition mensuelle de la superficie moyenne estimée des incendies (`Estimated_fire_area`).
  * **Graphique en barres (Bar Chart) :** Évolution mensuelle du nombre moyen de pixels détectés pour les feux de végétation présumés (`Count`).

---

## Configuration et Installation

### Prérequis
L'application nécessite **Python 3.8+** ainsi que les bibliothèques suivantes :
* `pandas`
* `dash`
* `plotly`

### Installation
1. Clonez ce dépôt sur votre machine locale :
   ```bash
   git clone [https://github.com/Eleazar-ZOUBGA/australia-wildfire-analytics.git](https://github.com/Eleazar-ZOUBGA/australia-wildfire-analytics.git)
   cd australia-wildfire-analytics

```

2. Installez les dépendances requises via `pip` :
```bash
pip install pandas dash plotly

```



---

## Lancement de l'Application

Pour démarrer le serveur de développement Dash, exécutez simplement le script Python principal :

```bash
python3.8 Dash_wildfire.py

```

Une fois le script lancé, ouvrez votre navigateur web et accédez à l'adresse locale suivante :
[http://127.0.0.1:8050/](http://127.0.0.1:8050/)

---

## Origine des Données

Les données utilisées proviennent des observations historiques de la NASA (Firms MCD14DL) collectées et hébergées sur le cloud storage d'IBM Skills Network.

Le jeu de données inclut automatiquement :

* Les régions converties sous forme de codes abrégés (`NSW`, `NT`, `QL`, `SA`, `TA`, `VI`, `WA`).
* Des transformations temporelles pour extraire l'année (`Year`) et le nom complet du mois (`Month`) afin de faciliter la lecture des graphiques.

```

```