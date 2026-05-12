# AI Healthcare Neurological Analysis Platform

## Overview

This project was developed at **Esprit School of Engineering** in collaboration with **Razi Hospital** as part of an AI healthcare research and innovation initiative focused on neurological disorder analysis.

The platform combines Artificial Intelligence, Deep Learning, Computer Vision, MRI analysis, fMRI connectivity analysis, EEG processing, and neuromotor video analysis to detect hidden neurological abnormalities and support medical interpretation.

---

## Features

* Alzheimer’s disease MRI analysis
* Parkinson’s disease vs atypical parkinsonism classification
* Cerebellar dysfunction MRI analysis
* Uneven brain aging analysis
* Functional brain connectivity analysis using fMRI
* Epilepsy vulnerability and network instability detection
* Ataxia neuromotor instability detection using video analysis
* Explainable AI visualizations
* AI-assisted neurological interpretation

---

## Tech Stack

### Frontend
- React
- TanStack Start
- Vite
- TypeScript
- npm

### Backend
- Django
- Django REST Framework
- Python
- Django ORM
- SQLite (development database)

### AI / Machine Learning
- Scikit-learn models (`.pkl`)
- PyTorch for Axis 4 brain aging
- Grad-CAM / SHAP for explainability
- Mock AI outputs for demo-ready axes

### Other Tools
- GitHub
- PowerShell script for local development (`dev-all.ps1`)
- cURL for API testing

---

## AI Axes

### Axis 1 — Alzheimer’s vs Healthy Subjects

MRI-based AI analysis for Alzheimer-like structural abnormalities.

### Axis 2 — Parkinson’s vs Atypical Parkinsonism

Deep learning classification of Parkinson’s disease and atypical syndromes.

### Axis 3 — Cerebellar Dysfunction

Computer Vision and MRI analysis of cerebellar neurological disorders.

### Axis 4 — Uneven Brain Aging

Explainable AI framework for heterogeneous brain aging analysis.

### Axis 5 — Functional Connectivity

fMRI-based brain connectivity and cognitive load analysis.

### Axis 6 — Neuromotor Video

Ataxia and neuromotor instability detection using pose estimation and temporal motion analysis.

### Axis 7 — Epilepsy Vulnerability

EEG and fMRI network instability analysis for epilepsy vulnerability detection.

---

## Directory Structure

```bash
backend/
├── axis1_alzheimer_dementia/
├── axis2_parkinson_atypical/
├── axis3_cerebellar_dysfunction/
├── axis4_brain_aging/
├── axis5_functional_connectivity/
├── axis6_neuromotor_video/
├── axis7_epilepsy_network/

src/
assets/
datasets/
models/
