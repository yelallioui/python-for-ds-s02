# 🔢 Séance 2 — NumPy : penser en tableaux

_Master IA‑GI · Python pour les sciences de données · FPK / USMS_

Ce dépôt contient **le TP de la séance 2**. Deux notebooks, à faire **dans l'ordre** :

| | Notebook | Durée | Ouvrir dans Colab |
|---|---|---|---|
| **1** | **Partie 1 · Pratiquer** : 39 exercices en 9 séries, de votre premier tableau jusqu'aux fichiers | environ 2 h | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yelallioui/python-for-ds-s02/blob/main/tp-seance-02.ipynb) |
| **2** | **Partie 2 · Mini‑projet Titanic** : charger, interroger, écrire un CSV, puis découvrir les limites de NumPy | environ 45 min | [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/yelallioui/python-for-ds-s02/blob/main/mini-projet-02/mini-projet-02.ipynb) |

---

## 🚀 Pour commencer : 3 étapes

### Étape 1 · Ouvrir le notebook
Cliquez sur **Open in Colab** (tableau ci‑dessus). Connectez‑vous avec votre **compte Google** si Colab le demande. Le notebook s'ouvre dans **votre** session Colab.

### Étape 2 · Faire votre copie (à ne pas oublier ⚠️)
Colab **ne sauvegarde pas** un notebook ouvert depuis GitHub : si vous fermez l'onglet, **tout est perdu**. Dès l'ouverture :

1. Menu **Fichier ▸ Enregistrer une copie dans Drive**.
2. Une **copie** s'ouvre dans un nouvel onglet : **travaillez dans cette copie**, et fermez l'original.

### Étape 3 · Travailler
- **Remplissez d'abord la cellule 🪪 « Qui êtes‑vous ? »** : votre **nom**, votre **prénom** et votre **CNE**, entre guillemets. Le contrôle reste ❌ tant qu'elle n'est pas remplie.
- Exécutez les cellules **dans l'ordre** (`Maj + Entrée`).
- Faites chaque exercice en remplaçant les `...` par votre code. Un **✅** ou un **❌** s'affiche sous chaque exercice ; en cas de ❌, ouvrez l'**indice 1**, puis 2, puis 3.
- **Partie 1** : rien d'autre à faire, elle est indépendante.
- **Mini‑projet** : Colab ouvre le notebook **sans son dossier**. Avant tout, exécutez dans **une cellule** ces deux lignes (elles sont aussi rappelées en haut du notebook) :

  ```
  !git clone https://github.com/yelallioui/python-for-ds-s02
  %cd python-for-ds-s02/mini-projet-02
  ```

---

## 📂 Créer votre dépôt GitHub (pour rendre votre travail)

![Visibilité : PRIVATE obligatoire](https://img.shields.io/badge/Visibilit%C3%A9-PRIVATE%20OBLIGATOIRE-red?style=for-the-badge)

> [!CAUTION]
> **CHOISISSEZ « PRIVATE ». GitHub propose « Public » par défaut : changez‑le !**
>
> Un dépôt **public** est visible par **tout le monde**, avec **vos réponses et votre CNE**. Si vous vous trompez, voir « En cas de problème » plus bas.

1. Créez un compte sur [github.com](https://github.com) si vous n'en avez pas (gratuit).
2. En haut de **cette page**, cliquez sur le bouton vert **Use this template**, puis **Create a new repository**.
3. **Nom du dépôt** : **`nom-prenom-s02`**, en **minuscules**, **sans accent**, **sans espace** (remplacez‑les par des tirets). Exemple : `benali-sara-s02`.
4. **Visibilité : cochez `Private`** (voir l'encadré rouge ci‑dessus), puis **Create repository**.
5. Dans Colab : **Fichier ▸ Ouvrir le notebook ▸ onglet GitHub**. Saisissez votre identifiant GitHub, cochez **Include private repos** (autorisez Colab si demandé), puis choisissez votre dépôt et le notebook.
6. Pour sauvegarder : **Fichier ▸ Enregistrer une copie dans GitHub**.

> ⚠️ Les boutons **Open in Colab** de cette page et des notebooks ouvrent toujours la **version d'origine** de l'enseignant. Pour rouvrir **votre** copie, passez par l'onglet **GitHub** de Colab (point 5).

---

## 📤 Partager votre dépôt avec l'enseignant

Votre dépôt est **privé** : l'enseignant ne peut le voir que si **vous l'y invitez**. Le **nom du dépôt** est la première chose qu'il verra : respectez la convention `nom-prenom-s02`.

1. Ouvrez **votre** dépôt sur GitHub (celui créé avec **Use this template**).
2. Cliquez sur l'onglet **Settings** (en haut de la page du dépôt), puis sur **Collaborators** dans le menu de gauche.
3. Cliquez sur **Add people**, saisissez **`yelallioui`**, choisissez ce compte dans la liste, puis cliquez sur **Add yelallioui to this repository**.
4. **Envoyez l'adresse de votre dépôt** à l'enseignant, par le moyen indiqué en cours. Elle ressemble à `https://github.com/votre-identifiant/nom-prenom-s02`. L'enseignant reçoit une invitation et l'accepte.

> 💡 L'enseignant ne voit que ce qui est **dans le dépôt**. Quand vous avez terminé une séance de travail, faites **Fichier ▸ Enregistrer une copie dans GitHub** (point 6 de la section précédente) : le notebook est enregistré **avec ses résultats**, les ✅ et les ❌ y restent visibles.

---

## 💻 Sur votre ordinateur (sans Colab)

1. Installez **Python 3** avec Jupyter (le plus simple : [Anaconda](https://www.anaconda.com/download)), ou VS Code avec l'extension Jupyter. NumPy doit être installé : `pip install numpy` (déjà présent avec Anaconda).
2. Téléchargez le dépôt (**Code ▸ Download ZIP**) ou clonez‑le, puis **décompressez‑le** si besoin.
3. Ouvrez chaque notebook **depuis son dossier**, sans le déplacer : la partie 1 depuis le dossier du dépôt, le mini‑projet depuis `mini-projet-02/`.

---

## ❓ En cas de problème

| Message ou symptôme | Cause et remède |
|---|---|
| 🔴 **Mon dépôt est « Public »** | **Rendez‑le privé tout de suite** : dans votre dépôt, **Settings ▸ General**, descendez jusqu'à **Danger Zone**, **Change repository visibility ▸ Change to private**. |
| `FileNotFoundError` sur `data/titanic.csv` | Le notebook n'est pas ouvert depuis son dossier. Dans Colab, exécutez d'abord les deux lignes `!git clone …` et `%cd …` ci‑dessus ; sur votre ordinateur, rouvrez le notebook depuis `mini-projet-02/`. |
| Tout a disparu après avoir fermé l'onglet | La copie n'avait pas été faite (étape 2). Recommencez et faites **Fichier ▸ Enregistrer une copie dans Drive** dès l'ouverture. |
| Colab n'affiche pas mon dépôt privé | Cochez **Include private repos** dans l'onglet GitHub et autorisez Colab. |
| L'enseignant ne voit pas mon travail | Soit le notebook n'a pas été enregistré **dans votre dépôt** (**Fichier ▸ Enregistrer une copie dans GitHub**), soit l'enseignant n'est pas encore **collaborateur** (section « Partager votre dépôt avec l'enseignant », points 2 et 3). |
| Une cellule affiche `NameError` | Une cellule précédente n'a pas été exécutée : exécutez les cellules **dans l'ordre**, depuis le début. |
| Un ❌ qui ne part pas | Lisez les indices 1, 2, 3 de l'exercice, puis affichez vos variables avec `print`. |

---

## 🗂️ Contenu du dépôt

```
tp-seance-02.ipynb              Partie 1 : 39 exercices en 9 séries
mini-projet-02/
  mini-projet-02.ipynb          Partie 2 : mini-projet Titanic
  data/titanic.csv              le fichier de départ du mini-projet
```

Le dossier `result/` est créé par le notebook quand il écrit votre fichier `s2_titanic.csv`.
