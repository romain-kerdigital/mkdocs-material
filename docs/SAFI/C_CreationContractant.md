# Reprise des marchés SAFI - C_CreationContractant

![Reprise Marchés SAFI - C_CreationNouveauContractant Diagramme](RepriseMarchesSAFI-C_CreationNouveauContractant_Diagramme.png)

```javascript
//Cliquer sur l'onglet détails
ChangerOnglet(2);
```
```javascript
// Créer un contractant
chargerPage('../../intranet/marc/CreerContractant.gda', event)
```

Etant donné qu'il y a le numéro du contractant variable dans le nom de colonne, par précaution, on assigne une nouvelle variable : "Colonne Contractant" qui contient le numéro dynamique du contractant :
```
Contractant %LoopIndexContractant% - Tiers - Code
```

```javascript
// Remplir le Code Tiers
document.getElementsByName('contractantTiers_miCode')[0].value="%ExcelData[LoopIndex][ColonneContractant]%";
```
```javascript
lancerAllerRetourRPCTiers(document.forms[0], 'contractantTiers_miCode', 'contractantTiers_msLib', 'contractantRefBancaire_miCode', 'contractantRefBancaire_msLib', 'contractantTiers_miCode', null, 'callbackRetourARTiers','contracantRefBancaireTiers_miCode','contracantRefBancaireTiers_msLibelle','provenance');
```