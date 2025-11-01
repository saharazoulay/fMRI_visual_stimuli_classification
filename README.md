# fMRI_visual_stimuli_classification 

This project explores decoding **which movie clip** (or rest segment) a participant was watching based on fMRI brain activity patterns.  
Using data from the Human Connectome Project (HCP), the task involved classifying **14 movie clips and 14 rest periods** recorded from **170 subjects**, focusing on three functional brain networks: **Visual (VIS)**, **Dorsal Attention (DAN)**, and **Default Mode (DMN)**.

---

##  Project Overview

###  Part 1 - Movie Classification
- Each participant watched 14 movies, 50 seconds each.  
- Only the **first and last 5 seconds** of every clip were analyzed to capture temporal dynamics.  
- Models trained to identify *which movie* was being viewed based on the fMRI signal.

###  Part 2 - Rest Classification
- Between movie clips, participants experienced **14 rest periods** of approximately 20 seconds each.  
- Similar analysis was applied to the first and last 5 seconds of these segments.  
- The goal was to compare activation patterns between stimulus-driven and resting states.

###  Bonus Experiments
- Tested additional classifiers (**Random Forest, Logistic Regression, MLP**).  
- Introduced a **STD-based temporal feature**, which slightly reduced performance.  
- Compared **K-Fold** and **Group K-Fold** cross-validation (minimal differences observed).

---

##  Methods
- Extracted voxel activity from three functional brain networks: **VIS**, **DAN**, and **DMN**.  
- Converted 4D fMRI data into feature matrices with corresponding class labels.  
- Evaluated multiple classifiers: **LDA, QDA, SVM, KNN, and Naive Bayes**.  
- Results visualized using bar plots and confusion matrices for start vs. end segments.

---

##  Key Results
- The **DMN** network achieved the highest accuracy (**LDA = 0.86**) for movie-start segments.  
- **VIS** and **DAN** networks showed moderate accuracies (~0.5-0.6), likely reflecting passive viewing.  
- Rest classification yielded lower accuracy, supporting the idea of weaker activation patterns.  
- Simpler linear models (LDA, QDA) outperformed complex classifiers.

---

##  Insights
- Findings highlight the **DMN’s strong role in higher-level perceptual and memory processing** during movie viewing.  
- Even short fMRI segments (5s) contain sufficient temporal information to decode visual and cognitive context.  
- Demonstrates the potential of **machine learning for brain decoding** using concise, interpretable models.

---

##  Tools & Libraries
Python | NumPy | pandas | scikit-learn | matplotlib | nilearn | nibabel | Jupyter Notebook  

---

##  Authors
**Sahar Azoulay**, **Yarin Ben Saadon**, **Yair Kitron Kuperstein**  
Electrical & Electronics Engineering Department, Holon Institute of Technology (HIT)
