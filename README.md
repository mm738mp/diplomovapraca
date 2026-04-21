# Kódy k diplomovej práci – Automatizácia spracovania a analýzy dát v oblasti galaktickej astronómie

Tento repozitár obsahuje všetky Jupyter notebooky použité pri spracovaní dát,
segmentácii galaxií a výpočte zakrivenia (warp) galaktických diskov v rámci mojej diplomovej práce.

Notebooky sú rozdelené do troch častí:

# 1. Data preprocessing 
V týchto notebookoch prebieha príprava dát:

- Filtrovanie morfologického katalógu podľa pravdepodobnosti edge-on orientácie.  
- Generovanie FITS výrezov (cutoutov) pomocou WCS.  
- Tvorba log‑stretch vizualizácií z FITS súborov.  
- Automatické generovanie binárnych masiek z log‑stretch obrázkov.

# 2. Segmentation
Táto časť sa venuje segmentácii galaxií pomocou DeepLabV3+:

- Párovanie obrázkov a masiek, train/test split.  
- Tréning modelu DeepLabV3+.  
- Predikcia masiek na testovacej množine.  
- Čistenie a spracovanie predikovaných masiek.

# 3. Warp analysis
V tejto časti sa počíta zakrivenie galaktického disku:

- Vylepšenie masiek  
- PCA analýza a extrakcia stredovej línie  
- Výpočet warp krivky  
- Vizualizácie a export výsledkov

Repozitár obsahuje aj exportované *.csv* súbory s finálnymi výsledkami warp analýzy, ktoré sumarizujú parametre zakrivenia pre všetky spracované galaxie.

--------------------------------------------------------------------------------------------------

# Code for Master's Thesis – Automation of processing and analysis of data in galactic astronomy

This repository contains all Jupyter notebooks used for data processing,
galaxy segmentation, and warp analysis of galactic disks for my master's thesis.

# 1. Data preprocessing
These notebooks prepare the input data:

- Filtering the morphological catalogue by edge-on probability.  
- Generating FITS cutouts using WCS coordinates.  
- Creating log‑stretch visualizations from FITS files.  
- Automatic generation of binary masks from log‑stretch images.

# 2. Segmentation
This part focuses on galaxy segmentation using DeepLabV3+:

- Pairing images and masks, train/test split.  
- Training the DeepLabV3+ model.  
- Predicting masks on the test set.  
- Cleaning and post‑processing predicted masks.

# 3. Warp analysis
These notebooks compute the warp of each galaxy:

- Mask refinement  
- PCA-based midplane extraction  
- Warp curve computation  
- Visualizations and parameter export

The repository also includes exported *.csv* files containing the final warp analysis results, summarizing warp parameters for all processed galaxies.
