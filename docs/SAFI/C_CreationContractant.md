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
Variable "Colonne Contractant"
Contractant %LoopIndexContractant% - Tiers - Code
```

```javascript
// Remplir le Code Tiers
document.getElementsByName('contractantTiers_miCode')[0].value="%ExcelData[LoopIndex][ColonneContractant]%";
```
```javascript
lancerAllerRetourRPCTiers(document.forms[0], 'contractantTiers_miCode', 'contractantTiers_msLib', 'contractantRefBancaire_miCode', 'contractantRefBancaire_msLib', 'contractantTiers_miCode', null, 'callbackRetourARTiers','contracantRefBancaireTiers_miCode','contracantRefBancaireTiers_msLibelle','provenance');
```


```
Variable "Colonne Contractant"
Contractant %LoopIndexContractant% - Rôle - Code
```

```javascript
// Remplir le rôle
document.getElementsByName('contractantRole_msIdentif')[0].value="%ExcelData[LoopIndex][ColonneContractant]%";
```

```javascript
Si le rôle est mandataire :
%ExcelData[LoopIndex][ColonneContractant]% = MA
```

```javascript
Contractant %LoopIndexContractant% - Mandataire - Désignation
```



## Tiers

```javascript
// Remplir Désignation
document.getElementsByName('contractantMsDesignationGroupementMandataire')[0].value="%ExcelData[LoopIndex][ColonneContractant]%";
```

### Références bancaires

```javascript
// Cliquer sur la loupe
saisieAssisteeReferenceBancaire('contractantTiers_miCode', 'contracantRefBancaireTiers_miCode', 'contractantRefBancaire_miCode', 'contractantRefBancaire_msLib');
```

Attacher le navigateur
http://garec.cg29.local/intranet/glob/sass/recherchePopupRefTiers.gda

```javascript
// Obtenir le nombre de résultats
nb=document.getElementsByTagName('strong').length-3;
return nb;
```

Convertir le texte en nombre

Colonne contractant :
Contractant %LoopIndexContractant% - Iban à créditer
