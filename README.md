# brAIn — AI-powered Neurology Decision Support

A demo-ready clinical AI platform that allows clinicians and researchers to upload neurological data (MRI, fMRI, EEG, and video), run specialized AI models for each neurological axis, and generate explainable decision-support reports.

This project was developed at **Esprit School of Engineering** in collaboration with **Razi Hospital** as part of an AI healthcare research and innovation initiative focused on neurological disorder analysis.

The platform combines Artificial Intelligence, Deep Learning, Computer Vision, MRI analysis, fMRI connectivity analysis, EEG processing, and neuromotor video analysis to detect hidden neurological abnormalities and support medical interpretation.

---

## Repository Structure

```bash id="r7s8v2"
.
├── src/         # Frontend — React + TanStack Start (Vite)
└── backend/     # Backend — Django + Django REST Framework
```

The backend is organized into one application per neurological axis. Each team member is responsible for integrating and maintaining one AI axis.

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
* Demo-ready clinical workflow
* Modular AI integration per axis

---

## Tech Stack

### Frontend

* React
* TanStack Start
* Vite
* TypeScript
* npm

### Backend

* Django
* Django REST Framework
* Python

### AI / Machine Learning

* Scikit-learn models (`.pkl`)
* PyTorch for Axis 4 brain aging
* Grad-CAM / SHAP for explainability
* Mock AI outputs for demo-ready axes

### Other Tools

* GitHub
* PowerShell script for local development (`dev-all.ps1`)
* cURL for API testing

---

## The 7 AI Axes

| Axis   | Description                          | Data Type    | Folder                                   |
| ------ | ------------------------------------ | ------------ | ---------------------------------------- |
| Axis 1 | Alzheimer's vs Healthy Subjects       | MRI          | `backend/axis1_alzheimer_dementia/`      |
| Axis 2 | Parkinson's vs Atypical Parkinsonism | MRI          | `backend/axis2_parkinson_atypical/`      |
| Axis 3 | Cerebellar Dysfunction               | MRI          | `backend/axis3_cerebellar_dysfunction/`  |
| Axis 4 | Uneven Brain Aging                   | MRI          | `backend/axis4_brain_aging/`             |
| Axis 5 | Hidden Cognitive Effort              | fMRI         | `backend/axis5_functional_connectivity/` |
| Axis 6 | Neuromotor Video                     | Video        | `backend/axis6_neuromotor_video/`        |
| Axis 7 | Epilepsy Vulnerability               | EEG / Signal | `backend/axis7_epilepsy_network/`        |

---

## Directory Structure

```bash id="c8knj6"
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
```

---

## Getting Started

### Frontend

```bash id="ljq3r4"
npm install
npm run dev
```

### Backend

```bash id="mr2pt8"
cd backend
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py runserver 0.0.0.0:8000
```

### Run Frontend + Backend on Windows

```powershell id="8p0eq4"
.\dev-all.ps1
```

This script automatically launches Django in a second PowerShell window and starts the Vite frontend development server.

---

## Smoke Test

```bash id="g3m5fy"
curl -X POST http://localhost:8000/api/axis1-alzheimer-dementia/analyze/ \
  -F 'metadata={"demo":true}'
```

The API returns a realistic mock result even without trained `.pkl` models.

---

## AI Integration Workflow

Each team member only needs to:

1. Add their trained `.pkl` model inside the correct axis folder.
2. Edit `ml/inference.py`
3. Replace mock explainability outputs inside `explain/explainer.py`
4. Test the API endpoint with sample neurological data.

The frontend, serializers, persistence layer, and API routes are already connected.

---

## Deployment

### Frontend

The frontend can be deployed using Vercel or any static hosting platform.

### Backend

The Django backend can be deployed on:

* Render
* Railway
* Fly.io
* Virtual Machines (VM)

Environment variables:

* `DJANGO_SECRET_KEY`
* `DJANGO_DEBUG=0`
* `CORS_ALLOWED_ORIGINS`

---

## Keywords

Artificial Intelligence, Deep Learning, Healthcare AI, MRI Analysis, fMRI, EEG, Computer Vision, Explainable AI, Neurology, Medical Imaging, React, Django, Django REST Framework, PyTorch, Scikit-learn, Vite, TypeScript.

---

## Acknowledgments

This project was developed at **Esprit School of Engineering** with academic supervision and collaboration with **Razi Hospital**.
