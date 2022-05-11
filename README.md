# PDSSS
Fichier de reproduction du projet "La diffusion des goûts culturels: le cas des prénoms bretons" dans le cadre du projet DSSS

Ce repository contient:
  - les fichiers d'inputs nécessaires à la reproduction
  - les codes : 1) Creation de la base de travail ; 2) Estimation des modèles ; 3) Analyse de l'autocorrélation spatiale

Les fichiers d'inputs sont issus directement des données en libre accès (fichier des prénoms sur l'INSEE), ou bien issus de traitements annexes à partir de données géographiques qu'il n'est pas nécessaire de reproduire ici (distance entre centroides de départements, base de départements contigus), ou pas possible à reproduire facilement (la base du recensement de l'INSEE a du être traitée à part sur SAS pour tirer les variables par année et par département). Plus précisément, ces fichiers d'inputs sont:
  - prenoms_bretons.xlsx : liste de prénoms bretons créée à partir de dictionnaires en ligne 
  - dpt2020.csv : fichiers des prénoms de l'INSEE
  - prop_bretons_annee_dep_new.xlsx : prop de personnes nées en bretagne par année et département (issue du recensement)
  - compo_csp_pond_new.xlsx : base avec proportion par année et departement des PCS (issue du recensement)
  - contiguous.xlsx et contiguous_cols.xlsx : bases des départements voisins par département (deux formats différents). Contiguous_cols_nobret est le même fichier sans la Bretagne
  - RP_pour_densite.xlsx: variable de nombre d'habitants par km² par département et année (issue du recensement)


D'autre part, les fichiers de code sont:
- 01_Creation_bases.Rmd : création des bases finales de travail par année et département, et par paires de département. Les fichiers d'output de 01_Creation_bases.Rmd sont à utiliser dans les deux codes suivants.
- 02_Modeles_regressions.Rmd : estimation des modèles présentés dans la note
- 03_Autocorr_spatiale.Rmd : approfondissement des questions d'autocorrélation spatiales.
