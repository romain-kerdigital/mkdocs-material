# Mémo Javascript - Grand Angle

!!! Warning
    Ces codes fonctionnent dans le cadre de l'automatisation de Reprise des marchés SAFI, mais il faut quand même vérifier avec l'inspecteur de Microsoft Edge au cas où Grand Angle effectue une mise à jour ou bien si la fonction n'est pas exactement la même.

## Enlever le bandeau lors de la connexion
``` javascript
// Enlever bandeau
document.cookie = "rgpdInfosHidden=1; path=/;";
document.getElementsByClassName("mat-snack-bar-container")[0].style.display = "none";
```

## Cliquer sur des boutons
### Passer à la page suivante
``` javascript
// Page suivante
effectuerSuivante()
```

### Cliquer sur Valider
``` javascript
Valider()
```

### Cliquer sur Enregistrer
``` javascript
// Enlever bandeau
document.cookie = "rgpdInfosHidden=1; path=/;";
document.getElementsByClassName("mat-snack-bar-container")[0].style.display = "none";
```
### Cliquer sur Retour
``` javascript
// Cliquer sur Retour
Retour(00, "../../intranet/marc/AfficheMarche.gda?cas=4&IDG=1&IDG=1&IDIP=IDIP_1670579254806&code=1052&ignorerIDIP=1&onglet=2&histoaction=-1")
```

``` javascript
// Cliquer sur Retour
Retour(00, "../../intranet/marc/AfficheMarche.gda?cas=4&IDG=1&IDG=1&IDIP=IDIP_1670856590548&code=1078&ignorerIDIP=1&onglet=2&histoaction=-1")
```

### Cliquer sur Rechercher
```javascript
rch_jsp_BoutonRechercher()
```

## Créer un nouvel élément

```javascript
//Cliquer sur l'onglet détails
ChangerOnglet(2);
```

```javascript
// Créer un contractant
chargerPage('../../intranet/marc/CreerContractant.gda', event)
```

```javascript
// Créer une formule
chargerPage('../../intranet/marc/CreerFormuleVariation.gda')
```

```javascript
// Creer un acte
chargerPage('../../intranet/marc/CreerActe.gda', event);
```

## Cliquer sur une loupe
```javascript
// Cliquer sur la loupe Type d'engagement
saisieAssisteeTypeEnga()
```
```javascript
// Cliquer sur la loupe Références Bancaires
saisieAssisteeReferenceBancaire('contractantTiers_miCode', 'contracantRefBancaireTiers_miCode', 'contractantRefBancaire_miCode', 'contractantRefBancaire_msLib');
```


```