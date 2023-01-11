# Mémo Javascript - Grand Angle

!!! Warning
    Ces codes fonctionnent dans le cadre de l'automatisation de Reprise des marchés SAFI, mais il faut quand même vérifier avec l'inspecteur de Microsoft Edge au cas où Grand Angle effectue une mise à jour ou bien si la fonction n'est pas exactement la même.

## Enlever le bandeau lors de la connexion
``` javascript
// Enlever bandeau
document.cookie = "rgpdInfosHidden=1; path=/;";
document.getElementsByClassName("mat-snack-bar-container")[0].style.display = "none";
```

## Passer à la page suivante
``` javascript
// Page suivante
effectuerSuivante()
```

## Cliquer sur Valider
``` javascript
Valider()
```

## Cliquer sur Enregistrer
``` javascript
// Enlever bandeau
document.cookie = "rgpdInfosHidden=1; path=/;";
document.getElementsByClassName("mat-snack-bar-container")[0].style.display = "none";
```
## Cliquer sur Retour
``` javascript
// Enlever bandeau
document.cookie = "rgpdInfosHidden=1; path=/;";
document.getElementsByClassName("mat-snack-bar-container")[0].style.display = "none";
```
### Cliquer sur Rechercher
```javascript
rch_jsp_BoutonRechercher()
```

## Simuler la saisie manuelle des montants pour le calcul de la TVA
``` javascript
// Enlever bandeau
document.cookie = "rgpdInfosHidden=1; path=/;";
document.getElementsByClassName("mat-snack-bar-container")[0].style.display = "none";
```

## Cliquer sur une loupe
```javascript
// Cliquer sur la loupe Type d'engagement
saisieAssisteeTypeEnga()
```

## Sélectionner un élément sans ClassName
On peut chercher avec le TagName : [Voir exemple](../SAFI/B_CreationNouveauMarche/#cliquer-sur-le-premier-element-de-la-liste)
```javascript
document.getElementsByTagName('a')[4].click()
```