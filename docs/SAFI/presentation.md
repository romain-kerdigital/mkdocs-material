# Reprise des marchés SAFI - Présentation

## Gestion des données

Un fichier Excel Online pour favoriser un travail collaboratif entre la DFP et la RPA.

Les modifications sont traitées en temps réel avec les données à jour pour permettre à la DFP de mettre à jour les valeurs et que la RPA puisse continuer les tests au fur et à mesure.

Le fichier Excel comporte environ 200 colonnes. Elles sont détaillées en [Annexe](#donnees-excel-projet-reprise-des-marches-safi)

[Lien vers le fichier Excel](https://1drv.ms/x/s!AmiJK4RIVLBXgSBT9GcikC_QRGv6?e=z07vII)

## Vision globale du projet

Un diagramme LucidChart est attaché au projet et permet de visualiser les différentes étapes.

Il permet de confirmer les étapes à paramétrer pour le robot en envisageant tous les cas possibles à traiter.

[Lien vers le diagramme LucidChart](https://lucid.app/lucidchart/481ce2c2-3b15-4080-a4a7-5e4b729edab0/edit?viewport_loc=-3659%2C-1579%2C45266%2C27069%2C0_0&invitationId=inv_0482e918-03d2-4dc7-ac95-2fddd838edbc)

## Procédure

![Reprise Marchés SAFI - main](RepriseMarchesSAFI-main.png)

[A_Initialisation](/SAFI/A_Initialisation) :
    - Fermer les applications ouvertes
    - Lire les données dans le fichier Excel
    - Se connecter à Grand Angle


Ensuite on démarre une boucle qui se répétera à chaque ligne du fichier Excel
Tous les contractants sont sur la même ligne (jusqu'à 10 contractants, d'où le nombre important de colonnes)

[B_CreationNouveauMarche](/SAFI/B_CreationNouveauMarche) :
    - Cliquer sur créer un nouveau marché et remplir les premières informations
    - Ajouter un type d'engagement
    - Remplir la forme et le type de prix
    - ...

[C_CreationContractant](/SAFI/C_CreationContractant) :
    - ...
    - ...

[D_FormulesActes](/SAFI/D_FormulesActes) :
    - ...
    - ...


[E_RapportExecution](/SAFI/E_RapportExecution) :
    - Récupérer informations
    - Ecrire informations dans Excel

[F_Finalisation](/SAFI/F_Finalisation) :
    - Fermer applications en cours

[G_RapportErreur](/SAFI/G_RapportErreur) :
    - Récupérer informations
    - Ecrire informations dans Excel