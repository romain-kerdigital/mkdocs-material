# Mémo Javascript (Formulaire Grand Angle)

## Pointer sur un champ du formulaire
Tous les scripts commencent par "document", "document" correspond au contenu visible de la page.

### .getElementbyId
On peut alors pointer sur un champ du formulaire en le retrouvant grâce à son ID unique.
``` javascript
document.getElementById("test");
```
Toutefois, sur Grand Angle, la majorité des champs du formulaire n'ont pas d'ID renseigné.


### .getElementsByName
Sur Grand Angle, la majorité des champs du formulaire ont un "name" et pas d'ID.
Mais ce "name" n'est pas nécessairement unique sur la page il peut y avoir plusieurs éléments avec le même "name" contrairement à l'ID.
``` javascript
document.getElementsByName("test");
```
Ce code ci-dessus ne pointera pas sur l'élément même si le nom est utilisé une seule fois sur la page.
Il pointera vers la liste des éléments avec ce nom. (Même si la liste ne comporte qu'un seul élément)
Il faut donc pointer sur le premier élément de la liste : L'élement [0] de la liste.
``` javascript
document.getElementsByName("test")[0];
```
Ce code ci-dessus pointera sur le premier élément de la liste et s'il n'y a qu'un seul élément sur la page avec ce "name" il sera sélectionné également.

Si l'élement n'a ni ID et ni "name". Il est possible de pointer par rapport au "classname" et au "tagname".
On les verra sur des cas concrets.


## Remplir le champ du formulaire

### Cliquer sur un bouton
Pour cliquer sur un élément, il suffit d'ajouter .click() après avoir sélectionner l'élément à cliquer.
``` javascript
document.getElementsByName("test")[0].click();
```

Certains boutons comme "Page suivante", "Valider", "Retour" ou les onglets déclenchent uniquement des scripts très courts qui peuvent être repris directement.

### Remplir du texte dans le champ du formulaire
Pour remplir du texte, il suffit de changer la valeur de l'élément.
``` javascript
document.getElementsbyId('test').value="Texte";

```

> :warning: Attention ! En remplissant manuellement certaines cases, des scripts se lancent automatiquement parfois. (Notamment sur des montants)
Généralement on les retrouve dans le paramètre "onchange" de l'élément.
Lorsque l'on change uniquement la valeur par script, les scripts qui se lançaient automatiquement ne se lancent pas.
C'est notamment le cas pour tous les montants avec TVA calculée.

Il existe deux méthode pour simuler la saisie manuelle :
1. Reprendre le script avec l'inspecteur
2. Lancer le script avec onchange()

``` javascript
document.getElementsByName("test")[0].onchange();
```


## Cocher une case

## Choisir un élément dans une liste déroulante

## Choisir un élément dans une liste de boutons radio

## Exécuter un script javascript directement sur la page

## Cas particuliers