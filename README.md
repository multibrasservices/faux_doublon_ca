# Détecteur de Faux Doublons pour Rapprochement Bancaire

Outil web pour détecter les écarts et "faux doublons" entre un extrait du Grand-Livre (logiciel GADM) et un relevé bancaire (Crédit Agricole).

![Aperçu de l'application](mon_logo.png)

## Contexte du projet

Cet outil a été développé pour résoudre un problème spécifique et récurrent lors du rapprochement bancaire pour les entités du groupement Les Mousquetaires utilisant le logiciel comptable GADM.

Il arrive fréquemment que des montants identiques apparaissent un nombre de fois différent entre l'extrait du compte 512 du Grand-Livre et le relevé bancaire. Ces "faux doublons" peuvent être fastidieux à identifier manuellement. Cette application automatise la détection de ces écarts.

## Fonctionnalités

- **Chargement de fichiers Excel :** Importez directement l'extrait du Grand-Livre et le relevé bancaire.
- **Analyse côté client :** Aucune donnée n'est envoyée sur un serveur. L'analyse se fait entièrement dans votre navigateur pour une confidentialité totale.
- **Tableau de résultats clair :** Affiche uniquement les montants qui n'ont pas le même nombre d'occurrences dans les deux fichiers.
- **Détails des transactions :** Pour chaque écart, l'outil précise les dates et les numéros de pièce comptable du Grand-Livre.
- **Calcul de l'écart total :** Fournit le solde total des anomalies détectées.

## Comment l'utiliser ?

1.  Ouvrez le fichier `index.html` dans votre navigateur (ou accédez à l'URL GitHub Pages).
2.  **Chargez l'extrait du Grand-Livre (512)** au format `.xlsx` ou `.xls`.
3.  **Chargez le relevé bancaire** au format `.xlsx` ou `.xls`.
4.  Cliquez sur le bouton **"Analyser les fichiers"**.
5.  Les résultats s'affichent en dessous.

### Format des Fichiers Attendu

Pour que l'analyse fonctionne correctement, les fichiers Excel doivent respecter une structure précise :

-   **Fichier du Grand-Livre (GADM) :**
    -   Les données doivent commencer à la **ligne 8**.
    -   Date : Colonne **B**
    -   N° de pièce : Colonne **F**
    -   Montant au débit : Colonne **H**
    -   Montant au crédit : Colonne **J**

-   **Fichier du Relevé Bancaire (Crédit Agricole) :**
    -   Les données doivent commencer à la **ligne 11**.
    -   Date : Colonne **A**
    -   Montant au débit : Colonne **C**
    -   Montant au crédit : Colonne **D**

## Déployer sur GitHub Pages

Pour rendre cet outil accessible en ligne facilement et gratuitement :

1.  Créez un nouveau dépôt **public** sur GitHub (par exemple, `detecteur-faux-doublons`).
2.  Uploadez les fichiers `index.html`, `mon_logo.png` et `README.md` dans ce dépôt.
3.  Allez dans les **Settings** (Paramètres) de votre dépôt.
4.  Dans le menu de gauche, cliquez sur **Pages**.
5.  Sous "Branch", sélectionnez la branche `main` (ou `master`) et laissez le dossier à `/root`.
6.  Cliquez sur **Save**.
7.  Attendez quelques minutes. Votre site sera disponible à l'adresse `https://VOTRE_NOM_UTILISATEUR.github.io/faux_doublon_ca`.

## Auteur

Développé par **Multibrasservices**.
*Version : 06.08.25*
