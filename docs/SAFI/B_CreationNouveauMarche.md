# Reprise des marchés SAFI - B_CreationNouveauMarche

![Reprise Marchés SAFI - B_CreationNouveauMarche_1](RepriseMarchesSAFI-B_CreationNouveauMarche_1.png)
![Reprise Marchés SAFI - B_CreationNouveauMarche_2](RepriseMarchesSAFI-B_CreationNouveauMarche_2.png)
![Reprise Marchés SAFI - B_CreationNouveauMarche_3](RepriseMarchesSAFI-B_CreationNouveauMarche_3.png)
![Reprise Marchés SAFI - B_CreationNouveauMarche_4](RepriseMarchesSAFI-B_CreationNouveauMarche_4.png)

## Cliquer sur créer un nouveau marché et remplir les premières informations

### Cliquer sur les éléments du menu

```javascript
//Cliquer sur les elements du menu
document.getElementsByClassName("bouton-menu")[0].click()
document.getElementsByClassName("mat-focus-indicator bandeau__button mat-button mat-button-base ng-star-inserted")[3].click()
document.getElementsByClassName('menu ng-star-inserted')[0].click()
document.getElementsByClassName('gda_bouton NouveauImg gda_bouton_actif')[0].click()
```

### Remplir la première page
```javascript
//Remplir les informations sur le marché
document.getElementsByName('marche_miAnnee')[0].value="%ExcelData[LoopIndex]['Numéro de marché - Année AAAA']%";
document.getElementsByName('marche_msNumero')[0].value="%ExcelData[LoopIndex]['Numéro de marché - Code']%";
document.getElementsByName('marche_msObjet')[0].value="%ExcelData[LoopIndex]['Objet']%";
```
### Cliquer sur Suivant

On lance le javascript associé au bouton Suivant.

```javascript
effectuerSuivante()
```
### Remplir la durée
```javascript
// Duree
document.getElementsByName('marcheDuree_miAnnees')[0].value="%ExcelData[LoopIndex]['Durée du marché - Années']%";
document.getElementsByName('marcheDuree_miMois')[0].value="%ExcelData[LoopIndex]['Durée du marché - Mois']%";
document.getElementsByName('marcheDuree_miJours')[0].value="%ExcelData[LoopIndex]['Durée du marché - Jours']%";
```

## Ajouter un type d'engagement

### Cliquer sur la loupe Type d'engagement

Plutôt que de cliquer sur la loupe directement, on lance le javascript associé.

```javascript
// Cliquer sur la loupe Type d'engagement
saisieAssisteeTypeEnga()
```

### Attacher la nouvelle fenêtre de navigateur


### Remplir la code à rechercher

```javascript
document.getElementsByName('typejCode')[0].value="%ExcelData[LoopIndex]['Type d\'engagement - Code']%";
```

### Cliquer sur le bouton Rechercher

On lance le script associé au bouton Rechercher
```javascript
rch_jsp_BoutonRechercher()
```

### CLiquer sur le premier élément de la liste
Ici, il n'y a pas de Name ou d'ID pour choisir l'élément à cliquer. On fait donc une recherche par TagName. Il s'agit du 5ème élément de la liste des "a" sur la page.
```javascript
document.getElementsByTagName('a')[4].click()
```
!!! note
    Pour déduire la recherche par TagName à utiliser. Dans l'inspecteur il faut regarder le type d'élément. Ici il s'agit d'un lien "a". On recherche ensuite par itération avec la console jusqu'à ce que notre élément soit sélectionné:
    ```javascript
      document.getElementsByTagName('a')[0]
      document.getElementsByTagName('a')[1]
      document.getElementsByTagName('a')[2]
      document.getElementsByTagName('a')[3]
      document.getElementsByTagName('a')[4]
    ```

## Remplir la forme, le type de prix et leur date d'établissement
### Forme de prix
Il s'agit d'un menu déroulant, mais on peut valoriser la valeur comme un champ de texte.
```javascript
// Forme de prix
document.getElementsByName('formePrix_miCode')[0].value="%ExcelData[LoopIndex]['Forme de prix - Code']%";
```

!!! note
    Pour simplifier l'automatisation, tous les choix possibles sont rassemblés dans la feuille "Listes" sur Excel avec la correspondance avec le code sur Grand Angle.
    Une colonne a ensuite été ajoutée sur la feuille principale en utilisant RECHERCHEV() qui affiche directement le code qui correspond à l'option à sélectionner.

### Type de prix

Il s'agit d'un bouton radio, mais on peut valoriser la valeur comme un champ de texte.
```javascript
// Type de prix
document.getElementsByName('typePrix_miCode')[0].value="%ExcelData[LoopIndex]['Type de prix - Code']%";
```

Après avoir sélectionné le type de prix, de nouvelles cases s'affichent.



## Choisir le Code CPV
## Remplir les Montants
## Remplir Mode de passation, dévolution et la gestion de la retenue de garantie
## Définir l'auto-liquidation de la sous-traitance
## Reconduction
## Définir les dates de consultation, de signature
## Délai de liquidation et fin du flux