# Reprise des marchés SAFI - D_FormulesActes

![Reprise Marchés SAFI - D_FormulesActes Diagramme](RepriseMarchesSAFI-D_FormulesActes_Diagramme.png)

## Créer une formule
```javascript
// Créer une formule
chargerPage('../../intranet/marc/CreerFormuleVariation.gda')
```

```javascript
// Choisir une formule
document.getElementsByName('typeFormuleVariation_miCode')[0].value="%ExcelData[LoopIndex]['Formule de variation du marché - Code']%";
RemplirFormulaire()
```

```javascript
// Suivant
effectuerSuivante()
```

```javascript
// Valider
Valider()
```

```javascript
// Retour
Retour(00, "../../intranet/marc/AfficheMarche.gda?cas=4&IDG=1&IDG=1&IDIP=IDIP_1670856590548&code=1078&ignorerIDIP=1&onglet=2&histoaction=-1")
```

## Créer un acte
```javascript
// Creer un acte
chargerPage('../../intranet/marc/CreerActe.gda', event);
```

```javascript
// Ajouter dates
document.getElementsByName('acte_mdtEffet')[0].value="%ExcelData[LoopIndex]['Notification du marché - Date d\'effet']%";
document.getElementsByName('acte_mdtSignature')[0].value="%ExcelData[LoopIndex]['Notification du marché - Date de signature']%";
document.getElementsByName('acte_mdtNotification')[0].value="%ExcelData[LoopIndex]['Notification du marché - Date de notification']%";
document.getElementsByName('acte_mdtArrete')[0].value="%ExcelData[LoopIndex]['Notification du marché - Date d\'accusé réception']%";
```

```javascript
// Page suivante
effectuerSuivante()
```

```javascript
Valider()
```

```javascript
Retour(00, "../../intranet/marc/ChargerRechercheMarche.gda?favCode=145&IDG=1&ignorerIDIP=1&ignorerIDIP=1&onglet=2&histoaction=-1")
```

```javascript
rch_jsp_BoutonRetour();
```

```javascript
rch_jsp_BoutonRetour();
```