# Medicaments.gouv.fr
Latest update: 
Data version: 20 April 2016


Downloaded and analyzed files (source: http://base-donnees-publique.medicaments.gouv.fr/telechargement.php)

| Index  | File Name | Number of columns | Number of lines | 
| ------------- | ------------- |-------------|-------------|
| 1  | Fichier des spécialités (CIS_bdpm.txt) |12 |13994 |
| 2  | Fichier des présentations (CIS_CIP_bdpm.txt)  |13 |19712 |
| 3  | Fichier des compositions (CIS_COMPO_bdpm.txt)  |9 | 26067|
| 4  | Fichier des avis SMR de la HAS (CIS_HAS_SMR_bdpm.txt)  |6 |9099 |
| 5  | Fichier des avis ASMR de la HAS (CIS_HAS_ASMR_bdpm.txt) | 6|5112 |
| 6  | Fichier des liens vers les avis de la commission de la transparence de la HAS (HAS_LiensPageCT_bdpm.txt) |2 | 6018 |
| 7  | Fichier des groupes génériques (CIS_GENER_bdpm.txt) | 6| 8530|
| 8  | Fichier des conditions de prescription et de délivrance (CIS_CPD_bdpm.txt) |2 | 18175|
| 9  | Fichier des Informations importantes (CIS_InfoImportantes.txt) |6 | 2708|

```R
# Load required packages
library(data.table)
library(bit64)

# Data source: http://base-donnees-publique.medicaments.gouv.fr/telechargement.php

# File1: Fichier des spécialités (date de mise à jour : 29/04/2016, 2634 Ko)
CIS_bdpm <- fread('http://base-donnees-publique.medicaments.gouv.fr/telechargement.php?fichier=CIS_bdpm.txt')
head(CIS_bdpm)
dim(CIS_bdpm)

# File2: Fichier des présentations (date de mise à jour : 12/05/2016, 3801 Ko)
CIS_CIP_bdpm <- fread('http://base-donnees-publique.medicaments.gouv.fr/telechargement.php?fichier=CIS_CIP_bdpm.txt')
head(CIS_CIP_bdpm)
dim(CIS_CIP_bdpm)

# File3: Fichier des compositions (date de mise à jour : 29/04/2016, 2032 Ko)
CIS_COMPO_bdpm <- fread('http://base-donnees-publique.medicaments.gouv.fr/telechargement.php?fichier=CIS_COMPO_bdpm.txt')
head(CIS_COMPO_bdpm)
dim(CIS_COMPO_bdpm)

# File4: Fichier des avis SMR de la HAS (date de mise à jour : 29/04/2016, 2286 Ko)
CIS_HAS_SMR_bdpm <- fread('http://base-donnees-publique.medicaments.gouv.fr/telechargement.php?fichier=CIS_HAS_SMR_bdpm.txt')
head(CIS_HAS_SMR_bdpm)
dim(CIS_HAS_SMR_bdpm)

# File5 Fichier des avis ASMR de la HAS (date de mise à jour : 29/04/2016, 1438 Ko)
CIS_HAS_ASMR_bdpm <- fread('http://base-donnees-publique.medicaments.gouv.fr/telechargement.php?fichier=CIS_HAS_ASMR_bdpm.txt')
head(CIS_HAS_ASMR_bdpm)
dim(CIS_HAS_ASMR_bdpm)

# File6: Fichier des liens vers les avis de la commission de la transparence de la HAS (date de mise à jour : 29/04/2016, 329 Ko)
HAS_LiensPageCT_bdpm <- fread('http://base-donnees-publique.medicaments.gouv.fr/telechargement.php?fichier=HAS_LiensPageCT_bdpm.txt')
head(HAS_LiensPageCT_bdpm)
dim(HAS_LiensPageCT_bdpm)

# File7: Fichier des groupes génériques (date de mise à jour : 29/04/2016, 938 Ko)
CIS_GENER_bdpm <- fread('http://base-donnees-publique.medicaments.gouv.fr/telechargement.php?fichier=CIS_GENER_bdpm.txt')
head(CIS_GENER_bdpm)
dim(CIS_GENER_bdpm)

# File8: Fichier des conditions de prescription et de délivrance (date de mise à jour : 29/04/2016, 692 Ko)
CIS_CPD_bdpm <- fread('http://base-donnees-publique.medicaments.gouv.fr/telechargement.php?fichier=CIS_CPD_bdpm.txt')
head(CIS_CPD_bdpm)
dim(CIS_CPD_bdpm)

# File9: Fichier des Informations importantes (génération en direct)
CIS_InfoImportantes <- fread('http://base-donnees-publique.medicaments.gouv.fr/telechargement.php?fichier=CIS_InfoImportantes.txt')
head(CIS_InfoImportantes)
dim(CIS_InfoImportantes)


```

